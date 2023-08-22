# GitHub actions:
## Task 2(V2): 
In this task with the help of github actions we are creating a s3 bucket and copying .war file into that bucket. <br>

## Create main.tf write the below content: <br>

```

terraform {
  required_version = ">= 0.12.26"
}

provider "aws" {
  access_key = "AKIA4DN5TV67YT3EE52A"
  secret_key = "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"
  region     = "us-east-1"
}

resource "aws_s3_bucket" "b" {
  bucket = "mohit-bkt-22-august"
  acl    = "private"

  versioning {
    enabled = true
  }
}

```

## Create JavaMvnJUnitApp.yml file and write the below content: <br>

```
name: Perform CICD Operations on Console Based Java App
on: push
jobs:
  CICD:
    runs-on: ubuntu-latest
    steps:
      - name: 1. Config Tools(JAVA, MVN)
        uses: actions/setup-java@v3
        with:
          java-version: '11'
          distribution: 'temurin'

      - name: 2. Provision Tools(Terraform)
        uses: hashicorp/setup-terraform@v2
        with:
          terraform_version: 1.5.5

      - name: 3. Check Java and Maven Versions
        run: |
          java -version
          javac -version
          mvn --version
          terraform --version

      - name: 4. Clone Project
        uses: actions/checkout@v3     

      - name: 5. Clean Project
        run: mvn clean

      - name: 6. Build ,Test and Packaging Project
        run: mvn package 
      
      - name: 7. Infrastructure Provisioning(Initialize)
        run: terraform init

      - name: 8. Infrastructure Provisioning(Plan)
        run: terraform plan 

      - name: 9. Infrastructure Provisioning(Apply)
        run: terraform apply -auto-approve -input=false

      - name: 10. Deploy and Run Project
        run: |
          cd target
          export AWS_ACCESS_KEY_ID=AKIA4DN5TV67YT3EE52A
          export AWS_SECRET_ACCESS_KEY=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
          export AWS_DEFAULT_REGION=us-east-1
          aws s3 ls
          aws s3 cp Tomcat-DeployWAR.war s3://mohit-bkt-22-august

```









