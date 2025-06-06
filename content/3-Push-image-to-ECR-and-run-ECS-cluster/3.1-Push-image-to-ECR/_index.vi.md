---
title : "Push image lên ECR"
date :  2025-05-21 
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---
Tiến hành push 1 image từ máy local lên ECR để quản lý và lưu trữ
1. Tại **AWS Management Console** tìm **Elastic Container Registry**
    ![AWS Console](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0001-AWSConsole.png)
2. Tại thanh bên trái trong phần **Private repositories** chọn **Repositories** rồi chọn **Create repositories**
    ![Create Repositories](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0002-CreateRepo.png)
3. Tại **Create private repository**
    - Nhập **Repositories name** là **fcj-my-repo**
    - Kéo xuống và ấn **Create**
    ![Create Repositories](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0003-CreateRepo.png)
4. Push image từ local lên **ECR**
    - Từ IDE như VS Code tiến hành **AWS configure** với IAM user đã tạo là **ECR_admin** ở trên
    ![AWS Configure](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0004-AWSconfigure.png)
5. Quay lại trang quản lý reposirories của **ECR** chọn vào repositories vừa tạo
    ![ECR Repositories](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0005-ECRrepositories.png)
6. Chọn **View push commands**
    ![View Push Commands](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0006-ViewPushCommands.png)
7. Thực hiện theo thứ tự các bước để login, build, gắn tag và push image lên **ECR**
    ![View Push Commands](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0007-ViewPushCommands.png)
8. Sau khi hoàn tất việc push image lên **ECR** quay lại **ECR repositories** 
    ![Push image](/images/3-Push-image-to-ECR-and-run-ECS-cluster/3.1-Push-image-to-ECR/0008-PushImage.png)
{{% notice note %}}
Copy URI của repositories vừa tạo để sử dụng trong việc khai báo ở bước tiếp theo
{{% /notice %}}