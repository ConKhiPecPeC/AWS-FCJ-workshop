---
title : "Cấu hình Route Table"
date :  2025-05-21 
weight : 5
chapter : false
pre : " <b> 2.2.5 </b> "
---

#### Public Route Table
1. Tại **VPC Dashboard** chọn **Route table** chọn **Create route table**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0001-VPCdashboard.png)
2. Tại trang **Create route table**
    - **Name** điền **public-route**
    - **VPC** chọn VPC đã tạo
    - Chọn **Create route table**  
    ![Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0002-CreatePublicRoute.png)
3. Chọn route table vừa tạo chọn **Edit route**
    ![Edit Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0003-EditPublicRoute.png)
4. Chọn **Add route**
Tạo 2 route để route tới Internet Gateway và Egress only internet gateway
    - Destionation **0.0.0.0/24** Target **Internet Gateway** - **igw-09881de6e00fff886**
    - Destination **::/0** Target **Egress Only Internet Gateway** - **eigw-0cfa00385fe41e2a3**
    - Chọn **Save change** để lưu lại
    ![Add Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0004-PublicRoute.png)
5. Chọn **public-route** vừa tạo chọn **Action** chọn **Edit subnet associations**
    ![Edit Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0005-EditSubnetAssociation.png)
6. Tích chọn **public-subnet-1a** và **public-subnet-1b** rồi chọn **Save Associations**
    ![Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0006-SubnetAssociation.png)

#### Private Route Table 
1. Tại **VPC Dashboard** chọn **Route table** chọn **Create route table**
    ![VPC Dashboard](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0007-VPCDashboard.png)
2. Tại trang **Create route table**
    - **Name** điền **private-route**
    - **VPC** chọn VPC đã tạo
    - Chọn **Create route table**
    ![Create Private Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0008-CreatePrivateRoute.png)
3. Chọn route table vừa tạo chọn **Edit route**
    ![Edit Public Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0009-CreatePrivateRoute.png)    
4. Chọn route table vừa tạo chọn **Edit route**
Tạo route để đi tới NAT gateway
    - Chọn **Add route**
    - Destionation **0.0.0.0/0** Target **NAT Gateway** - **nat-00f40babba2f71fa4**
    - Chọn **Save change** để lưu lại
    ![Create Private Route](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0010-PrivateRoute.png)
5. Chọn **public-route** vừa tạo chọn **Action** chọn **Edit subnet associations**
    ![Edit Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0011-SubnetAssociation.png)
6.  Tích chọn **public-subnet-1a** và **public-subnet-1b** rồi chọn **Save Associations**
    ![Subnet Association](/images/2-Setup-Resource/2.2-CreateVPC/2.2.5-RouteTable/0012-PrivateRouteAssociation.png)
