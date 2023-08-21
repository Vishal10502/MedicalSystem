# **Terraform version 1**

 Step 1: Create Key pair

 Step 2: Create security group

Step 3: Create EC2 Instance 

Step 4: Open command prompt run following commamds
```
-	Cd .ssh
-	Ssh –I key_pair_file_name.pem ubuntu@public_IP_address
-	Sudo su
-	Visit www.terraform/download and copy following commands and run
-	wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
-	echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
-	sudo apt update && sudo apt install terraform
```
**Make directory using mkdir directory_name**

# Example 1

```
-	cd Example1/
-	ls –ltra
-	Now create main.tf using vi editor
-	Vi main.tf
-	Vi editor is in reading mode by default to change it to writing press ‘I’ 
-	Now write the following content into the file
-	Resource “local_file” “myfile”{
content = “This is my text”
filename = “%mytextfile.txt”
}
-	Press esc to go to read mode
-	Press shift + ‘:’  and now write mode to quit “wq!”
-	Now to look into main. Tf run “cat main.tf”
-	Aias tf = terraform, aliasing to call terraform with short variable name
-	Tf init, to initialize the terraform and get required files
-	Tf plan
-	Tf apply
-	Now it run whatever written in main.tf file
-	Come out of the folder and create new folder using command
```
# Example 2
```
-	 “cd .. && mkdir Ex-2 && cd Ex-2”
-	Cat > main.tf , > sign is used to write a new file 
-	Write 
Terraform {
Required_version = “>=0.12.26”
}
Output “Welcome_world” {
Value = “Welcome, world!”
}
-	Press enter
-	To stop, save and exit from editor we press ctrl + Z
-	Tf init
-	Tf plan 
-	Tf apply 
-	Terraform will run main.tf and give output
```
# Example 3
```
-	Cd .. && Mkdir Ex-3
-	Cd Ex-3
-	cat<<EOF > main.tf 
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
-	EOF
-	Versioning maintains history of our data
-	Tf init
-	Tf plan
-	Tf apply, you can check the bucket is created
-	Now to destroy the bucket we will run following command
-	Tf destroy
```