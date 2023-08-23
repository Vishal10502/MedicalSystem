
## Deploy Application using ngnix-aspnet-mysql Containers and Docker compose


**Task 1 (v1):**

   In this task I created an Amazon EC2 instance, utilizing user data to automatically install Docker during launch. Establish an SSH connection to the instance and execute the command 'docker info' to retrieve Docker-related information.


Steps:

**1. Create EC2 Instance:**

             - Log in to your AWS Management Console. 
             - Navigate to the EC2 dashboard. 
             - Click "Launch Instance" and choose an Amazon Machine Image (AMI) that suits                   .                  your needs. 
             - Configure the instance settings (instance type, VPC, subnet, etc.). 
             - Add storage, tags, and security group settings as required. 
             - Review and launch the instance.

             
**2. Add User Data:**

 -  While configuring the instance, find the "Advanced Details" or "Configure    Instance" section. 
 - Locate the "User data" field.
 -  Add a cloud-init script to install Docker, for example: #include get.docker.com.

**3. Launch Instance:**
- Continue through the instance launch process and choose or create an SSH key pair for secure access.
Connect via SSH:
- Once the instance is running, note its public IP address or DNS name. 
- Open terminal (for Windows, you can use tools like PuTTY or Windows Subsystem for Linux).
- Run the following command to connect via SSH: (take path according to your pc)

  
    **Command:**
  
    ``` ssh -i key.pem ubuntu@IP_address ```
  
**4. Run Docker Info:**

- After successfully connecting to the EC2 instance via SSH, you'll be in the instance's command-line interface. 
- Run the following command to check Docker information:
  
  **Command:**
  
    ` docker info `



