# Version1 #
## DATABASE INFRASTRUCTURE PREPARATION : 
### Step-By-Step 
### Process for creating an EC2 instance :
**CREATING AN EC2 INSTANCE** <br>


**Step 1**: First, login into your AWS account and click on “services” <br
                                                                         
**Step 2**: From the drop-down menu of options, tap on “EC2 " <br>

**Step 3**: For Creating an Instance we first need to create a "KEY PAIR " <br>

1. Under Resources click-on Key pairs <br>
2. Now Create a new keypair by clicking on "create key pair " at the top right of the section <br>
3. Now enter the key pair name , select key pair type to RSA or ED25519 respectively <br>
4. Now selectthe private key type as .pem or .ppk according to your working enviornment <br>
5. Now Finally click-on create keypair <br
                                          
**Step 4**: After successfully creating a keypair we now need to create a security group <br>

   1. Under the Resources click-on Security Groups <br>
   2.  We already have an existing security group ie: the default security group but for our requirements we well create new one
   3. So now Create a new security group by clicking on "create security group " <br>
   4. Fill in the security group name , description , vpc info and then add inbound rules to it <br>
   5. Select in-bound rules and add a new rule with type as "All Traffic" and source as "IPV4" <br>
   6. Click-on create security group <br>
   
**Step 5**: Now for creating an instance <br>

   1. click on instance under the resources section <br>
   2. Click on launch instance ,  after clicking on it you will be redirected to a launch page where we can create instance
   3. Create a name for the instance <br>
   4. Select AMI – Required operating system from the available. <br>
   5. I am selecting Ubuntu AMI as we need to create Ubuntu instance. By default, it selects a free tier storage. <br>
   6. Select instance type <br>
       By default, instance type is “t2.micro” which is free tier eligible service. <br>
       Do not select any other which leads to billing amount. <br>
   7. Now Select the key pair which me made earlier . <br>
   8. In the network setting Select to existing security group and under that 
      select the Security group which we had prepared earlier . <br>
   9. Click on launch the instance <br>
   
**Step 6**: After Launching the instance right click-on the instance and select the option connect <br>

**Step 7**: It automatically takes us to "Connect to Instance" page <br>

**Step 8**: Now here select "Connect to EC2 instance connect" <br>

**Step 9**: Click on Connect <br>

**Step 10**: We get re-directed to a new page in which we now have the terminal <br>


# Version2
## Installing & Connecting MySql Server and then further Creating a Database 
### COMMANDS USED TO HOST MYSQL SERVER ON AWS EC2 INSTANCE :

 
**Step 1**: Update the system
```
sudo apt update
```
**Step 2**: Install MySql
```
sudo apt install mysql-server
```
**Step 3**: Check the Status of MySql (Active or Inactive)
```
sudo systemctl status mysql
```
**Step 4**: Login to MySql as a root
```
sudo mysql
```
**Step 5**: Update the password for the MySql Server
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'place-your-password-here';
```
```
FLUSH PRIVILEGES;
```
**Step 6**: Test the MySql server if it is working by running sample sql queries
```
CREATE DATABASE mysql_test;
USE mysql_test;
CREATE TABLE table1 (id INT, name VARCHAR(45));
INSERT INTO table1 VALUES(1, 'Ayush'), (2, 'Heeral');
SELECT * FROM table1;
```





