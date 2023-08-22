# Task 2(V2): AWS cli(Create Bucket , copy .txt to S3 bucket)
In this task we have created EC2 instance ,also created a s3 bucket and upload .txt file to s3 bukcet. All the actions are performed using AWS cli.<br>
<br>
## AWS cli installation: <br>
  <br>
1. Create an EC2 instance and launch the instance.<br>
2. Connect instance to ubuntu server. ``` ssh -i keyname.pem ubuntu@publicip ``` <br>
3. Update the repository . ``` sudo apt update ``` <br>
4. Install aws cli into ubuntu server. ``` sudo apt install awscli -y ``` <br>
5. Check whether cli is installed or not. ``` aws --version ```
6. Configure the aws cli. ``` aws configure ```
   6.1. Enter the following details accordingly: <br>
     a) AWS Access Key ID [IAM user's Access key] <br>
     b) AWS Secret Access Key [IAM user's secret key] <br>
     c) Default region name [Aws region] <br>
     d) Default output format [JSON format is fine] <br>







