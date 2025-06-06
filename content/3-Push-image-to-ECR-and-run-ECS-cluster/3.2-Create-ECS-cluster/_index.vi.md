---
title : "Tạo và run task với ECS cluster"
date :  2025-05-21 
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

1. Tại **AWS Management Console** tìm **Elastic Container Service** 
    ![AWS Console](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0001-AWSConsole.png)
2. Tại thanh bên trái chọn **Clusters** chọn **Create Cluster**
    ![Create Cluster](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0002-ECS.png)
3. Trong phần **Create cluster**
    - Nhập **Cluster name** là **fcj-my-cluster**
    - Trong phần **Infrastructure** chọn **AWS Fargate**
    - Kéo xuống và chọn **Create**
    ![Create Cluster](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0003-CreateCluster.png)
4. Quay lại **ECS Management Console** tại thanh bên trái chọn **Task definitions** chọn **Create new task definition**
    ![Create Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0004-TaskDefinitions.png)
5. Tại trang **Create new task definition**
    - Trong phần **Task definition configuration** trong ô **Task definition family** điền **my-task**
    - Trong phần **Infrastructure requirements**  
      - **Launch type** chọn **AWS Fargate**
      - **Task execution role** chọn **ECS-TaskExecute**
    - Trong phần **Container** 
      - **Name** nhập **2048**
      - **Image URI** nhập **199464522308.dkr.ecr.us-east-1.amazonaws.com/fcj-my-repo**
      - **Container port** nhập **8080**    
    - Kéo xuống và ấn **Create**
    ![Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0005-TaskDefine.png)
    ![Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0006-TaskDefine.png) 
    ![Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0007-TaskDefine.png)
6. Quay lại **ECS Management Console** chọn **Cluster** chọn vào cluster đã tạo kéo xuống chọn **Tasks** và chọn **Run new task**
    ![Run New Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0008-RunNewTask.png)
7. Tại cửa sổ **Run task**
    - **Task definition family** chọn **my-task**
    - **Desired tasks** điền **3**
    - Trong phần **Compute options** chọn **Lauch type**
    ![Run Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0009-CreateTask.png)
    - Trong phần **Networking**
      - **VPC** chọn **my-dual-vpc**
      - **Subnets** chọn **private-subnet-1a** và **private-subnet-1b**
      - **Security group** chọn **Use an existing security group** và chọn **Private-SG**
      - **Public IP** chọn **Turn off**
    - Kéo xuống và chọn **Create**
    ![Run Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0010-CreateTask.png)
8. Quay lại **ECS Management Console** và đợi cho trạng thái các task là **Running**
    ![Run Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0011-TaskStatus.png)
{{% notice note %}}
Chọn các task và lưu lại địa chỉ IP private của các task
{{% /notice %}}