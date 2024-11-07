---
title : "Validation"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

### Kiểm tra

1. Gửi 1 email có tệp tin đính kèm tới địa chỉ email receiver đã cấu hình ở bước trước
![Send Mail](/images/4.email-receiving-solution/009-send-mail-test.png)
2. Nếu tệp tin đính kèm không phải là malware, sau quá trình scanning, tệp tin sẽ được lưu trữ ở **Production Bucket**. Ngược lại, tệp tin sẽ bị cách ly ở **Quarantine Bucket**.
![Production Object](/images/4.email-receiving-solution/010-production.png)

![Tags Object](/images/4.email-receiving-solution/011-tags.png)




