# V1 #
DATABASE INFRASTRUCTURE PREPARATION : 

Step-By-Step 
Process for creating an EC2 instance :

CREATING AN EC2 INSTANCE 
Step 1: First, login into your AWS account and click on “services” 
Step 2: From the drop-down menu of options, tap on “EC2 " 
Step 3: For Creating an Instance we first need to create a "KEY PAIR " 
       3.1: Under Resources click-on Key pairs 
       3.2: Now Create a new keypair by clicking on "create key pair " at the top right of the section 
       3.3: Now enter the key pair name , select key pair type to RSA or ED25519 respectively 
       3.4: Now selectthe private key type as .pem or .ppk according to your working enviornment 
       3.5: Now Finally click-on create keypair 
Step 4: After successfully creating a keypair we now need to create a security group 
       4.1: Under the Resources click-on Security Groups 
       4.2 We already have an existing security group ie: the default security group but for our requirements
           we well create a new one  
       4.2: So now Create a new security group by clicking on "create security group "
       4.3: Fill in the security group name , description , vpc info and then add inbound rules to it
       4.4: Select in-bound rules and add a new rule with type as "All Traffic" and source as "IPV4"
       4.5: Click-on create security group
Step 5: Now for creating an instance 
       5.1: click on instance under the resources section 
       5.2: Click on launch instance ,  after clicking on it you will be redirected to a launch page where 
         we can create instance   
       5.3: Create a name for the instance
       5.4: Select AMI – Required operating system from the available.
       5.5: I am selecting Ubuntu AMI as we need to create Ubuntu instance.
           By default, it selects a free tier storage.
       5.6: Select instance type
           By default, instance type is “t2.micro” which is free tier eligible service.
           Do not select any other which leads to billing amount.
       5.7 Now Select the key pair which me made earlier .
       5.8 In the network setting Select to existing security group and under that 
           select the Security group which we had prepared earlier . 
       5.9 Click on launch the instance

Step 6: After Launching the instance right click-on the instance and select the option connect 
Step 7: It automatically takes us to "Connect to Instance" page 
Step 8: Now here select "Connect to EC2 instance connect"
Step 9 Click on Connect
Step 10: We get re-directed to a new page in which we now have the terminal 

#V2#

Installing & Connecting MySql Server and then further Creating a Database 

COMMANDS USED TO HOST MYSQL SERVER ON AWS EC2 INSTANCE :

 
Step 1: Update the system
-sudo apt update
Step 2: Install MySql
-sudo apt install mysql-server
Step 3: Check the Status of MySql (Active or Inactive)
-sudo systemctl status mysql
Step 4: Login to MySql as a root
-sudo mysql
Step 5: Update the password for the MySql Server
-ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'place-your-password-here';
-FLUSH PRIVILEGES;
Step 6: Test the MySql server if it is working by running sample sql queries
-CREATE DATABASE mysql_test;
-USE mysql_test;
-CREATE TABLE table1 (id INT, name VARCHAR(45));
-INSERT INTO table1 VALUES(1, 'Ayush'), (2, 'Heeral');
-SELECT * FROM table1;





