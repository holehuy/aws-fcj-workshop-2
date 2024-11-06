---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

### Malware và Amazon S3

Khi làm việc với AWS, chúng ta thường chạy nhiều loại khối lượng công việc khác nhau, trong đó có [Amazon Simple Storage Service](https://aws.amazon.com/vi/s3/) (S3), một dịch vụ lưu trữ object có độ bền cao, có khả năng mở rộng cao để lưu trữ và xử lý các dữ liệu (có cả dữ liệu quan trọng).

Việc bảo vệ dữ liệu khỏi các phần mềm độc hại được tải lên S3 là một công việc quan trọng mà các doanh nghiệp có thể yêu cầu. Công việc khó khăn khi xử lý phần mềm độc hai không phải là quá trình quét (scanning) mà là phải phát hiện phần mềm độc hại mộc cách nhanh chóng và xử lý một cách kịp thời. 

[Trend Micro](http://www.trendmicro.com/aws) có thể được tích hợp trong quá trình này để cảnh báo phần mềm độc hại. Chúng ta có thể kết hợp với [AWS Security Hub](https://aws.amazon.com/security-hub/) để có thể quản lý tập trung và thực hiện các hành động khắc phục (chẳng hạn như cách ly phần mềm độc hại, chặn địa chỉ IP, hoặc người dùng vi phạm, ...)

### Malware và Email Attachments

Trong môi trường kinh doanh hiện đại, việc nhận và xử lý email cũng rất quan trọng. Không chỉ có thể gửi email, SES còn cho phép người dùng thiết lập các quy tắc để nhận email và xử lý tự động.

Tự động hóa quy trình xử lý email giúp tăng cường năng suất làm việc, áp dụng được cho nhiều business thực tế (tự động import data thông qua attachments, tự động phân loại email, ...)

Và chúng ta cũng cần giải pháp để có thể bảo vệ khách hàng và hệ thống khỏi các email có chứa malware. Ngoài khả năng scan malware đã được AWS giới thiệu trong SES email receiving rule, bài lab này còn giới thiệu một phương pháp khác đó là lưu trữ email ở S3 và sử dụng Trend Micro để quét các tệp đính kèm trong email.

### Trend Micro Cloud One

[Trend Micro](http://www.trendmicro.com/aws) là một Partner của AWS trong lĩnh vực bảo mật. [Trend Micro Cloud One](https://cloudone.trendmicro.com/) là nền tảng dịch vụ bảo mật dành cho cloud, cho phép khách hàng AWS bảo mật khối lượng công việc trên cloud một cách dễ dàng và đơn giản.

![Diagram](/images/1.introduce/trend-micro-services.png) 

[Cloud One File Storage Security](https://cloudone.trendmicro.com/docs/file-storage-security/what-is-fss/) là một trong những dịch vụ bảo mật trong Trend Micro Cloud One. **File Storage Security** bảo vệ quy trình làm việc bằng cách sử dụng chức năng quét theo event, chẳng hạn như quét phần mềm độc hại, tích hợp vào quy trình làm việc tùy chỉnh của bạn và hỗ trợ nhiều nền tảng lưu trữ đám mây chứ không chỉ riêng với AWS.



