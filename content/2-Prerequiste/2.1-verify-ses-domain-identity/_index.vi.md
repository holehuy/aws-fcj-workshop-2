---
title : "Xác thực SES domain identity"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

### Tổng quan

Để SES có thể nhận email, bạn cần có 1 domain và cần tạo một SES domain identity, sau đó verity nó.

### Nội dung

1. Đăng nhập vào **AWS console** -> search và chọn **Amazon Simple Email Service**

2. Chọn **Create identity** -> chọn Identity Type là **Domain**
   
3. Nhập domain mà bạn đang quản lý và các thông tin như hình và bấm **Create identity**

![Identity](/images/2.prerequisite/012-create-identity-ses.png)

4. Lưu ý, để nhận được email, DNS cần phải cấu hình record MX cho domain đó. Tham khảo thêm tài liệu [này](https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#just-verify-domain-proc) nếu bạn đang quản lý domain ở DNS khác mà không phải là **Route53**.
Nếu domain được quản lý ở Route53, quá trình xác thực sẽ diễn ra trong giây lát

![Verified Identity](/images/2.prerequisite/013-verified-identity.png)

5. Cấu hình DNS MX record để SES có thể nhận được email của bạn. Tuỳ theo region mà bạn đang cấu hình SES mà value inbound sẽ khác nhau. Tham khảo [tài liệu](https://docs.aws.amazon.com/general/latest/gr/ses.html#ses_inbound_endpoints) để lấy được value tương ứng với region của bạn. Ở đây mình chọn `ap-southest-1`

![Add MX Record](/images/4.email-receiving-solution/002-mx-record.png)
