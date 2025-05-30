---
title : "Tạo IAM user và IAM role"
date :  2025-05-21 
weight : 2
chapter : false
pre : " <b> 2.1 </b> "
---

#### Tạo IAM user
Tạo user và cấp quyền để có thể push image từ máy local lên ECR
1. Đăng nhập vào **IAM Management Console**
    ![IAM Management Console](/images/2-Setup-Resource/2.1-Create-IAM/0001-IAM_console.png)
2.  Tại thanh bên trái chọn **Users** rồi chọn **Create user**
    ![Tạo useruser](/images/2-Setup-Resource/2.1-Create-IAM/0002-CreateUser.png)
3. Tại trang **Specify user details**
   - Nhập User name: **ECR_admin**
   - Ấn **Next**
    ![Tạo useruser](/images/2-Setup-Resource/2.1-Create-IAM/0003-Username.png)
4. Tại trang **Set permissions**
   - Trong phần **Permissions options** chọn **Attach policies directly**
   - Trong phần **Permissions policies** điền **AmazonEC2ContainerRegistryFullAccess** sau đó tích chọn
   - Sau đó ấn **Next**
    ![User Permission](/images/2-Setup-Resource/2.1-Create-IAM/0004-UserPermission.png)
5. Tại trang **Review and create**
    - Chọn **Create User**
    ![Tạo User](/images/2-Setup-Resource/2.1-Create-IAM/0005-CreateUser.png)
6. Quay lại **IAM Management Console** và chọn user vừa tạo
    ![Chọn User](/images/2-Setup-Resource/2.1-Create-IAM/0006-ChoseUser.png)
7. Tạo access key 
    - Trong trang quản lý user chọn **Security credentials**
    - Trong phần **Access Key** chọn **Create access key**
    - Tại trang **Access key best practices & alternatives** trong phần **Use case** chọn **Command Line Interface (CLI)**
    - Kéo xuống ấn tích trong phần **Confirmation** và ấn **Next**
    - Chọn **Create access key**
    ![CLI Access KeyKey](/images/2-Setup-Resource/2.1-Create-IAM/0007-AccessKeyCLI.png)
8. Tải Access Key 
    - Chọn **Download .csv file** hoặc có thể copy **Access Key** và **Secret access key** và lưu trữ trong các trình lưu trữ văn bản như Notepad
    - Chọn **Done**
    ![Download Access KeyKey](/images/2-Setup-Resource/2.1-Create-IAM/0008-SaveAccessKey.png)

#### Tạo IAM role
1. Quay lại **IAM Management Console**
2. Tại thanh bên trái chọn **Role** rồi chọn **Create Role**
    ![Create Role](/images/2-Setup-Resource/2.1-Create-IAM/0009-IAMconsole-role.png)
3. Tại trang **Select trusted entity**
    - Trong phần **Trusted entity type** chọn **AWS Service**
    ![Role Type](/images/2-Setup-Resource/2.1-Create-IAM/0010-RoleType.png)
    - Kéo xuống trong phần **Use case**
    - Nhập **Elastic Container Service** trong **Service or use case**
    - Chọn **Elastic Container Service Task** và ấn **Next** 
    ![Role UseCase](/images/2-Setup-Resource/2.1-Create-IAM/0011-RoleUseCase.png)
4. Trong phần **Add permissions**
    - Nhập **AmazonECSTaskExecutionRolePolicy** vào thanh tìm kiếm 
    - Tích chọn policy và ấn **Next**
    ![Role Permission](/images/2-Setup-Resource/2.1-Create-IAM/0012-RolePermission.png)
5. Trong phần **Name, review, and create**
    - Tại ô **Role name** nhập **ECS-TaksExecute**
    - Kéo xuống chọn **Create Role**
    ![IAM role create](/images/2-Setup-Resource/2.1-Create-IAM/0013-IAMroleCreate.png)
