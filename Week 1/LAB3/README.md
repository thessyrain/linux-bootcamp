# Lab 3: Manage Azure disks with the Azure CLI

1. Default Azure disks
2. Azure data disks
3. VM disk types
4. Launch Azure Cloud Shell
5. Create and attach disks
6. Prepare data disks
7. Take a disk snapshot

### Notes:

Quickstart: Manage Azure disks
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-disks

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart

# PRACTICE LAB 3. MANAGE AZURE DISK WITH THE AZURE CLI

# 1 DEFAULT AZURE DISKS

At the creation of any virtual machine two disks are automatically attached to the virtual machine, they are the operating system disk and temporary disk. I

#2. AZURE DATA DISK

 Azure data disk is a managed disk that's attached to a virtual machine to store application data, or other data you need to keep. Data disks are registered as SCSI drives and are labeled with a letter that you choose. Each data disk has a maximum capacity of 32,767 gibibytes (GiB). The size of the virtual machine determines how many data disks you can attach to it and the type of storage you can use to host the disks.
 
#3. VM DISKS TYPES

Azure managed disks currently offers four disk types, each intended to address a specific customer scenario
(a). Ultra disks
(b). Premium SSDs (Solid-state drives)
(c). Standard SSDs
(d). Standard HDDs( Hard disk drives)

#4. LAUNCH AZURE CLOUD SKILLS
 Launch Azure Cloud Shell Lunching an Azure Cloud Shell just involves a prompt clicking on it's icon on azure portal then it auomatically opens.

#5. CREATE AND ATTACH DISKS

The Add-AzVMDataDisk cmdlet adds a data disk to a virtual machine, you can add a data disk when you create a virtual machine, or you can add a data disk to an exisiting virtual machine.


#6. TAKE A DISK SNAPSHOT
To create a snapshot using the Azure portal, complete these steps.

In the Azure portal, select Create a resource.
(a). Search for and select Snapshot.
(b). In the Snapshot window, select Create. The Create snapshot window appears.
For Resource group, select an existing resource group or enter the name of a new one.
(c). Enter a Name, then select a Region and Snapshot type for the new snapshot. If you would like to store your snapshot in zone-resilient storage, you need to select a region that supports availability zones. For a list of supporting regions, see Azure regions with availability zones.
(d). For Source subscription, select the subscription that contains the managed disk to be backed up.
(e). For Source disk, select the managed disk to snapshot.
(f). For Storage type, select Standard HDD, unless you require zone-redundant storage or high-performance storage for your snapshot.
If needed, configure settings on the Encryption, Networking, and Tags tabs. Otherwise, default settings are used for your snapshot.
(g). Select Review + create.




























