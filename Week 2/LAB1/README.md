# Lab 1: Create a Linux virtual machine with the AWS CLI

1. Launch AWS Cloud Shell
2. Create virtual machine
3. Open port 80 for web traffic
4. Connect to virtual machine
5. Install web server
6. View the web server in action

### Notes:

Quickstart: Create a Linux VM
* https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/

Quickstart for AWS CloudShell
* https://docs.aws.amazon.com/cloudshell/latest/userguide/working-with-cloudshell.html




# LAUNCH AWS CLOUD SHELL

Step 1: To get started with the AWS Cloud Shell, I signed into the AWS Management console and chose AWS CLOUDSHELL from the home page with the use of the cloud command shell pwsd-for powershell, bash- for bash.


# CREATE A VIRTUAL MACHINE

In Amazon Web Services, Virtual Machines can be created basically  by using the following procedures

1. The user inter-face  2. The command line. 

I employed both for the creation of my VMs. I used the Cli to create a VM by using the cloud shell commands for example; Aws ec2 run instance --image-id ami-0abcdef1234567890(the image i choose)--instance-type t2.micro --key-name Linuxaws.pem

# OPEN PORT 80 FOR WEB TRAFFIC

Port 80 is default for web traffic, Virtual Machine is created to allows web server then port 80 needs to be opened for traffic. I opened port 80 on my already craeted using the interface. clicked on security group, then to the inbound rule, I opened a new inbound rule to allow HTTP and port 80 was opened.

# CONNECT TO VIRTUAL MACHINE

I ssh into my Virtual machine using the ssh client. I copied the key on the interface and opened it on my local bash where the key is located and i was able to connect to my VM.

# INSTALL WEB SERVER

I was able to install a web server (apache2)   by using the following command lines;

yum update -y
sudo yum install -y httpd (apache2)
sudo systemctl start httpd
sudo systemctl enable httpd

# VIEW THE WEB SERVER IN ACTION

I copied my Ip address pasted it on google and i was able to see my installed apache2.
















