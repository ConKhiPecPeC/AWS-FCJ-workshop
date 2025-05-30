---
title : "Tạo các gateways"
date :  2025-05-21 
weight : 3
chapter : false
pre : " <b> 2.2.3 </b> "
---

#### Internet gateways
1. Tại **VPC Dashboard** chọn **Internet gateways**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0001-VPC-internetgateway.png)
2. **Name tag** điền **dual-vpc-igw**
    ![CreateIGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0002-CreateIGW.png)
3. Tại trang **Internet gateways**
    - Chọn interet gateway vừa tạo 
    - Trong phần **Action**
    - Chọn **Attach to VPC**
    ![AttachIGWAttachIGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0003-AttachIGW.png)
4. Chọn **VPC** đã tạo rồi chọn **Attach internet gateway**
    ![AttachIGWAttachIGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0004-AttachIGW.png)
#### NAT gateways
1. Tại **VPC Dashboard** chọn **Elastic IPs** chọn **Allocate Elastic IP address**
2. Tại trang **Allocate Elastic IP address** chọn **Allocate**
    ![AllocateIPs](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0005-AllocateIPs.png)
3. Quay lại **VPC Dashboard** chọn **NAT gateways** rồi chọn **Create NAT gateway**
4. Tại trang **Create NAT gateways**
    - **Name** điền **dual-vpc-ngw**
    - **Subnet** chọn **public-subnet-1a**
    - **Connectivity type** chọn **public**
    - **Elastic IP allocation ID** chọn IP vừa tạo
    - Chọn **Create NAT gateway**
    ![CreateNAT Gateway](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0006-CreateNATgateway.png)
#### Egress only internet gateways
1. Tại **VPC Dashboard** chọn **Egress only internet gateways** chọn **Create egress only internet gateways**
    ![VPC Dashboard EGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0007-VPCDashboardEGW.png)
2. Tại trang **Create egress only internet gateway**
    - **Name** điền **dual-vpc-egw**
    - **VPC** chọn VPC đã tạo
    - Chọn **Create egress only internet gateway**
    ![Create EGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0008-CreateEGW.png)