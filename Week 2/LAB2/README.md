# Lab 2: Manage Linux VMs with the AWS CLI

1. Create virtual machine
2. Connect to VM
3. Understand VM images
4. Understand VM sizes
5. VM power states
6. Management tasks

### Notes:

Quickstart: Create a Linux VM
* https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/

Using a custom Amazon machine image (AMI)
* https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.customenv.html

Quickstart: Restart VM via CLI
* https://docs.aws.amazon.com/cli/latest/reference/ec2/reboot-instances.html

Quickstart for AWS CloudShell
* https://docs.aws.amazon.com/cloudshell/latest/userguide/working-with-cloudshell.html





# CREATE  VIRTUAL MACHINE
The Aws virtual machine can be created basically using two procedures

The user inter-face

The command line. I employed both for the creation of VMs. I used the Cli to create a VM by using various commands for example;

--image-id ami-0abcdef1234567890(the image i choose)--instance-type t2.micro --key-name linuxaws I employed this as the command i used to create one of my VMs.

# CONNECT TO VIRTUAL MACHINE
I ssh into my Virtual machine using the ssh client. I copied the key on the interface and opened it on my local bash where the key is located and i was able to connect to my VM.

# UNDERSTAND VIRTUAL MACHINE IMAGES
VM images stands as configuration for the instance created. One has to choose an image or configuration before setting up a virtual machine depending on what is supposed to be used for. In an situation where there is need to add to the configuration or image there's a laid down procedure for that both on the user interface and command line. One can also choose from template images or create one from the scratch. The VM Images are in hundreds, there are lots of configurations to pick from depending on the work we want to carry out.

# UNDERSTAND VIRTUAL MACHINE SIZES
The virtual machine size(s) determines the amount of compute resource and the memory avaliable to our instance. We have various sizes to pick from either from the inception or creation of the instance or we can as well add to it even after the machine is running. One need to pick the size or sizes that would be enough for the workload to be done. If the instance is created to run a number of activites then we will definately need to pick a large size for the instance and vice versa . One can also create the particular size needed for the job.

# VIRTUAL MACHINE POWER STATE
The Virtual power state shows the current state of any virtually machine. it shows if it is running or not, maybe it's stopped or starting or maybe it has been terminated. we can view the power state of any instance by running some command on the cloud shell.

aws ec2 stop-instances --instance-ids (instance id) - This is to stop the instance
aws ec2 start-instances --instance-ids (instance id) - This is to start the instance
aws ec2 terminate-instances --instance-ids (instance id) - This is to terminate the instance.

# MANAGEMENT TASKS
We will have to manage our instance for various reasons, One being to help us lower cost or help from incuring some avoidable charges. For example when an instance is not in use we can stop for the main time instead of making it run which incur lots of charges for something not in use. We will want to run the management tasks such as deleting, starting, stopping, a VM. Using various command for various task.











































