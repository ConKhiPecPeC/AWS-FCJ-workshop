---
title : "Create IAM user and IAM role"
date :  2025-05-21 
weight : 2
chapter : false
pre : " <b> 2.1 </b> "
---
#### Create IAM user
Create a user and grant permissions to push images from your local machine to ECR.
1. Log in to the **IAM Management Console**
    ![IAM Management Console](/images/2-Setup-Resource/2.1-Create-IAM/0001-IAM_console.png)
2. In the left sidebar, select **Users** then click **Create user**
    ![Tạo useruser](/images/2-Setup-Resource/2.1-Create-IAM/0002-CreateUser.png)
3. On **Specify user details**
   - Type User name: **ECR_admin**
   - Click **Next**
    ![Tạo useruser](/images/2-Setup-Resource/2.1-Create-IAM/0003-Username.png)
4. On **Set permissions**
   - Under **Permissions options** choose **Attach policies directly**
   - In **Permissions policies** search fo **AmazonEC2ContainerRegistryFullAccess** and select it
   - Then click **Next**
    ![User Permission](/images/2-Setup-Resource/2.1-Create-IAM/0004-UserPermission.png)
5. On **Review and create**
    - Click **Create User**
    ![Tạo User](/images/2-Setup-Resource/2.1-Create-IAM/0005-CreateUser.png)
6. Return to the **IAM Management Console** and select the newly created user
    ![Chọn User](/images/2-Setup-Resource/2.1-Create-IAM/0006-ChoseUser.png)
7. Create an access key
    - On the user's management page, go to **Security credentials**
    - Under **Access Key** click **Create access key**
    - On the **Access key best practices & alternatives** in **Use case** choose **Command Line Interface (CLI)**
    - Scroll down, check the **Confirmation** click **Next**
    - Click **Create access key**
    ![CLI Access KeyKey](/images/2-Setup-Resource/2.1-Create-IAM/0007-AccessKeyCLI.png)
8. Download the access key 
    - Choose **Download .csv file** or copy **Access Key** and **Secret access key** and store them in a secure text editor like Notepad
    - Click **Done**
    ![Download Access KeyKey](/images/2-Setup-Resource/2.1-Create-IAM/0008-SaveAccessKey.png)

#### Create IAM role
1. Return to the **IAM Management Console**
2. In the left sidebar select **Role** then click **Create Role**
    ![Create Role](/images/2-Setup-Resource/2.1-Create-IAM/0009-IAMconsole-role.png)
3. On **Select trusted entity**
    - Under **Trusted entity type** choose **AWS Service**
    ![Role Type](/images/2-Setup-Resource/2.1-Create-IAM/0010-RoleType.png)
    - Scroll down to the **Use case**
    - Enter **Elastic Container Service** in **Service or use case**
    - Choose **Elastic Container Service Task** click **Next** 
    ![Role UseCase](/images/2-Setup-Resource/2.1-Create-IAM/0011-RoleUseCase.png)
4. In the **Add permissions**
    - Search for **AmazonECSTaskExecutionRolePolicy** 
    - Check the policy and click **Next**
    ![Role Permission](/images/2-Setup-Resource/2.1-Create-IAM/0012-RolePermission.png)
5. In the **Name, review, and create**
    - In **Role name** type **ECS-TaksExecute**
    - Scroll down and click **Create Role**
    ![IAM role create](/images/2-Setup-Resource/2.1-Create-IAM/0013-IAMroleCreate.png)
