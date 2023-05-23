# HomeServer
Change history for multipurpose home setup

https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-22-04
https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-22-04

## Hardware
> * Processor: Intel i7-8700 6-core @3.2GHz
> * Memory: 32 GB - 2666MHz - DDR4
> * Unit: Dell Optiplex 7090

## Info & Installation
* Name: johnson-server
* User: john
* Install Ubuntu 20.04
* Reserved IP bound to MAC address on Network
* DHCP IP
* Install 3rd Party drivers
* Install OpenSSH
* Install Docker
* Install OS on m.2 NVMe

## Change History
  ## 4/26
  ### Basic configuration
  > * ufw allow OpenSSH
  > * ufw enable
  > * reboot

  ## 5/22
  ### mySQL
  > * apt install mysql-server
  > * mysql
  > * ALTER USER 'root'@'localhost' IDENTIFIED BY '#########'
  > * mysql_secure_secure installation
  > * mysql -u root -p
  > * CREATE USER 'john'@'localhost'
  
  ## 5/23
  ### Other LAMP Server Installations
  > * apt install apache2
  > * ufw allow in "apache"
  > * mv /var/www/html/index.html ./apacheTest.html
  > * apt install php libapache2-mod-php php-mysql
  
  ### Virtual Host Setup
  > * mkdir /var/www/johnjohnson.dev
  > * chown -R $USER:$USER /var/www/johnjohnson.dev
  > * nano /etc/apache2/sites-available/your_domain.conf
  > * a2ensite johnjohnson.dev
  > * a2dissite 000-default
  > * nano /var/www/johnjohnson.dev/index.html
   
