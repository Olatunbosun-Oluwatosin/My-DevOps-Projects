## Implementing Load Balancer with Nginx

Load balancing means distributing the work or tasks among several computers or servers so that no one workstation gets overloaded with too much work. This mechanism distribute incoming traffic around several capable virtual private servers. By apportioning the processing mechanism to several machines, redundancy is provided to the application -- ensuring fault tolerance and heightened stability.

### _Installing 2-EC2 instances_
![](./img/1.%20EC2-Instances(2-webservers).png)

The first step is to create the two(2) EC2 instances that will serve as webservers on AWS platform.

### _Security permission for the EC2 instance_
![](./img/2.%20Security-Permission.png)

Port 8000 was open on the security settings of the EC2 to allow our webservers communication.

### _Installation of apache web-server_
![](./img/3.%20webserver01-installed.png)
The command "sudo apt update -y &&  sudo apt install apache2 -y" is used to install the first apache2 web-server.


### _Installation of apache Webserver02_
![](./img/4.%20webserver02-installed.png)

The command "sudo apt update -y &&  sudo apt install apache2 -y" is used to install the second apache2 web-server and the command "sudo systemctl status apache2" was used to verify if our webserver is active & running.

### _Configure apache to serve content on port 8000_
![](./img/5.%20Edit-Port-Number.png)

Using text editor, the command "sudo vi /etc/apache2/ports.conf" was used to add port 8000 into the apache default configuration file.

### _Edited port 80 to 8000_
![](./img/6.%20Edit-port80-to-port8000.png)

With this command "sudo vi /etc/apache2/sites-available/000-default.conf", i was able to edit port 80 to port 8000.

### _Create a new index.html file_
![](./img/7.%20index-file-created.png)

with "sudo vi index.html", the index file was created.

### _Content of the new index.html file_
![](./img/8.%20Index-file-content.png)


### _New index.html file for webserver02_
![](./img/9.%20webserver02-index-file-content.png)

The creation of new index.html was done for both servers hence the repeat.

### _Default html file replaced_
![](./img/10.%20default-index-file-replaced.png)

This command "sudo cp -f ./index.html /var/www/html/index.html" was used to replaced the default html file with our new html file.

### _The page_ 
![](./img/11.%20the-page.png)
The webserver launch on port 8000 came back with the expected output.

### _Installation of nginx server_
![](./img/12.%20nginx-installed.png)
The nginx server was installed with this command "sudo apt update -y && sudo apt install nginx -y" and verified with this command "sudo systemctl status nginx".

### _Nginx configuration file_
![](./img/13.%20upstream-backend-config.png)
This command "sudo vi /etc/nginx/conf.d/loadbalancer.conf" was deployed to configure the load balancer with the ip addresses of the web servers.

### _Configuration file verified_
![](./img/14.%20config-file-okay.png)
"sudo nginx -t" was used to verify if the configuration was okay.

### _Default server configuration disabled_
![](./img/15.%20default-server-config-disable.png)
This command "sudo rm /etc/nginx/sites-enabled/default" was deployed to remove the default symbolic link from the _sites-enabled_ folder.

### _The final output of the load balancer task with nginx_
![](./img/16.%20final-output.png)

The task was completed succeefully with the expected output.

Thank you!!!