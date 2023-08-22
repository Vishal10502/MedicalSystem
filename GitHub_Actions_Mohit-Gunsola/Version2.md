# Task 2(V2): AWS cli(Create Bucket , copy .txt to S3 bucket)
In this task we have created EC2 instance ,also created a s3 bucket and upload .txt file to s3 bukcet. All the actions are performed using AWS cli.<br>
<br>
## Creating EC2 instance: <br>

**Step 1**: After,login into your AWS account click “services” <br>
                                                                         
**Step 2**: Into services click on "Ec2" <br>

**Step 3**: To create an Instance we have to make "KEY PAIR " <br>

1. Under Resources click-on Key pairs <br>
2. Create a new keypair by clicking on "create key pair " <br>
3. After writing keypair name, select key pair type to RSA or ED25519 accordingly <br>
4.  Finally you will get keypair after clicking-on create keypair <br>
                                          
**Step 4**: Create a security group after creating keypair <br>

   1. Under the Resources click-on Security Groups <br>
   2.  We already have an existing security group ie: the default security group but for our requirements we well create new one <br>
   3. So now Create a new security group by clicking on "create security group " <br>
   4. Fill in the security group name , description , vpc info and then add inbound rules to it <br>
   5. Select in-bound rules and add a new rule with type as "All Traffic" and source as "IPV4" <br>
   6. Click-on create security group <br>
   
**Step 5**: Now for creating an instance <br>

   1. Click on instance under the resources section <br>
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

   
## AWS cli installation: <br>

1. Launch the instance.<br>
2. Connect instance to ubuntu server. <br>

```
ssh -i keyname.pem ubuntu@publicip

```
  
3. Update the repository .  <br>

```
sudo apt update

```

4. Install aws cli into ubuntu server. <br>

```
sudo apt install awscli -y

```

5. Check whether cli is installed or not. <br>

```
aws --version

```

6. Configure the aws cli. <br>

```
aws configure

```

   6.1. Enter the following details accordingly: <br>
     a) AWS Access Key ID [IAM user's Access key] <br>
     b) AWS Secret Access Key [IAM user's secret key] <br>
     c) Default region name [Aws region] <br>
     d) Default output format [JSON format is fine] <br>

## Create a s3 bucket using cli: <br>

1. Create a bucket with any name.<br>

``` 
create-bucket --bucket "bucketname" --region us-east-1

 ```

2. list all the aws bucket.<br>

```
aws s3 ls

```

## Copy .txt file to s3 bukcet using cli: <br>

1. Create a file in ubuntu server.<br>

``` 
touch "filename.txt"

 ```

2. Copy the created file to the aws s3 bucket.<br>

``` 
aws s3 cp "filename.txt" s3://"bucketname"

 ``` 







