
## _Implementing Wordpress website with LVM Storage Management on AWS EC2_

This is a step by step introduction to implementing wordpress on AWS EC2 using RedHat linux as the operating system. It's a guide through the process of creating logical volumes, managing disk space and dynamically resizing volumes to accomodate changing storage requirements. As part of the course, one will gain proficiency in installing and configuring WordPress.

### _creating physical volume_
![](./img/1.%20pvcreate.png)

After setting up my server and adding the 3-storage volume according to the manual. The command "pvcreate" was deployed to create physical volumes.

### _creation of volume group_
![](./img/2.%20vgcreate.png)

The command "sudo vgcreate webdata-vg /dev/nvme1n1 /dev/nvme2n1 /dev/nvme3n1" was used to create the volume group.

### _logical volume formatted_
![](./img/3.%20logical%20volume%20formatted.png)

This process was used to format the volumes and the command "sudo lvcreate" was used.

## _list of volumes_
![](./img/4.%20lsblk.png)
 
 The command "lsblk" was used to list all the volumes.

 ## _block volume ID_
 ![](./img/5%20blkid.png)

 The command "blkid" was used to display the ID of the block volume.

 ## _disk information_
 ![](./img/6.%20df%20-h.png)

 The command "df -h" display information about the disk space usage of all mounted file systems in a human readable format.

 ## _creating database user_
 ![](./img/7.%20creating-database-user.png)
 After successful installation of MySQL database, what follows is the creation of database user.
 This command "create user 'myuser'@'172.31.41.124' identified by 'mypass';" was used for creation of database user and the ip address above is the webserver.

 ## _successful connection with the database_
 ![](./img/8.%20myuser-to-database.png)
 The image above shows how the user "myuser" was successfully connected to the database using the command "mysql -u myuser -p -h 172.31.34.250 in which the ip address is for the database server.

 ## _WordPress config file edited_
 ![](./img/9.%20wp-config.png)
 with "sudo vi wp-config.php", i'm able to edit the Wordpress configuration file to capture the "database-name", "DB-username", "DB-password" and "DB-host".

 ## _security rule_
 ![](./img/10.%20allow-security-rule.png)
 If i must be able to reach my wordpress website via the browser, then i must allow port 3306 in my security policy settings. This is shown in the above image.

 ## _WordPress page_
 ![](./img/11.%20wordpress-setup-page.png)
 After following the whole process, i was able to access the wordpress website and setup the page as seen above.

 ## _WordPress successfully installed
 ![](./img/12.%20wordpress-successful-installation.png)

## _WordPress dashboard
![](./img/13.%20wordpress-dashboard.png)




Thank you!!!