# Lab 1: Create a Linux virtual machine with the AWS CLI

1. Launch AWS Cloud Shell
3. Create virtual machine
4. Open port 80 for web traffic
5. Connect to virtual machine
6. Install web server
7. View the web server in action

### Notes:
1 Launch AWS Cloud Shell 
 I visited the the Amazon website https://us-east-2.console.aws.amazon.com/
 there is an icon at the top right immediately after the Search bar you click it to Lunch your AWS Cloud shell.

 3 Create Virtual Machine 
  Using the Graghical Interface 
    you will clicks on luuch instance the you follow the steps which are 
Step 1 Choose AMI. AMI which means Amazon Machine Image.
Step 2 Choose your instance Type Tag
Step 3 Configure Instance 
Step 4 Add Storage 
Step 5 Add tags 
Step 6 Configure Security Groups
Step 7 Review your insatnce.

While using the Cloud Shell AWS CLI

For Guidlines yo can check out aws cli command reference for guid lines on how to USE AWS CLI 
through the guidelines you can create or lunch a an instance or Virtual Machine. Then you search for EC2 you click and go to run-instances then you click on the examples.

By using this steps of command Lines
 "aws ec2 run-instances --image-id ami-0abcdef1234567890 --instance-type t2.micro --key-name MyKeyPair"

5 Connect to a Virtual Machine 
 connecting to your Virtual Machine.
 I used from My local Terminal to ssh into my instance. i made sure i was in that same directory the pem file was downloaded then i will run the following commands 

 "chmod 400 Martins-KeyAWS.pem"
  "ssh -i "Martins-KeyAWS.pem" ec2-user@ec2-3-15-232-87.us-east-2.compute.amazonaws.com"

6 Install a webserver
  



Quickstart: Create a Linux VM
* https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/

Quickstart for AWS CloudShell
* https://docs.aws.amazon.com/cloudshell/latest/userguide/working-with-cloudshell.html