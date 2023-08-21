# Terraform version 2
### -Create main.tf file and add the following content
```
terraform {
 required_version = ">= 0.12.26"
 } 
provider "aws" { 
access_key = " " 
secret_key = " "
region = "us-east-1" 
} 
resource "aws_s3_bucket" "b" {
 bucket = "my-tf-your-18augbucket22" 
acl = "private"
 versioning { 
enabled = true 
} 
}
```
Now make a .github folder, make new workflows folder in it and make new file .YAML file with .yml or .yaml
-	Add the following content into YAML file 
```
name: Perform CICD Operations on Console Based Java Application
```
```	
on: push
 ```
 ```
	jobs:
```
	  MyJob:
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

- **name** in above file is optional
- **on** is for the command on which you want the file to be executed
- In **jobs** you can write different task you want to execute and write following commands

- Now, open terminal in vs code and do
 ``` git add . ```
 to add everything
- the run 
```git commit –m “any _message”```
- now to push changes to github run 
```git push –u origin main```

When you press enter the yaml file gets executed and the job will be performed which will create an s3 bucket and run the java maven file
