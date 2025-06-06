---
title : "Resource Cleanup"
date : 2025-05-21
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

# Resource Cleanup

#### 1. Delete Application Load Balancer and Target Group
- **Delete the Application Load Balancer**
  - Go to the **EC2 Management Console**
  - In the left-hand menu, select **Load Balancers**
  - Select **fcj-my-alb**
  - Click **Actions** then choose **Delete load balancer**
  - Type **confirm** and then click **Delete**

- **Delete the Target Group**
  - Go to the **EC2 Management Console**
  - In the left-hand menu, select **Target Groups**
  - Select **ECS-TaskRunner**
  - Click **Actions**, then choose **Delete**
  - Click **Delete**

#### 2. Delete ECS Cluster
- **Delete the Cluster**
  - Go to the **ECS Management Console**
  - Click **Clusters**, then select **fcj-my-cluster**
  - Go to **Tasks**, click **Stop**, then choose **Stop all**
  - Enter **stop all tasks**, then click **Stop all**, and wait until all task statuses show **Stopped**
  - Click **Delete Cluster**
  - Enter **delete fcj-my-cluster**, then click **Delete**

- **Delete Task Definitions**
  - Go to the **ECS Management Console**
  - Click **Task definitions**, then select **my-task**
  - In the **Task definition: revision** section, select all revisions
  - Click **Actions**, then choose **Deregister**, and confirm with **Deregister**

#### 3. Delete ECR Repositories
- **Delete ECR repositories**
  - Go to the **ECR Management Console**
  - Under **Private registry**, click **Repositories**
  - Select **fcj-my-repo**, then click **Delete**, and confirm with **Delete**

#### 4. Delete VPC and Associated Resources
- **Delete NAT Gateways**
  - Go to the **VPC Management Console**
  - In the left navigation pane, select **NAT Gateways**
  - Select NAT gateways related to **dual-vpc-ngw**
  - Click **Actions**, then **Delete NAT gateway**
  - Type **delete**, then click **Delete**

- **Release Elastic IP Addresses**
  - Go to the **VPC Management Console**
  - In the left navigation pane, select **Elastic IPs**
  - Select the created **Elastic IPs**
  - Click **Actions**, then **Release Elastic IP addresses**
  - Click **Release**

- **Delete Internet Gateways**
  - Go to the **VPC Management Console**
  - In the left navigation pane, select **Internet Gateways**
  - Select the gateway related to **dual-vpc-igw**
  - Click **Actions**, choose **Detach from VPC**, then click **Detach internet gateway**
  - Click **Actions** again, then choose **Delete internet gateway**
  - Type **delete**, then click **Delete internet gateway**

- **Delete Egress-only Internet Gateways**
  - Go to the **VPC Management Console**
  - In the left navigation pane, select **Egress-only internet gateways**
  - Select the gateway related to **dual-vpc-egw**
  - Click **Actions**, then choose **Delete egress-only internet gateway**
  - Type **delete**, then click **Delete egress-only internet gateway**

- **Delete the VPC**
  - Go to the **VPC Management Console**
  - In the left navigation pane, select **Your VPCs**
  - Select the VPC related to **my-dual-vpc**
  - Click **Actions**, then choose **Delete VPC**
  - Type **delete**, then click **Delete**

{{% notice tip %}}
When deleting a VPC, AWS will automatically delete associated resources such as: Subnets, Route Tables, Security Groups, and Internet Gateways.
{{% /notice %}}
