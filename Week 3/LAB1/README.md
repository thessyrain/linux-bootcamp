# Lab 1: Install a LAMP stack on an Azure Linux VM

1. Create a resource group
2. Create a virtual machine
3. Open port 80 for web traffic
4. SSH into your VM
5. Install Apache, MySQL, and PHP
6. Install WordPress

### Notes:

Tutorial: Install a LAMP stack on an Azure Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-lamp-stack

Sample Gist
* https://gist.github.com/mikepfeiffer/96d659042f0575a617648a33c92b8f4a

Build and run a web application with the MEAN stack on an Azure Linux virtual machine
* https://docs.microsoft.com/en-us/learn/modules/build-a-web-app-with-mean-on-a-linux-vm/

MEAN Stack App
* https://github.com/MicrosoftDocs/mslearn-build-a-web-app-with-mean-on-a-linux-vm




# linux-bootcamp Schull.io 

# PRACTICE LAB I: CREATE A LINUX VIRTUAL MACHINE WITH THE AZURE CLI
  1. Lanuch Microsoft Azure Cloud Shell (Free Subcription)
  2. Create a resource (UBUNTU SERVER )
  3. I deployed with Ubuntu Server 20.04 LTS, this is the leading Linux
     in public cloud with > 50% of LINUX WORKLOADS.
  4. Created a Virtual Machine with the IP address of 20.120. 36. 68 with
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
      


# SSH IN YOUR VM

With the public key deployed on my Azure VM, and the private key on your local system, SSH into your VM using the IP address. In the following command, 

a. I opened the client of my choice (Kali Linux terminal)
b. I ensured i had read-only access to the private key  (chmod 400 thessyrain.pem)
c. I provided a path to my SSH private key file 
d. Then i ran this command below to connect SSH to my VM
ssh -i < /home/thessyrain/Downloads> thessyrain @ 20.120.36.68



# INSTALL APACHE, MYSQL, PHP and Wordpress

i ran the following command on my bash terminal to install APACHE, Mysql and PHP


# Install LAMP
sudo apt update && sudo apt install lamp-server^ -y

# Secure MySQL and set root pwd
sudo mysql_secure_installation

# Validate login to MySQL
sudo mysql -u root -p

# Create PHP Info page
sudo sh -c 'echo "<?php phpinfo(); ?>" > /var/www/html/info.php'

# Install WordPress
sudo apt install wordpress -y

# Create WordPress DB Script
sudo nano wordpress.sql

# CREATE DATABASE wordpress;
# GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,ALTER
# ON wordpress.*
# TO wordpress@localhost
# IDENTIFIED BY 'P@ssw0rd2021';

# Configure DB
cat wordpress.sql | sudo mysql --defaults-extra-file=/etc/mysql/debian.cnf

# Remove WordPress DB Script
sudo rm wordpress.sql

# Prep config-default.php file
sudo nano /etc/wordpress/config-localhost.php

# <?php
# define('DB_NAME', 'wordpress');
# define('DB_USER', 'wordpress');
# define('DB_PASSWORD', 'P@ssw0rd2021');
# define('DB_HOST', 'localhost');
# define('WP_CONTENT_DIR', '/usr/share/wordpress/wp-content');
# ?>

# Move the WordPress installation to the web server document root
sudo ln -s /usr/share/wordpress /var/www/html/wordpress
sudo mv /etc/wordpress/config-localhost.php /etc/wordpress/config-default.php



















































































