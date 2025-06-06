---
title : "Create Security Group"
date :  2025-05-21 
weight : 4
chapter : false
pre : " <b> 2.2.4 </b> "
---

#### Create public Security Group
1. In the **VPC Dashboard** choose **Security Group** choose **Create security group**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0001-VPCDashboard.png)
2. In the **Create security group**
    - **Security group name** type **Public-SG**
    - **Description** type **Allows HTTP and HTTPs**
    - **VPC** choose VPC just create
    ![Public SG](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0002-PublicSG.png)
3. Configure **Inbound rules**
Choose **Add rule**
    - Type **HTTP** Source **Anywhere-IPv4**
    - Type **HTTP** Source **Anywhere-IPv6**
    - Type **HTTPS** Source **Anywhere-IPv4**
    - Type **HTTPS** Source **Anywhere-IPv6**

Scroll down and choose **Create security group**
    ![Public SG](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0003-PublicSG.png)

#### Create private Security Group
1. In the**VPC Dashboard** choose **Security Group** choose **Create security group**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0004-VPCDashboard.png)
2. In the **Create security group**
    - **Security group name** type **Private-SG**
    - **Description** type **Allows TCP port 8080**
    - **VPC** choose VPC just create
3. Configure **Inbound rules**
    - Choose **Add rule**
    - Type **Custom TCP** Port range **8080** Source **Custom** choose **Secutiry group** choose **Public-SG** just create above
    - Scroll down and choose **Create security group**
    ![Public SG](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0005-Private-SG.png)