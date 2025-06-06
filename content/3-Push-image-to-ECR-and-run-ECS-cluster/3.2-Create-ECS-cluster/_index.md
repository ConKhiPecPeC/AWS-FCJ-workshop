---
title : "Create and run task with ECS cluster"
date :  2025-05-21 
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

1. In the **AWS Management Console** search for **Elastic Container Service** 
    ![AWS Console](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0001-AWSConsole.png)
2. In the left pannel choose **Clusters** then choose **Create Cluster**
    ![Create Cluster](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0002-ECS.png)
3. In the **Create cluster**
    - Type **Cluster name**: **fcj-my-cluster**
    - In the **Infrastructure** choose **AWS Fargate**
    - Scroll down and choose **Create**
    ![Create Cluster](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0003-CreateCluster.png)
4. Back to **ECS Management Console** in the left pannel choose **Task definitions** then choose **Create new task definition**
    ![Create Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0004-TaskDefinitions.png)
5. In the **Create new task definition**
    - In the **Task definition configuration** in **Task definition family** type **my-task**
    - In the **Infrastructure requirements**  
      - **Launch type** choose **AWS Fargate**
      - **Task execution role** choose **ECS-TaskExecute**
    - In the **Container** 
      - **Name** type **2048**
      - **Image URI** type **199464522308.dkr.ecr.us-east-1.amazonaws.com/fcj-my-repo**
      - **Container port** type **8080**    
    - Scroll down and click **Create**
    ![Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0005-TaskDefine.png)
    ![Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0006-TaskDefine.png) 
    ![Task Definitions](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0007-TaskDefine.png)
6. Back to **ECS Management Console** choose **Cluster** choose cluster just create, then scroll down and choose **Tasks** and choose **Run new task**
    ![Run New Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0008-RunNewTask.png)
7. In the **Run task**
    - **Task definition family** choose **my-task**
    - **Desired tasks** type **3**
    - In the **Compute options** choose **Lauch type**
    ![Run Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0009-CreateTask.png)
    - In the **Networking**
      - **VPC** choose **my-dual-vpc**
      - **Subnets** choose **private-subnet-1a** và **private-subnet-1b**
      - **Security group** choose **Use an existing security group** and choose **Private-SG**
      - **Public IP** choose **Turn off**
    - Scroll down and choose **Create**
    ![Run Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0010-CreateTask.png)
8. Back to **ECS Management Console** and wait until task status is **Running**
    ![Run Task](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.2-Create-ECS-cluster/0011-TaskStatus.png)
{{% notice note %}}
Select all task and save all task private IP for next step
{{% /notice %}}