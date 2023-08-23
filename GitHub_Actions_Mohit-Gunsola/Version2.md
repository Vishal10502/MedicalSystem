# GitHub actions:
## Task 2(V2): 
In this task with the help of github actions we are creating a s3 bucket and copying .war file into that bucket. <br>

## CI/CD architecture : <br> 

![main v2](https://github.com/NubeEra-Projects/MedicalSystem/assets/103624779/7d826e00-b77b-4c20-a478-3c97c5125c41)




### Create main.tf write the below content: <br>

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
 

### Create JavaMvnJUnitApp.yml file and write the below content: <br>
Now make a .github folder, make new workflows folder in it and make new file .YAML file with .yml or .yaml. <br>

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

* **name** in above file is optional. It is used to give the message. <br>
* **on** is for the command on which you want the file to be executed. <br>
* **jobs** are used to write different task you want to execute and write the commands. <br>
* **run** is used to execute the commands. <br>

Open the terminal in VS code and push the changes by using below commands. <br>

1. **git add** : Adds a change in the working directory to the staging area. <br>
```
git add .

```

2. **git commit** :It records the changes to the repository. <br>

```
git commit -m "V1.2"

```

3. **git push** : It upload local repository content to a remote repository.. <br>
```
git push orgin V2
```

## Output:
* The changes will be reflected in the repository under actions section. <br>

![image](https://github.com/NubeEra-Projects/MedicalSystem/assets/103624779/bdc9d62e-4a94-45da-9c00-1cebb8f91ddc)
![image](https://github.com/NubeEra-Projects/MedicalSystem/assets/103624779/f33d5ff0-38d0-48f9-a079-76298139d981)

## Auto deployment of artifacts: <br>

* s3 bucket will be created in aws automatically and .war file will also get uploaded. <br>

![image](https://github.com/NubeEra-Projects/MedicalSystem/assets/103624779/8517ad54-8678-4bc5-882a-6b461c0976e7)
![image](https://github.com/NubeEra-Projects/MedicalSystem/assets/103624779/59fcc783-d242-45ac-98c3-a2b3dd98ee8b)














