---
title : "Create Subnets"
date :  2025-05-21 
weight : 2
chapter : false
pre : " <b> 2.2.2 </b> "
---

#### Create public subnet
1. In the **VPC Dashboard** choose **Subnets** from the left panel then click **Create subnet**
    ![VPC Dashboard create subnets](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0001-VPCDashboard.png)
2. In the **Create Subnet**
    - **VPC ID** Select the VPC you just created
    - **Subnet name** type **public-subnet-1a**
    - **Availability Zone** choose **us-east-1a**
    - **IPv4 subnet CIDR block** type **10.0.0.0/24**
    - **IPv6 subnet CIDR block** type **2600:1f18:7004:7800::/64**
    - Choose **Create Subnet**
    ![create Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0002-PublicSubnet.png)
    ![create Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0003-PublicSubnet.png)
3. Repeat the process with **public-subnet-1b**
    - **Subnet name** type **public-subnet-1b**
    - **Availability Zone** choose **us-east-1b**
    - **IPv4 subnet CIDR block** type **10.0.1.0/24**
    - **IPv6 subnet CIDR block** type **2600:1f18:7004:7801::/64**
#### Create private subnet
1. In the **VPC Dashboard** choose **Subnets** from the left panel choose **Create subnet**
2. In the **Create Subnet**
    - **VPC ID** choose VPC you just create
    - **Subnet name** type **private-subnet-1a**
    - **Availability Zone** choose **us-east-1a**
    - **IPv4 subnet CIDR block** type **10.0.2.0/24**
    - **IPv6 subnet CIDR block** type **2600:1f18:7004:7802::/64**
    - choose **Create Subnet**
    ![create Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0004-PrivateSubnet.png)
    ![create Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0005-PrivateSubnet.png)
3. Repeat the process with **private-subnet-1b**
    - **Subnet name** type **privateprivate-subnet-1b**
    - **Availability Zone** choose **us-east-1b**
    - **IPv4 subnet CIDR block** type **10.0.3.0/24**
    - **IPv6 subnet CIDR block** type **2600:1f18:7004:7803::/64**

{{% notice note %}}
To implement a Multi-AZ setup, each Availability Zone should have one public and one private subnet. You can use multiple AZs within a region depending on your needs and use case.
{{% /notice %}}