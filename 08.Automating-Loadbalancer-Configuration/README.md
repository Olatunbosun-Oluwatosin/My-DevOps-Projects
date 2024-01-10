## _Automating Loadbalancer Configuration with Shell Scripting

### _shell script to setup our Apache web server_
![](./img/1.%20web01-script.png)

The script has shown in the image was used to setup our EC2 web-servers.

### _status of web-server_
![](./img/2.%20web02-Apache2-active.png)

The image shown in our output shows the status of one of our web-servers. The output shows a webserver is active and running.

### _systemctl status apache2 to determine webserver status.
![](./img/3.%20web01-Apache2-active.png)

The command "sudo systemctl status apache2" was used to determine the status of our webserver as we can see in the output.

### _The script bash for setting up our webserver_
![](./img/4.%20web02-script-bash.png)

The script to setup the webserver is seen in the image displayed.

### _Installation of nginx and status of the webserver_
![](./img/5.%20nginx-status.png)

Using the script in our project assignment, we are able to install nginx successfully. This is active and running as seen in the image.

### _successful installation of the webserver and webpage outcome_
![](./img/6.%20EC2-webserver01.png)

The image shows the installation was done successfully as we can the outcome on the webpage.

### _successful installation of the second webserver_
![](./img/7.%20EC2-WebServer02.png)

The image shows the installation was done successfully as we can the outcome on the webpage with the respective IP address.

### _outcome of nginx load balancer_
![](./img/8.nginx-loadbalancer.png)

 The image above shows the successful deployment of nginx load balancer with shell scripting. A careful look of those pages shows what have been learnt so far using nginx webserver as a load balancer for the 2 EC2 web-servers. 