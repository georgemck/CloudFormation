# CloudFormation

Create a WordPress website using EC2 with a few configurations.


This CloudFormation template installs an older version of PHP which must be upgraded for WordPress to install. The directions follow.


#Upgrading to PHP 7.2 on Amazon Linux

#check current version of PHP
php -v

#stop APACHE and PHP services
sudo service httpd stop

#uninstall APACHE and PHP
sudo yum remove httpd* php*

#Get latest updates
sudo yum update -y

#install PHP 7.2
sudo yum install php72

#install MySQL driver for PHP 7.2
sudo yum install php72-mysqlnd
 
#Start APACHE web server
sudo service httpd start

#cleanup
sudo yum clean all

