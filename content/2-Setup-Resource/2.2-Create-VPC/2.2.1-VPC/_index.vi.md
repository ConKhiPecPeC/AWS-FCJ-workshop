---
title : "Tạo VPC"
date :  2025-05-21 
weight : 1
chapter : false
pre : " <b> 2.2.1 </b> "
---

#### Tạo VPC hỗ trợ dual-stack
1. Tại **AWS Management Console** tìm **VPC**
    ![AWS Console](/images/2-Setup-Resource/2.2-CreateVPC/2.2.1-VPC/0001-AWSConsole.png)
2. Chọn **Create VPC**
    ![Create VPC](/images/2-Setup-Resource/2.2-CreateVPC/2.2.1-VPC/0002-CreateVPC.png)
3. Trong phần **Create VPC**
    - Chọn **VPC only**
    - **Name tag** điền **my-dual-vpc**
    - **IPv4 CIDR** điền **10.0.0.0/16**
    - **IPv6 CIDR block** chọn **Amazon-provided IPv6 CIDR block**
    - Kéo xuống và chọn **Create VPC**
    ![VPC Configure](/images/2-Setup-Resource/2.2-CreateVPC/2.2.1-VPC/0003-VPCConfigure.png)
