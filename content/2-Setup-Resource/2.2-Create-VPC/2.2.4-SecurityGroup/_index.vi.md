---
title : "Tạo các Security Group"
date :  2025-05-21 
weight : 4
chapter : false
pre : " <b> 2.2.4 </b> "
---

#### Tạo public Security Group
1. Tại **VPC Dashboard** chọn **Security Group** chọn **Create security group**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0001-VPCDashboard.png)
2. Tại trang **Create security group**
    - **Security group name** điền **Public-SG**
    - **Description** điền **Allows HTTP and HTTPs**
    - **VPC** chọn VPC đã tạo
    ![Public SG](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0002-PublicSG.png)
3. Cấu hình **Inbound rules**
Chọn **Add rule**
    - Type **HTTP** Source **Anywhere-IPv4**
    - Type **HTTP** Source **Anywhere-IPv6**
    - Type **HTTPS** Source **Anywhere-IPv4**
    - Type **HTTPS** Source **Anywhere-IPv6**
Kéo xuống và chọn **Create security group**s
    ![Public SG](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0003-PublicSG.png)


#### Tạo private Security Group
1. Tại **VPC Dashboard** chọn **Security Group** chọn **Create security group**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0004-VPCDashboard.png)
2. Tại trang **Create security group**
    - **Security group name** điền **Private-SG**
    - **Description** điền **Allows TCP port 8080**
    - **VPC** chọn VPC đã tạo
Cấu hình **Inbound rules**
    - Chọn **Add rule**
    - Type **Custom TCP** Port range **8080** Source **Custom** chọn **Secutiry group** chọn **Public-SG** đã tạo ở trên
    - Kéo xuống và chọn **Create security group**
    ![Public SG](/images/2-Setup-Resource/2.2-CreateVPC/2.2.4-SecurityGroup/0005-Private-SG.png)