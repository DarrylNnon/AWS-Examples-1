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

