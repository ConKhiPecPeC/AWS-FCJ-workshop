---
title : "Giới thiệu"
date :  2025-05-21 
weight : 1
chapter : false
pre : " <b> 1. </b> "
---

**VPC Dual Stack** Ngày càng có nhiều tổ chức áp dụng IPv6 trong môi trường của họ, do không gian IPv4 công cộng cạn kiệt, IPv4 riêng tư khan hiếm, đặc biệt là trong các mạng quy mô lớn và nhu cầu cung cấp dịch vụ khả dụng cho các máy khách chỉ sử dụng IPv6. Một bước trung gian trên con đường hỗ trợ đầy đủ IPv6 là thiết kế IPv4/IPv6 dual-stack, tận dụng cả hai phiên bản của giao thức IP song song.
   ![VPC Dual Stack](/images/1-Introduction/0001_DualStackVPC.png)

**Amazon Elastic Container Registry (Amazon ECR)** là một dịch vụ lưu trữ hình ảnh container (container image registry) được AWS quản lý, đảm bảo tính bảo mật, khả năng mở rộng và độ tin cậy cao. **Amazon ECR** hỗ trợ các kho lưu trữ riêng tư (private repositories) với quyền truy cập dựa trên tài nguyên, sử dụng AWS IAM. Nhờ đó, bạn có thể chỉ định người dùng hoặc các phiên bản Amazon EC2 cụ thể được phép truy cập vào kho lưu trữ và các hình ảnh container của bạn.
Bạn có thể sử dụng công cụ dòng lệnh (CLI) ưa thích của mình để đẩy (push), kéo (pull) và quản lý các Docker image, image theo tiêu chuẩn Open Container Initiative (OCI), cũng như các đối tượng tương thích với OCI.
   ![ECR](/images/1-Introduction/0002_ECR_icon.png)

**Amazon Elastic Container Service (Amazon ECS)** là một dịch vụ điều phối container được quản lý hoàn toàn, giúp bạn dễ dàng triển khai, quản lý và mở rộng các ứng dụng được đóng gói dưới dạng container. Là một dịch vụ được quản lý hoàn toàn, Amazon ECS tích hợp sẵn các cấu hình và thực tiễn vận hành tốt nhất từ AWS.
Dịch vụ này được tích hợp với cả các công cụ của AWS như **Amazon Elastic Container Registry**, cũng như các công cụ của bên thứ ba như Docker. Sự tích hợp này giúp các nhóm phát triển tập trung vào việc xây dựng ứng dụng, thay vì phải lo lắng về môi trường vận hành. Bạn có thể chạy và mở rộng khối lượng công việc container của mình trên các vùng (Region) của AWS trong đám mây hoặc tại chỗ (on-premises) mà không cần phải quản lý mặt phức tạp của một mặt phẳng điều khiển (control plane). 
   ![ECS](/images/1-Introduction/0003_ECS_icon.png)

**Amazon Route 53** là dịch vụ web Hệ thống tên miền (DNS) có khả năng mở rộng và tính khả dụng cao. Bạn có thể sử dụng Route 53 để thực hiện ba chức năng chính theo bất kỳ sự kết hợp nào: đăng ký tên miền, định tuyến DNS và kiểm tra tình trạng.
Các tính năng của Route53
- Route 53 Resolver
- Amazon Route 53 Resolver trên Outposts
- Tường lửa DNS Route 53 Resolver
- Traffic Flow
- Amazon Route 53 Profiles