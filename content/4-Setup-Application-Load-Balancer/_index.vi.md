---
title : "Triển khai Load Balancer"
date :  2025-05-21 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Cấu hình Target Group
1. Tại **AWS Management Console** **EC2**
    ![AWS Console](/images/4-Setup-Application-Load-Balancer/0001-AWSConsole.png)
2. Tại thanh bên trái trong phần **Load Balancing** chọn **Target Groups** rồi chọn **Create target group**
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0002-CreateTargetGroup.png)
3. Tại trang **Specify group details**
    - Trong phần **Choose a target type** chọn **IP addresses**
    - **Target group name** điền **ECS-TaskRunner**
    - **Protocol** chọn **HTTP** và **Port** điền **8080**
    - **VPC** chọn **my-dual-vpc**
    - Kéo xuống và ấn **Next**
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0003-CreateTargetGroup.png)
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0004-CreateTargetGroup.png)
4. Tại trang **Register targets** 
    - **Step 1: Choose a network** chọn **my-dual-vpc**
    - **Step 2: Specify IPs and define ports**
      - Điền **10.0.2.40**
      - Chọn **Add IPv4 address** rồi điền **10.0.3.32**
      - Chọn **Add IPv4 address** rồi điền **10.0.3.190**
      - Chọn **Include as pending below**
    - Kéo xuống và chọn **Create target group**
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0005-CreateTargetGroup.png)
#### Cấu hình Application Load Balancer
1. Tại **EC2 Management Console** chọn **Load balancers** rồi chọn **Create Load Balancer**
    ![EC2 Management Console](/images/4-Setup-Application-Load-Balancer/0006-LoadBalancer.png)
2. **Load balancer types** chọn **Application Load Balancer** và ấn **Create**
3. Tại trang **Basic configuration**
    - **Basic configuration**
      - **Load balancer name** điền **fcj-my-alb**
      - **Scheme** chọn **Internet-facing**
      - **Load balancer IP address type** chọn **Dualstack**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0007-ALB.png)
    - **Network mapping**
      - **VPC** chọn **my-dual-vpc**
      - **Availability Zones and subnets** chọn 2 AZ 
        - **us-east-1a** và **public-subnet-1a**  
        - **us-east-1b** và **public-subnet-1b**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0008-ALB.png)
    - **Security groups** chọn **Public-SG**
    - **Listeners and routing** 
      - **Protocol** chọn **HTTP** 
      - **Port** điền **80**
      - **Default action** chọn Target group vừa tạo **ECS-TaskRunner**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0009-ALB.png)
    - Kéo xuống và chọn **Create load balancer**
4. Đợi cho trạng thái của Application Load Balancer chuyển thành **Active**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0010-ALBStatus.png)
5. Truy cập ứng dụng thông qua DNS name của AWS 
    ![Application](/images/4-Setup-Application-Load-Balancer/0011-App.png)

{{% notice note %}}
Dùng nslookup dns name của AWS trả về hai loại địa chỉ là IPv4 và IPv6
    ![nslookup](/images/4-Setup-Application-Load-Balancer/0012-nslookup.png)
{{% /notice %}}