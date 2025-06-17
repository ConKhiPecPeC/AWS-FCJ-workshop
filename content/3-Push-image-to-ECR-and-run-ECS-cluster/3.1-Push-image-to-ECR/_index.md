---
title : "Push image to ECR"
date :  2025-05-21 
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---
Push image from local to ECR to manage and archive
1. In the **AWS Management Console** search for **Elastic Container Registry**
    ![AWS Console](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0001-AWSConsole.png)
2. On the left pannel in the **Private repositories** choose **Repositories** then choose **Create repositories**
    ![Create Repositories](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0002-CreateRepo.png)
3. In the **Create private repository**
    - Type **Repositories name**: **fcj-my-repo**
    - Kéo xuống and click **Create**
    ![Create Repositories](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0003-CreateRepo.png)
4. Push image from local to **ECR**
    - From IDE like VSCode use **AWS CLI**  **AWS configure** with IAM user create is **ECR_admin** above
    ![AWS Configure](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0004-AWSconfigure.png)
5. Back to repositories management console **ECR** choose repositories just create
    ![ECR Repositories](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0005-ECRrepositories.png)
6. Choose **View push commands**
    ![View Push Commands](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0006-ViewPushCommands.png)
7. Type commands step by step to login, build, add tag and push image to **ECR**
    ![View Push Commands](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0007-ViewPushCommands.png)
8. After uploading image to **ECR** back to **ECR repositories** 
    ![Push image](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0008-PushImage.png)
{{% notice note %}}
Copy URI of repositories has just created to use in next step
{{% /notice %}}