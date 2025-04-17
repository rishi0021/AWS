#vpc project 

1.create a vpc ->vpc and more
2.project name 
3.no vpc end pont for s3 
4.create auto scaling group
    launch template (name ,discription, select ami, instance,pair key)
    created a security group for ssh
    select the created vpc
    slect the port that your app is working on 
    network 
      slect the created VPC / private subnet that you need
     group size 
       desire/min /max
    check if instances created 
5.create bastion host 
    create a instance which has ssh enable in the VPC 
    auto assign the public address
6.add the key pair of vpc to bastion host
    scp -i identity_file path_of_file ubuntu@ipaddress: paste_location
    copy file from one host machine to other
7.login into bastion host 
8.ssh into the vpc private instance using the pem file and private ip
9.in the private instance create a html file
10. host it on a python server "python3 -m http.server portno"

11.create a loadbalancer 
  select VPC
  select public subnet
  select the security group
    create a target group
  select a target group /port
  select instance/port 
12.go to load balance 
  go to security group -> allow http traffic
13. copy the dns name of loadbalancer access from a browser 

output:
![image](https://github.com/user-attachments/assets/1b4f73da-8c2d-435c-a70a-ebd5af41b32f)

    
    
