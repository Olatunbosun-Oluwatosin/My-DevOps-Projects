## LEMP Project Implementation

### sudo apt update

![](./img/1.%20sudo%20apt%20update.png)

### Installing nginx web server
The command 'sudo apt install nginx' will install our web server.
![](./img/2.%20apt%20install%20nginx.png)

### To check the status of nginx server
To verify if nginx was successfully installed and running as a service in Ubuntu, you run 'sudo systemctl status nginx' command.
![](./img/3.%20systemctl%20status%20nginx.png)

### To reach the nginx web server on the internet
This can be achieve by going to  http://16.170.221.57:80

![](./img/4.%20nginx%20webserver.png)

### To install mysql server
For mysql server to be installed, you run 'sudo apt install mysql-server' command.

![](./img/5.%20install%20mysql-server.png)

### To define password for mysql server

![](./img/6.%20to%20define%20password.png)

### This prompt you for password
'sudo mysql -p' command will prompt you for password to gain access to mysql console

![](./img/7.%20mysql%20-p.png)

### PHP Installation
PHP is installed to process code and generate dynamic content for the web server

![](./img/8.%20php%20component%20install.png)

### To create root directory
'sudo mkdir /var/www/projectLEMP' is the command to create the root directory

![](./img/9.%20root%20web%20directory.png)

### To test nginx & Configuration
The command 'sudo nginx -t' is used for the test.
![](./img/10.%20nginx%20config%20test.png)

### Nginx site is working

![](./img/11.%20nginx%20website.png)

### Testing PHP with Nginx
The site was reachable using this -- http://16.170.221.57/info.php

![](./img/12.%20Testing%20php%20with%20Nginx.png)

### Show Databases
After creating the example_database and example_user. The command 'SHOW DATABASES' in mysql display the outcome.

![](./img/13.%20show%20databases.png)

### Creating todo_list

![](./img/14.%20todo_list.png)

### Todo_list webpage
The webpage can be reachable via http://16.170.221.57/todo_list.php 

![](./img/15.%20todo_list%20webpage.png)

