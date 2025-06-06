---
title : "Configure Route Table"
date :  2025-05-21 
weight : 5
chapter : false
pre : " <b> 2.2.5 </b> "
---

#### Public Route Table
1. In the **VPC Dashboard** choose **Route table** choose **Create route table**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0001-VPCdashboard.png)
2. In the **Create route table**
    - **Name** type **public-route**
    - **VPC** choose VPC just create
    - Choose **Create route table**  
    ![Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0002-CreatePublicRoute.png)
3. Choose route table just create and choose **Edit route**
    ![Edit Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0003-EditPublicRoute.png)
4. Choose **Add route**
Create 2 route to route to Internet Gateway and Egress only internet gateway
    - Destionation **0.0.0.0/24** Target **Internet Gateway** - **igw-09881de6e00fff886**
    - Destination **::/0** Target **Egress Only Internet Gateway** - **eigw-0cfa00385fe41e2a3**
    - Choose **Save change** to save
    ![Add Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0004-PublicRoute.png)
5. Choose **public-route** just create choose **Action** choose **Edit subnet associations**
    ![Edit Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0005-EditSubnetAssociation.png)
6. Choose **public-subnet-1a** and **public-subnet-1b** then choose **Save Associations**
    ![Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0006-SubnetAssociation.png)

#### Private Route Table 
1. In the **VPC Dashboard** choose **Route table** choose **Create route table**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0007-VPCDashboard.png)
2. In the **Create route table**
    - **Name** type **private-route**
    - **VPC** choose VPC just create
    - Choose **Create route table**
    ![Create Private Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0008-CreatePrivateRoute.png)
3. Choose route table just create Create choose **Edit route**
    ![Edit Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0009-CreatePrivateRoute.png)    
4. Choose route table just create then choose **Edit route**
Create route to route to NAT gateway
    - Choose **Add route**
    - Destionation **0.0.0.0/0** Target **NAT Gateway** - **nat-00f40babba2f71fa4**
    - Choose **Save change** to save
    ![Create Private Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0010-PrivateRoute.png)
1. Choose **public-route** just create choose **Action** choose **Edit subnet associations**
    ![Edit Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0011-SubnetAssociation.png)
2. Choose **public-subnet-1a** and **public-subnet-1b** then choose **Save Associations**
    ![Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0012-PrivateRouteAssociation.png)