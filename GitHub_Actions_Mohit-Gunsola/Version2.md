## Github Actions:
## Task 2(V2): Maven(maven package, copy .jar to S3 bucket)-- In this task I have to create a CI pipeleine . I need to install mave,craete a S3 bucket and need to upload .jar file in the newly created bucket. All actions should take place using Github Actions only.
 
In main.tf<br>
-->Set up the required version for terraform. <br>
--> Create a access key and secrear access key in aws console and give those key in .tf file. <br>
-->Give the name of bucket in .tf which you want to create. <br>
```
terraform {
  required_version = ">= 0.12.26"
}

provider "aws" {
  access_key = "AKIA4DN5TV67QKAZGJ3M"
  secret_key = "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"
  region     = "us-east-1"
}

resource "aws_s3_bucket" "b" {
  bucket = "my-bkt-21-aug"
  acl    = "private"

  versioning {
    enabled = true
  }
}

```


In JavaMvnJUnitApp.yml <br>

--> Clone a Repositories(https://github.com/NubeEra-MCO/CICD-GithubActions-Java.git)<br>
-->  Install Java and Maven Versions<br>
--> Clean Project <br>
--> Build & Test Project <br>
-->Infrastructure Provisioning (initialize,Plan,Apply) <br>
-->Deploy and Run Project.<br>

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
          java-version: '17'
          distribution: 'temurin'

      - name: 2. Config Tools(Terraform)
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

      - name: 6. Build & Test Project
        run: mvn package 
      
      - name: 7. Infrastructure Provisioning(Initialize)
        run: terraform init

      - name: 8. Infrastructure Provisioning(Plan)
        run: terraform plan 

      - name: 9. Infrastructure Provisioning(Plan)
        run: terraform apply -auto-approve -input=false

      - name: 10. Deploy and Run Project
        run: |
          cd target/classes
          java com.mycompany.app.Calculator

```



Submitted by-Mohit Gunsola

