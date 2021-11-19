# Lab 2: Manage Linux VMs with the Azure CLI

1. Create resource group
2. Create virtual machine
3. Connect to VM
4. Understand VM images
5. Understand VM sizes
6. VM power states
7. Management tasks

### Notes:

Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart


# PRACTICE LAB 2. CREATE A LINUX VIRTUAL MACHINE WITH THE AZURE CLI
  1. Lanuch Microsoft Azure Cloud Shell (Free Subcription)
  2. Create a resource (UBUNTU SERVER )
  3. I deployed with Ubuntu Server 20.04 LTS, this is the leading Linux
     in public cloud with > 50% of LINUX WORKLOADS.
  4. Created a Virtual Machine with the IP address of 20.121.192.135 with
     the following steps;
# PROJECT DETAILS
     a. Created a resource group with the name THESSYRAIN_NG
# INSTANCE DETAILS
     b. Filled in a name for the VM  as Webserver1
     c. There are different regions available, i stuck with  (US) East US
     d. I chose Ubuntu Server 20.04 LTS- GEN 1 for my image
     e. To select the Size of my VM I chose DS1_v2 General purpose EAST  
        REGION with CPU 1, 3.5GB RAM, Data disk 4 and Max IOPS 3200 and
        Temporary Storage of 7 GiB
# ADMINISTRATOR ACCOUNT
Authentication type:  f. I selected Password, I couldnt SSH into my Kali terminal, so i download putty gen to access my webserver
      g. Password: I created a Username and Password to help access the ppk with the IP address created for the VM
# PUBLIC INBOUND PORTS
      h. Allowed for selected for port, HTTP (80) and SSH (22)
# INSTALL WEB SERVER
       a. on my kali terminal i ran the command line sudo apt-get update
       b. sudo apt-get install apache2
       c. systemctl status apache2   it reads active running
       d. to test i copied the IP address and google searched it.


# UNDERSTAND VM IMAGES

VM image is a collection of metadata and pointers to a set of VHDs (one VHD per disk) stored as page blobs in Azure Storage.  A VM Image containing a single VHD with a generalized  operating system is  essentially the OS image we are familiar with today. There are two types of VM Image -generalized and specialized - each serving their own purpose.
A generalized VM Image contains an OS disk, which as the name suggests, has been generalized ( for windows, OS Image today are generalized. This type of VM Image is meant to be used as a model to quickly stamp out similar virtual machines.

A Specialized VM Image contain an OS disk, which is already provisioned. It is similar to a disk today in that  it is "ready-to-use"  A specialized VM Image is meant to be used as a snapshot to deploy a VM to a good known point in time. 



# UNDERSTAND VM SIZES
TYPES                            SIZES                                DESCRIPTION
General Purpose               B, Dsv3, Dv3, Dasv4, Dav4              High CPU-to-memory ratio, ideal for 									     testing and development, small to
				    				     medium traffic web servers
                              DSV2  DV2, Av2, DC, DCv2, Dv4
                              Dsv5, Ddv5 Ddsv4 Dadsv5
                              
                              
                              
Compute optimized           F, Fs, Fsv2, FX			     High CPU-to-memory ratio. Good for
							             medium traffic web servers, network
							             appliances, batch processes and
							             application servers.
							           
# VM Power states
There are seven power states that a VM can exist
Starting: Indicates that the VM is being started
Running:  Indicates that the VM is running
Stopped:  Indicates that the VM is stopped
Deallocating : Indicates that the VM is being deallocated
Deallocated: Indicates that the VM is completed removed from the hypervisor






























