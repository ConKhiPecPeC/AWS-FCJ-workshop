---
title : "Deploy Load Balancer"
date :  2025-05-21 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### Cấu hình Target Group
1. In the **AWS Management Console** **EC2**
    ![AWS Console](/images/4-Setup-Application-Load-Balancer/0001-AWSConsole.png)
2. In the left pannel of **Load Balancing** choose **Target Groups** then choose **Create target group**
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0002-CreateTargetGroup.png)
3. In the **Specify group details**
    - In the **Choose a target type** choose **IP addresses**
    - **Target group name** type **ECS-TaskRunner**
    - **Protocol** choose **HTTP** and **Port** type **8080**
    - **VPC** choose **my-dual-vpc**
    - Scroll down and click **Next**
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0003-CreateTargetGroup.png)
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0004-CreateTargetGroup.png)
4. In the **Register targets** 
    - **Step 1: Choose a network** choose **my-dual-vpc**
    - **Step 2: Specify IPs and define ports**
      - type **10.0.2.40**
      - Choose **Add IPv4 address** then type **10.0.3.32**
      - Choose **Add IPv4 address** then type **10.0.3.190**
      - Choose **Include as pending below**
    - Scroll down and choose **Create target group**
    ![Target Group](/images/4-Setup-Application-Load-Balancer/0005-CreateTargetGroup.png)
#### Cấu hình Application Load Balancer
1. In the **EC2 Management Console** choose **Load balancers** then choose **Create Load Balancer**
    ![EC2 Management Console](/images/4-Setup-Application-Load-Balancer/0006-LoadBalancer.png)
2. **Load balancer types** choose **Application Load Balancer** and click **Create**
3. In the **Basic configuration**
    - **Basic configuration**
      - **Load balancer name** type **fcj-my-alb**
      - **Scheme** choose **Internet-facing**
      - **Load balancer IP address type** choose **Dualstack**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0007-ALB.png)
    - **Network mapping**
      - **VPC** choose **my-dual-vpc**
      - **Availability Zones and subnets** choose 2 AZ 
        - **us-east-1a** and **public-subnet-1a**  
        - **us-east-1b** and **public-subnet-1b**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0008-ALB.png)
    - **Security groups** choose **Public-SG**
    - **Listeners and routing** 
      - **Protocol** choose **HTTP** 
      - **Port** type **80**
      - **Default action** choose Target group just create **ECS-TaskRunner**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0009-ALB.png)
    - Scroll down and choose **Create load balancer**
4. Wait until status of Application Load Balancer is **Active**
    ![ALB](/images/4-Setup-Application-Load-Balancer/0010-ALBStatus.png)
5. Access application through DNS name of AWS 
    ![Application](/images/4-Setup-Application-Load-Balancer/0011-App.png)

{{% notice note %}}
Use nslookup dns name of AWS return both IPv4 and IPv6
    ![nslookup](/images/4-Setup-Application-Load-Balancer/0012-nslookup.png)
{{% /notice %}}