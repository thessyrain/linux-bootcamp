# Lab 2: Install a LAMP stack on an Azure Linux VM

1. Prepare the LAMP server
2. Test your Lamp server
3. Secure the database server
4. (Optional) Install phpMyAdmin

### Notes:

Tutorial: Install a LAMP web server on the Amazon Linux AMI
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-LAMP.html

Tutorial: Host a WordPress blog on Amazon Linux 2
* https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/hosting-wordpress.html

Sample Gist
* https://gist.github.com/mikepfeiffer/c079608703e604224e58a3d40d0fa043#file-lamp-linux-aws-sh







# Prepare the Laompstack server

LAMP WEBSERVER/LAMP STACK- LAMP is an acronym for Linux, Apache, MySQL, and PHP.

To install a LAMP WEB SERVER ON THE Amazon Linux AMI, the following procedures was executed.  I was able to install the LAMP stack using the followings commands on Amazon Linux Ami. To install the LAMP webserver it is necessary to have a running instance and one must also have configured security group to allow SSH (Port 22,) HTTP(port 80), and HTTPS (Port 443) connections.

I was able to run this following command line to install Apache, Mysql and PHP (LAMPSTACK)

sudo yum install -y httpd24 php72 mysql57-server php72-mysqlnd
This command installed the various apps simultaneously.

sudo service httpd start - ( This is to start Apache web server after installation)
sudo chkconfig httpd on - ( This is to enable Apache web server to survive a reboot).
# Test your Lamp server

I was able to test my various installed apps by using my public Ip.

For my PHP, to create a PHP file i ran this command as directed

echo "" > /var/www/html/phpinfo.php
I encountered an error "permission denied" then  i ran  the following command which gave a positive output

sudo sh -c 'echo "" > /var/www/html/info.php'
After this i was able to view my PHP page  with my IP address (18.188.121.206./info.php/) on the internet browser, while Apache was the Index html file, PHP was the other page

# Secure the database server

To secure my database which is MySql i was able to run the following command to start and secure Mysql. The default installation of the MySQL server has features that are great for testing and development. The mysql_secure_installation command walks you through the process of setting a root password and removing the insecure features from your installation.

sudo service mysqld start - (This is to start Mysql database)
sudo mysql_secure_installation - (This is to secure Mysql, I was able setting my password, disable the remote root login. I was remove the test database).
# (Optional) Install phpMyAdmin

phpMyAdmin is a web-based database management tool  that you can use to view and edit the MySQL  database on your EC2 instance. The following steps below was executed to install and configure phpMyAdmin on my Amazon Linux instance

·         sudo yum install php72-mbstring.x86_64 –y (to  install the required dependencies )

·         sudo service httpd restart ( to start Apache)   (ok)

·         cd /var/www/html

 but I encountered errors trying to run the next commands to install the  PhpMyAdmin, I will further troubleshoot to solve the problem.

 





































