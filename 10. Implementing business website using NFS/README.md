## Implementing Business Website using NFS

### _formating disk with xfs_
![](./img/1.%20xfs%20filesystem.png)
The disk was formatted using the command "mkfs.xfs -f /dev/nvme1n1" where nvme1n1/nvme2n1/nvme3n1 are the disk identity.

### _physical volume, volume group & logical volume created_
![](./img/2.%20pv-vg-lv%20create.png)
physical volume, volume group and logical volumes was created as seen in the image. 

### _export filesystem_
![](./img/3.%20exportfs-arv.png)
export filesystem was created for 'opt, logs & apps'. with the command "exportfs -arv', all directories specified in /ext/exports are re-exported.

### _nfs-client setup_
![](./img/4.%20nfs-client-setup.png)
 This has the detailed commands with which nfs client was setup.

 ### _tooling_
 ![](./img/5.%20tooling.png)
This explained or detailed the creation of the tooling database, setup, forking repo as well as cloning the repo as specified in the manual/guide.

### _SE Linux disabled_
![](./img/6.%20selinux-disabled.png)

This is achieved by opening the config file with "sudo vi /etc/sysconfig/selinux" and set SELINUX=disabled, then restart httpd.

### _web login page_
![](./img/7.%20webpage-login.png)

### _Welcome page_
![](./img/8.%20webpage.png)


Thank you