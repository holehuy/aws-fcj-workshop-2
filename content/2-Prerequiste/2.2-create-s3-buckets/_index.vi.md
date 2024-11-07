---
title : "Tạo các S3 Bucket"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Tổng quan

Dựa theo sơ đồ kiến trúc của bài lab, chúng ta cần có 4 S3 Bucket:
   - Raw Email Bucket (Bucket này sẽ được tạo bằng CloudFormation)
   - Staging Bucket
   - Production Bucket
   - Quarantine bucket

### Tạo S3 bucket

1. Truy cập giao diện **AWS Management Console**:
   - Tìm **S3**
   - Chọn **S3**

![Search S3](/images/2.prerequisite/004-search-s3.png)

2. Click **Create Bucket**

![Click Create Bucket](/images/2.prerequisite/005-create-bucket-button.png)

3. Nhập tên bucket (lưu ý, tên bucket phải là duy nhất)

![Click Create Bucket](/images/2.prerequisite/006-create-bucket-name.png)

4. Cần chắc chắn rằng tất cả các Bucket đã được tạo

{{% notice info %}}
Tiến hành thao tác trên để tạo đủ 3 S3 bucket phục vụ cho bài lab.
{{% /notice %}}

![S3 buckets](/images/2.prerequisite/014-create-bucket.png)