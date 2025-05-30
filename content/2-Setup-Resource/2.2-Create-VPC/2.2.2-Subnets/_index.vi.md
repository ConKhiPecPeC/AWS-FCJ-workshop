---
title : "Tạo Subnets"
date :  2025-05-21 
weight : 2
chapter : false
pre : " <b> 2.2.2 </b> "
---

#### Tạo public subnet
1. Tại **VPC Dashboard** chọn **Subnets** ở góc trái rồi chọn **Create subnet**
    ![VPC Dashboard tạo subnets](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0001-VPCDashboard.png)
2. Trong phần **Create Subnet**
    - **VPC ID** chọn VPC vừa tạo
    - **Subnet name** điền **public-subnet-1a**
    - **Availability Zone** chọn **us-east-1a**
    - **IPv4 subnet CIDR block** điền **10.0.0.0/24**
    - **IPv6 subnet CIDR block** điền **2600:1f18:7004:7800::/64**
    - Chọn **Create Subnet**
    ![Tạo Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0002-PublicSubnet.png)
    ![Tạo Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0003-PublicSubnet.png)
3. Tương tự tạo **public-subnet-1b**
    - **Subnet name** điền **public-subnet-1b**
    - **Availability Zone** chọn **us-east-1b**
    - **IPv4 subnet CIDR block** điền **10.0.1.0/24**
    - **IPv6 subnet CIDR block** điền **2600:1f18:7004:7801::/64**
#### Tạo private subnet
1. Tại **VPC Dashboard** chọn **Subnets** ở góc trái rồi chọn **Create subnet**
2. Trong phần **Create Subnet**
    - **VPC ID** chọn VPC vừa tạo
    - **Subnet name** điền **private-subnet-1a**
    - **Availability Zone** chọn **us-east-1a**
    - **IPv4 subnet CIDR block** điền **10.0.2.0/24**
    - **IPv6 subnet CIDR block** điền **2600:1f18:7004:7802::/64**
    - Chọn **Create Subnet**
    ![Tạo Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0004-PrivateSubnet.png)
    ![Tạo Subnet](/images/2-Setup-Resource/2.2-CreateVPC/2.2.2-Subnets/0005-PrivateSubnet.png)
3. Tương tự tạo **private-subnet-1b**
    - **Subnet name** điền **privateprivate-subnet-1b**
    - **Availability Zone** chọn **us-east-1b**
    - **IPv4 subnet CIDR block** điền **10.0.3.0/24**
    - **IPv6 subnet CIDR block** điền **2600:1f18:7004:7803::/64**

{{% notice note %}}
Nhằm mục đích triển khai Multi-AZ, trên mỗi AZ có 1 public và 1 private subnet, có thể sử dụng nhiều AZ khác nhau trong 1 region tùy theo nhu cầu và mục đích sử dụng
{{% /notice %}}