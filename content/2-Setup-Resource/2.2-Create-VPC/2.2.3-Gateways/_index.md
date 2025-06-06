---
title : "Create gateways"
date :  2025-05-21 
weight : 3
chapter : false
pre : " <b> 2.2.3 </b> "
---

#### Internet gateways
1. In the **VPC Dashboard** choose **Internet gateways**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0001-VPC-internetgateway.png)
2. **Name tag** type **dual-vpc-igw**
    ![CreateIGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0002-CreateIGW.png)
3. In the **Internet gateways**
    - choose interet gateway just create 
    - In **Action**
    - choose **Attach to VPC**
    ![AttachIGWAttachIGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0003-AttachIGW.png)
4. Choose **VPC** you just create then choose **Attach internet gateway**
    ![AttachIGWAttachIGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0004-AttachIGW.png)
#### NAT gateways
1. In the **VPC Dashboard** choose **Elastic IPs** choose **Allocate Elastic IP address**
2. In the **Allocate Elastic IP address** choose **Allocate**
    ![AllocateIPs](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0005-AllocateIPs.png)
3. Quay lại **VPC Dashboard** choose **NAT gateways** then choose **Create NAT gateway**
4. In the **Create NAT gateways**
    - **Name** type **dual-vpc-ngw**
    - **Subnet** choose **public-subnet-1a**
    - **Connectivity type** choose **public**
    - **Elastic IP allocation ID** choose IP you just create
    - choose **Create NAT gateway**
    ![CreateNAT Gateway](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0006-CreateNATgateway.png)
#### Egress only internet gateways
1. In the **VPC Dashboard** choose **Egress only internet gateways** choose **Create egress only internet gateways**
    ![VPC Dashboard EGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0007-VPCDashboardEGW.png)
2. In the **Create egress only internet gateway**
    - **Name** type **dual-vpc-egw**
    - **VPC** choose VPC you just create
    - choose **Create egress only internet gateway**
    ![Create EGW](/images/2-Setup-Resource/2.2-CreateVPC/2.2.3-Gateways/0008-CreateEGW.png)