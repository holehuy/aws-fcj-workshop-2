+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

### Empty các S3 Bucket

Truy cập [giao diện quản trị dịch vụ S3](https://console.aws.amazon.com/s3/home)
  + Chọn S3 Bucket cần empty
  + Click button **Empty**
  + Xác nhận

### Disable email rule set

Truy cập [giao diện quản trị dịch vụ SES](https://console.aws.amazon.com/ses/home)
  + Click **Email Receiving**.
  + Chọn rule set
  + Chọn Set as inactive
  + Xác nhận
  
![In Active rule set](/images/5-cleanup/001-inactive-rule-set.png)

### Xoá CloudFormation Stack

Truy cập [giao diện quản trị dịch vụ CloudFormation](https://console.aws.amazon.com/cloudformation/home)
  - Chọn Stack cần xoá
  - Click **Delete**

![Delete Stacks](/images/5-cleanup/002-delete-stacks.png)

![Delete Stack](/images/5-cleanup/003-delete-stacks.png)
