# Lab 4: Manage Packages and Services on a Linux VM (Azure or AWS)

1. Create a Linux VM
2. Install the Apache Web Server
3. Start the service status via command line
4. Investigate the service status via command line
5. Stop the service 

Challenge: Create a boostrapping script that will install and start this service on new EC2 VMs

### Notes:

Install and Configure Apache (Ubuntu)
* https://ubuntu.com/tutorials/install-and-configure-apache#1-overview

How to install Apache on RHEL 8 / CentOS 8 Linux
* https://linuxconfig.org/installing-apache-on-linux-redhat-8

How to use cloud-init to customize a Linux virtual machine in Azure on first boot
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-automate-vm-deployment

Create bootstrap actions to install additional software
* https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-bootstrap.html


 Creating a VM.

 To create a Virtual Machine on Microsoft Azure the following command line was engaged.

az vm create \

  --resource-group myResourceGroup \

  --name myVM \

  --image UbuntuLTS \

  --admin-username azureuser \

  --generate-ssh-keys

# Installing the Apache Webserver.

The Apache web server can be installed using a remote SSH connection

I ran the following command line to install Apache

sudo apt-get update

sudo apt-get install apache2

 

Once the commands line was done, I pasted my public IP address into the internet browser to view my VM instance.

# Starting the Azure VM Command:

To start the stopped Azure VM using Azure CLI, I used the az vm start command line.

 az vm start -n vmname -g RGname --verbose

# Investigate the service status usng command line.

To investigate the service status. This tells us the state of all our VMs / resources, which have been created.

The following command can be employed to get the service status

get-azvm –status

 
# To stop the service

I   stopped your virtual machine using the Azure cloud shell PowerShell command line. To stop the service i ran the command line :

az vm stop -n cloudskillsserver -g cloudskillsRG --verbose

 
































