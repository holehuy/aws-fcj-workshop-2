---
title : "Nhận Email với Amazon SES & Quét Malware trên S3 bằng Trend Micro Cloud One"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Nhận Email với Amazon SES & Quét Malware trên S3 bằng Trend Micro Cloud One

### Tổng quan

Trong bài lab này, chúng ta sẽ khám phá cách thức nhận email sử dụng **[Amazon Simple Email Service](https://aws.amazon.com/vi/ses/)** và lưu trữ chúng trên **[Amazon S3](https://aws.amazon.com/vi/s3/)**. Bên cạnh đó, chúng ta sẽ thiết lập quy trình quét malware cho các tệp đính kèm email bằng giải pháp **[Trend Micro Cloud One](http://www.trendmicro.com/aws)**.

![ConnectPrivate](/images/diagram.png) 

### Mục tiêu

1. **Thiết lập Amazon SES Receiving Email** - Tạo và cấu hình dịch vụ SES để nhận email từ domain đã xác minh.
2. **Lưu trữ và xử lý Email trên S3** -  Thiết lập S3 bucket để lưu trữ các email nhận được.
3. **Extract tệp đính kèm bằng Lambda Function** - Thiết lập S3 event để trigger các Lambda Function xử lý các tệp đính kèm.
4. **Quét malware với Trend Micro Cloud One** - Tích hợp dịch vụ quét malware để bảo vệ dữ liệu khỏi các mối đe doạ tiềm ẩn. 


### Nội dung

{{% children  %}}