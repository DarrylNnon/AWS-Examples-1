# A overview of a vpc

A virtual private cloud is logical isolated virtual nettwork.

# Core vpc components

![alt text](image.png)

 # Key features of vpc

![alt text](image-1.png)

## Default vpc
Aws has a default vpc in every region for me to deploy immediatly instances
```sh
aws ec2 create-default-vpc --region ca-central-1
```
## Deleting a vpc
To delete a vpc, i have to delete multiple vpc resources before being able to delete the vpc.
![image](https://github.com/user-attachments/assets/a4f3883a-31a2-481c-842c-3cac7a9e3cc4)

## Default Route / Catch-All-Route
The default route or catch-all-route represents all possible IP addresses.Thimk of this route as giving access from anywhere or to the internet without restriction

![image](https://github.com/user-attachments/assets/45b32431-af47-44de-a266-f21b2d095eeb)

## Shared VPCs
![image](https://github.com/user-attachments/assets/86428e6c-b5a6-4c47-b518-8dfefb9bb1ca)

## Stateful vs Stateless in AWS VPC

![image](https://github.com/user-attachments/assets/08f79382-96f6-40ba-a4f4-8f6efb19d36a)

## Routes Tables

A route table specifies how packets are forwarded between the subnets within your VPC, the internet, and your VPN connection.

![image](https://github.com/user-attachments/assets/35d572af-57a7-4024-abb1-05de0badc5d1)

- route tables
![image](https://github.com/user-attachments/assets/005ae8da-c8c6-4812-a1e9-20a04993891d)
- target
  local - the default local route that lets associate subnetes within the vpc route to the other route.

![image](https://github.com/user-attachments/assets/9bb5bda3-3676-4736-9022-a3e48ea3469f)

## Wht is a Gateway
An internet gateway is a virtual router that connects a VPC to the internet.
A gateway is a networking service which sits between two differents networks.Gateway often act as reverse proxies, firewall and load balancers

![image](https://github.com/user-attachments/assets/78b284bd-0643-4742-99e3-b291ae84485b)

## internet gateway (IGW)
Internet gateway allows both inbound and outbound internet traffic to my vpc.
![image](https://github.com/user-attachments/assets/9412df01-4079-4d59-a8df-4801e90c49ba)

### Egress-Only internet gateway (EO-IGW)
Are specifically for ipv6 when i want to allow outbound traffic to the internet but prevent inbound traffic from the internet.

![image](https://github.com/user-attachments/assets/35944d42-4427-4af9-8059-febccdef8df5)

## Elastic IPs
![image](https://github.com/user-attachments/assets/cbee36a0-a645-4c11-8052-ddaab958e224)
![image](https://github.com/user-attachments/assets/a6b1bdf1-4cf1-4ab7-a205-851d4551ec3c)

## AWS IPv6 Support
was develop to provide a solution for eventual exhaustion of all IPV4 addresses.
![image](https://github.com/user-attachments/assets/270d3060-53a8-4790-a0eb-981487d9d57e)

## Migrating from IPV4 to IPV6
IPv4 only vpcs can be migrateed to operate in dual stack mode (ipv4 and ipv6)

![image](https://github.com/user-attachments/assets/81ce897e-f7c9-40d6-a0b0-8df57d65bb12)

### AWS Direct connect
is the aws solutions to establish a dedicated network connection from on-premises locations to AWS

![image](https://github.com/user-attachments/assets/0f516b26-1b67-4da1-8314-85e22e5c7248)

A- Connection requirements:
![image](https://github.com/user-attachments/assets/38d2bbf3-5e45-4f30-ac85-4c94efd4e8fa)

B- Direction connect supports:

![image](https://github.com/user-attachments/assets/f99dbe4e-5f08-4730-a9a3-29bc6c42d83f)

C - There are three factor to pricing:

![image](https://github.com/user-attachments/assets/340c25a3-8478-4f29-9915-c355d1f40ac2)

### VPC endpoints 
Allow me to privately connect my vpc to others AWS and others services

![image](https://github.com/user-attachments/assets/689a3f2b-bbbe-439e-bbc8-357a5df18eec)

### Introduction to Private link
Is a broader service that allows me to securely connect my vpc to:

![image](https://github.com/user-attachments/assets/d2b30933-076b-4bf4-99ee-81682bb381ed)

### Interface Endpoint
Are Elastic Network interface (ENI) with a private IP address.

![image](https://github.com/user-attachments/assets/562fd255-62d5-4d36-9162-b05b2755afde)

### Gateway Load Balancer Endpoints
Allows me to distribute traffic to a fleet of network virtual appliances.

![image](https://github.com/user-attachments/assets/7e07da7b-fce7-4c86-b068-e6b430905d40)

### VPC Gatway Endpoints
provide reliable connectivity to Amazon s3 and dynamoDB without requiring an internet gateway or a NAT device for my VPC

![image](https://github.com/user-attachments/assets/8df83939-2eef-4092-9a45-6a2a9af8fb0e)

### VPC Endpoints Comparison
I am making a comparison of vpc endpoints to solidify my understanding.

![image](https://github.com/user-attachments/assets/b00333f2-7808-4b7b-9109-1f353935e14f)

### VPC Flow Logs
Allow me to capture IP traffic information through my VPC.

![image](https://github.com/user-attachments/assets/1973569c-a9c3-4a33-9be1-a3438673666d)

to make it more digest, here is a simple version

![image](https://github.com/user-attachments/assets/60751c65-ad50-496c-8c4d-7956f3b3d66e)

### AWS Virtual Private Network
Aws vpn lets me establish a secure and private tunnel form my network or device to the aws global network

![image](https://github.com/user-attachments/assets/2e169509-eb0d-4c61-bb83-ba84df613a54)

### AWS Site-to-Site VPN
Allow me to connect my vpc to my on-premise network.

![image](https://github.com/user-attachments/assets/f9052261-27cc-437c-b40a-8810c82f8134)

Features:

![image](https://github.com/user-attachments/assets/86697435-2cf9-404a-ab34-fe872662a246)

### Virtual Private Gateway (VGW)

![image](https://github.com/user-attachments/assets/537c19e6-0211-4500-8ed5-90c882a92923)

### Customer Gatway (CGW)
is a resource that i create in AWS that represents the customer gateway device in my on-premises network.

![image](https://github.com/user-attachments/assets/a8cd5965-86be-4522-9014-198332cee69f)

Diagram:

![image](https://github.com/user-attachments/assets/90798468-72cc-4a6e-a985-a1b3487b0506)

Aws provide sample configuration files for various customer gateway devices:

![image](https://github.com/user-attachments/assets/6bad85f8-9a54-4022-a257-8fb959dffff7)

### Transit Gatway (TGW)
Is a transit hub that i can use to interconnect my vpc and my on-premises networks

![image](https://github.com/user-attachments/assets/02a028cb-c4f4-4072-b249-503edbb92090)

### AWS Client VPN
is a fully manage client-based VPN service that enables me to securely access AWS resources and resources in my on-premises network.

![image](https://github.com/user-attachments/assets/e7afd5ec-b150-4397-bb36-5b91481d5cdc)

### Network Address Translation (NAT)
Is modifying my network address information in the ip header of packet while they are in transit accross a traffic-routing device.

![image](https://github.com/user-attachments/assets/5e5f08c9-c7d3-4e51-a1e3-c7f26f88f4a9)

### NAT Gateway
Is a fully fully managed NAT service to allow instances in your private subnet to establish outbound connections.

![image](https://github.com/user-attachments/assets/2ea5dfdf-fd08-48a6-b31d-018f3de8f7c5)

### DNS64 and  NAT64
A NAT gateway supports network address translation from IPV6 to IPv4, popularly know as NAT64

![image](https://github.com/user-attachments/assets/75b88351-0a43-43a2-aac5-3f7fb4b10f85)

### NAT instances
Is an AWS managed IAM to launch a NAT into an individual EC2 instance.
NAT instances required the customer to handle scaling

![image](https://github.com/user-attachments/assets/1f288b05-d4f4-4aaf-9327-b511d307e6a3)

### Bastion / Jumpbox
Jumpbox are security hardened virtual machines that provide secure access to private subnets.

![image](https://github.com/user-attachments/assets/a533e316-3162-474b-a9ca-3e2f34f1e0b1)

### VPC Lattecie
is a fully managed application networking service that i use to connect, secure, and monitor the services for my application

![image](https://github.com/user-attachments/assets/c43e4d44-cf8a-404a-8791-aab000b8179c)

![image](https://github.com/user-attachments/assets/94ab8758-4356-4937-9456-7850984596ac)

### Transit Gateway

![image](https://github.com/user-attachments/assets/3216b533-bfaf-42f5-86e5-3d22131db530)

### Traffic Mirroring
sends a copy network traffic from source ENI to target ENI, or UDP-enabled NLB or GWLB

![image](https://github.com/user-attachments/assets/f054e52e-f57d-4744-b833-ac32d0f9808c)

### Route 53 Resolver DNS Firewall
Is a DNS firewall that protect against DNS exfiltration of my data.

![image](https://github.com/user-attachments/assets/57faab4f-4751-42e8-a2c8-0d159cb3279a)

### AWS Network Firewall
is stateful, managed, network firewall and IDS/IPS for VPCs

![image](https://github.com/user-attachments/assets/78296cb6-9e7e-4404-9c02-f72193da7631)

### VPC peering
It allows me to connect one vpc with another over a direct network route using a private IP addresses.

![image](https://github.com/user-attachments/assets/2cd1e6b7-888c-4157-a078-536085c1cfee)

![image](https://github.com/user-attachments/assets/0764af6f-d23b-4bd4-a377-17449f3b30d2)

### Referencing SG in Peering VPC

![image](https://github.com/user-attachments/assets/9df1f58c-e9b9-4252-8a47-86f0ffd8b479)

### Network Address Usage
is a metric applied to  resources in my virtual network to help me plan for and monitor the sie of my vpc

![image](https://github.com/user-attachments/assets/b272831d-184e-423e-9666-af12914d8a81)

![image](https://github.com/user-attachments/assets/624e2f43-bc6e-4553-bed6-676305e361c9)

### Identity Access Management (IAM)
manages access of AWS users and resources.

![image](https://github.com/user-attachments/assets/c8d13d53-e489-40cb-a3ba-1f4a0dca2100)
