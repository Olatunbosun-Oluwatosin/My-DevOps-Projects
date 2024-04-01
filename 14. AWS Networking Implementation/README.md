## _AWS Network Impelementation (VPC, Subnets, IG,NAT, Routing)_

### _creating vpc_
![](./img/1.%20vpc-created.png)
vpc stands for virtual private cloud on Amazon cloud where you can manage resources(like servers or databases). You control who and what goes in and out.AWS cloud platform has a default VPC that can be use if you decided not to create one, all that is needed is for you to edit it for your specific needs.
As seen in the image, a vpc was created tag "test-VPC".

### _creating subnets_
![](./img/2.%20subnet-created.png)
subnets are like smaller segments within a VPC that help you organize and manage your resources. subnets are created to organize and manage the network effectively.
four(4) different subnets were created according to the manual/guide. two(2) as public while the other two(2) as private subnets.

### _creating internet gateway_
![](./img/3.igw-created.png)
IG is a service on AWS that allows for inbound and outbound traffics to the internet from a public subnet. For a subnet to be public, an Internet gateway must be created and attached to the VPC and subnet with a route table configured.

### _internet gateway attached to VPC_
![](./img/4.%20IGW-attached-to-VPC.png)
As seen in the image, the IG created was attached to the VPC _"test-VPC"_.

### _creating route table_
![](./img/5.%20route-table-created.png)
After creating the IGW, the route table is what gives direction to our resources. Guiding the resources on how to get in and out of our VPC. The route table was created with a name tag "test-vpc-public-rtb", route table edited and default route was added to the IGW(internet Gateway).

### _default route add_
![](./img/6.default-route-added.png)
Route table was edited and the default route was added. This will allow inbound and outbound traffic between the resources within the public subnet and the internet.

### _public subnet attached to route table_
![](./img/7.publi-subnet-attached-routetable.png)
The public subnets as expected was attached to route table for free flow of communication between the resources in the subnets and the internet.

### _creating private route table_
![](./img/8.%20private-rtb-created.png)
A route table with a target to NAT gateway is a private route table.

### _creating NAT gateway_
![](./img/9.%20nat-gw-created.png)
In AWS virtual private cloud(VPC), private subnets are secluded areas where you can place resources that should not be directly exposed to the internet. But when this resources need access to the internet for updates or downloads, then there is a need for NAT gateway. So the NAT gateway is linked with the private subnets to connect to outside services.

### _route table edited_
![](./img/10.rtb-edited-natGW.png)
The route table was created for the private-subnet. This is also edited to capture the newly created NAT-gateway.

### _route table update_
![](./img/11.updated-rtb.png)

A route table was created for both the private and public subnets. Two subnets was attached to the route table created for public subnet while a subnet was attached the route table created for the private subnet. This can be noticed in the image.

I have learnt how to create a VPC and all needed resources associated with it. Thank you
