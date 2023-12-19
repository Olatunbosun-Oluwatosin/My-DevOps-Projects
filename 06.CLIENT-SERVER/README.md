## Client-Server Architecture with MySQL

Client-Server refers to an architecture in which two or more computers are connected together over a network to send and receive requests between one another.
In their communication, each machine has its own role: the machine sending requests is usually referred as "Client" and the machine responding (serving) is called "Server".

### Curl Command

![](./img/1.%20curl-command.png)

### EC2 Instances

![](./img/2.%20two-EC2-instances.png)
At this stage, EC2 instances were created for the task. One for the MySQL-Client(Public IP:16.16.213.240) while the second is MySQL-Server(Public IP:13.49.222.108)

### Installation of MySQL-Server

![](./img/3.%20Mysql-server-installed.png)

MySQL-Server was installed successfully using this command " sudo apt install mysql-server" and to check the status of the installation, the command "sudo mysql" was used.

### Installation of MySQL-Client

![](./img/4.%20mysql-client-installed.png)

MySQL-Client installation was completed successfully using this command,"apt install mysql-client -y".

### Security Permission

![](./img/5.%20security-permission.png)

This task is performed at the security setting on AWS platform to allow the IP address(Public IP:16.16.213.240) of MySQL client on port 3306 to be able to access MySQL-Server. In my case i used the public address of the client as against the private address specified in the assignment.

### Configure MySQL-Server to allow Connection from Remote host.

![](./img/6.%20Vi%20editor.png)

With this command, "sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf" I was able to edit the bind-address: 127.0.0.1 and replaced with 0.0.0.0.

### Output of MySQL-Server

![](./img/7.%20mysql-server.png)

This shows the outcome of what has been done so far and i was able to call out the databases. Which signified that i did the right thing.

### Output of MySQL-Client

![](./img/8.%20mysql-client.png)

With this command, "mysql -u newuser2 -h 13.49.222.108 -p", i was able to connect to MySQL-Server using the public ip address.

Before the above command, there was an entry on MySQL-Server.

CREATE USER 'newuser2'@'16.16.213.240' IDENTIFIED BY 'password2';
GRANT ALL PRIVILEGES ON * . * TO 'newuser2'@'16.16.213.240';

The above entry created the newuser2 on MySQL-Server and grant all privileges to the user.

Thank you!!!

