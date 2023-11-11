## LAMP STACK PROJECT

EC2 has been created since my first class with private key downloaded on my local machine to connect to my ec2 instance using termius or putty.

### Connection to EC2

![](./img/1.%20Connect_to_ec2.png)

### Sudo apt update
![](./img/2.%20sudo-apt-update.png)

### Apache2 web server installation
The command "sudo apt install apache2" is used to install apache web server on the linux machine.
![](./img/3.%20Apache2-server.png)

### Status of Apache web server
To check or know whether your server is up and running, you run this command "sudo systemctl status apache2"
![](./img/4.%20systemctl-status.png)

### Allow port 80
For my apache server to be reachable on the internet, i must therefore create an allow rule in the security framework on aws.
![](./img/5.%20port-80-allow.png)

### curl http://localhost:80

![](./img/6.%20curl-localhost.png)

### curl http://127.0.0.1:80

![](./img/7.curl-127.0.0.1.png)

### Apache HTTP server is now reachable over the internet.
This is achieveable using the public ip address from aws platform.

![](./img/8.%20public-ip.png)

### Mysql installation
mysql server is install using the command "sudo apt install mysql-server"

![](./img/9.%20install-mysql-server.png)

### MYSQL Console
To log in to the mysql console/monitor, the command "sudo mysql" is used.
![](./img/10.%20mysql-console.png)

### mysql native password
To define a password for mysql database server, the command is on the image below.
![](./img/11.%20mysql-native-password.png)

### Interactive script
To start interactive script, i ran the command "sudo mysql_secure_installation

![](./img/12.%20mysql_secure_installation.png)

### To login to mysql
The command "sudo mysql -p" is used to login to mysql requesting a password.

![](./img/13.%20login-to-mysql.png)

### PHP Installation
![](./img/14.%20php-installation.png)

### To check the version of PHP package
To check the version of the php installation, the command is "php -v"

![](./img/15.%20php%20-v.png)

### PHP site

![](./img/16.%20php%20-site.png)

### Apache Virtualhost
![](./img/17.%20apache-virtualhost-commands.png)

### Apache Virtualhost page
![](./img/18.%20apache-virtualhost-output.png)

