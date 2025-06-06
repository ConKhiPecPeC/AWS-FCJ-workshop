---
title : "Create VPC"
date :  2025-05-21 
weight : 1
chapter : false
pre : " <b> 2.2.1 </b> "
---

#### Tạo VPC hỗ trợ dual-stack
1. In the **AWS Management Console** search for **VPC**
    ![AWS Console](/images/2-Setup-Resource/2.2-CreateVPC/2.2.1-VPC/0001-AWSConsole.png)
2. Click **Create VPC**
    ![Create VPC](/images/2-Setup-Resource/2.2-CreateVPC/2.2.1-VPC/0002-CreateVPC.png)
3. In **Create VPC**
    - Choose **VPC only**
    - **Name tag** type **my-dual-vpc**
    - **IPv4 CIDR** type **10.0.0.0/16**
    - **IPv6 CIDR block** choose **Amazon-provided IPv6 CIDR block**
    - Scroll down and click **Create VPC**
    ![VPC Configure](/images/2-Setup-Resource/2.2-CreateVPC/2.2.1-VPC/0003-VPCConfigure.png)