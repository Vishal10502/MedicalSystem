**CREATING MAIN.TF FILE** <br>
```
terraform {
  required_version = ">= 0.12.26"
}
provider "aws" {
  access_key = "AKIASMJSK6OY2YJ5H65A"
  secret_key = "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"
  region     = "us-east-1"
}
resource "aws_s3_bucket" "b" {
  bucket = "bkt-vishal-final"
  acl    = "private"
  versioning {
    enabled = true
  }
}
```
<br>

**CREATING S3 BUCKET AND ADDING .war FILE TO IT** <br>
*Here the access and secret access keys shoukd be different for each individual** <br>
*AT the botton we have copied the .war file into the created bucket* <br>
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
          export AWS_ACCESS_KEY_ID=AKIASMJSK6OY2YJ5H65A
          export AWS_SECRET_ACCESS_KEY=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
          export AWS_DEFAULT_REGION=us-east-1
          aws s3 ls 
          aws s3 cp Tomcat-DeployWAR.war s3://bkt-vishal-final
```
<br>

**BUCKET WITH NAME- bkt-vishal-final WILL BE CREATED IN THE AWS S3** <br>
<img width="958" alt="Screenshot 2023-08-22 233831" src="https://github.com/NubeEra-Projects/MedicalSystem/assets/91366680/ded7eb5e-0cdd-407a-8c20-b35d57cd0e3b">
<br>

**.war file is in the bucket**<br>
<img width="934" alt="Screenshot 2023-08-22 234038" src="https://github.com/NubeEra-Projects/MedicalSystem/assets/91366680/1d0ea37a-f954-4c5e-b104-2d683af306cd">
<br>

