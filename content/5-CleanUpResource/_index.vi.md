---
title : "Dọn dẹp tài nguyên"
date :  2025-05-21 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---
Dọn dẹp tài nguyên
 #### 1. Xóa Application Load Balancer và Target group
- Xóa Application Load Balancer
  - Truy cập **EC2 Management Console** 
  - Tại thanh bên trái chọn **Load Balancers**
  - Tích chọn vào **fcj-my-alb** 
  - Chọn **Action** rồi chọn **Delete load balancer**
  - Điền **confirm** rồi chọn **Delete**
- Xóa Target Group
  - Truy cập **EC2 Management Console**
  - Tại thanh bên trái chọn **Target Groups**
  - Tích chọn vào **ECS-TaskRunner**
  - Chọn **Action** rồi chọn **Delete**
  - Chọn **Delete**
 #### 2. Xóa ECS Cluster
- Xóa Cluster
  - Truy cập **ECS Management Console**
  - Chọn **Clusters** rồi chọn **fcj-my-cluster**
  - Vào **Tasks** chọn **Stop** rồi chọn **Stop all**
  - Nhập **stop all tasks** rồi chọn **Stop all** đợi đến khi staus của các task là **Stopped**
  - Chọn **Delete Cluster**
  - Nhập **delete fcj-my-cluster** rồi chọn **Delete**
- Xóa Task Definitions
  - Truy cập **ECS Management Console**
  - Chọn **Task definitions** rồi chọn **my-task**
  - Chọn phần **Task definition: revision** tích chọn tất cả 
  - Chọn **Acion** chọn **Deregister** chọn **Deregister**
 #### 3. Xóa ECR repositories
- Xóa ECR repositories
  - Truy cập **ECR Management Console**
  - Chọn **Repositories** trong **Private registry**
  - Tích chọn **fcj-my-repo** chọn **Delete** rồi chọn **Delete**
 #### 4. Xóa VPC và các tài nguyên trong VPC
- Xóa NAT gateways
  - Truy cập **VPC Management Console** 
  - Tại thanh điều hướng bên trái chọn **NAT gateways**
  - Chọn **NAT gateways** liên quan tới bài **dual-vpc-ngw** 
  - Chọn **Action** chọn **Delete NAT gateway**
  - Nhập **delete** rồi chọn **Delele**
- Giả phóng Elastic IP Addresses
  - Truy cập **VPC Management Console** 
  - Tại thanh điều hướng bên trái chọn **Elastic IPs**
  - Chọn **Elastic IPs** đã tạo 
  - Chọn **Action** chọn **Release Elastic IP addresses**
  - Chọn **Release**
- Xóa Internet gateways
  - Truy cập **VPC Management Console** 
  - Tại thanh điều hướng bên trái chọn **Internet gateways** 
  - Chọn **Internet gateways** liên quan tới bài **dual-vpc-igw**
  - Chọn **Action** chọn **Detach from VPC** rồi chọn **Detach internet gateway**
  - Chọn **Action** chọn **Delete internet gateway** 
  - Nhập **delete** chọn **Delete internet gateway**
- Xóa Egress only internet gateways
  - Truy cập **VPC Management Console** 
  - Tại thanh điều hướng bên trái chọn **Egress-only internet gateways**
  - Chọn **Egress only internet gateways** liên quan tới bài **dual-vpc-egw**
  - Chọn **Action** chọn **Delete egress only internet gateway**
  - Nhập **delete** chọn **Delete egress only internet gateway**
- Xóa VPC 
  - Truy cập **VPC Management Console**
  - Tại thanh điều hướng bên trái chọn **Your VPCs**
  - Chọn **VPC** liên quan đến bài **my-dual-vpc**
  - Chọn **Action** chọn **Delete VPC**
  - Nhập **delete** chọn **Delete**

{{% notice tip %}}
Khi xóa VPC, AWS sẽ tự động xóa các tài nguyên liên quan như: Subnets, Route Table, Security Group và Internet Gateways
{{% /notice %}}