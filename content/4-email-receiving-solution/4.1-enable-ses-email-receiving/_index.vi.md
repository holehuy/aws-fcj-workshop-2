---
title : "Enable SES email receiving"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Enable Email Receiving và giải pháp extract email attachments bằng Lambda Function

![Diagram](/images/4.email-receiving-solution/001-diagram.png)

Dựa vào sơ đồ trên, chúng ta sẽ tiến hành deploy một CloudFormation stack để triển khai hệ thống. 

{{% notice info %}}
Lưu ý, bạn phải thực hiện yêu cầu ở bước chuẩn bị (verify SES domain identity) để có thể thực hiện phần thực hành này.
{{% /notice %}}

1. Truy cập [Link](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/quickcreate?templateURL=https://cfn-template-hlhuy.s3.ap-southeast-1.amazonaws.com/template-ses-receiving-email.yml&stackName=SESReceivingEmail) để có thể tạo CloudFormation stack.
2. Điền các thông tin cần thiết:
   - **AttachmentBucketARN**: chỉ định S3 bucket để lambda function extract các tệp đính kèm và lưu trữ vào. Trong trường hợp này là ARN của **Staging Bucket**
   - **EmailRecipient**: chỉ định địa chỉ nhận mail và các tệp đính kèm. Ví dụ `receiver@example.com`

![Create Stack](/images/4.email-receiving-solution/003-create-stack.png)
 
3. Check vào ô **I acknowledge ...** và click button **Create Stack**

![Acknowledged](/images/4.email-receiving-solution/004-acknowledge.png)

4. Sau khi Stack được tạo thành công, màn hình chi tiết như sau:

![Detail](/images/4.email-receiving-solution/005-stack-overview.png)
Một S3 bucket để lưu trữ raw email sẽ được tạo ra

![Raw bucket](/images/4.email-receiving-solution/008-output.png)

5. Enable Email receiving rule set
- Truy cập vào màn hình SES console
- Vào tab **Email receiving** trong phần **Configuration**
- Check chọn rule set và **Set as active**

![Enable rule set](/images/4.email-receiving-solution/006-enable-rule-set.png)

6. Kiểm tra raw email bucket
   - Truy cập vào S3 và chọn Bucket được tạo ở (4)
   - Nếu có object **AMAZON_SES_SETUP_NOTIFICATION** thì căn bản chúng ta đã thành công cấu hình SES Email Receiving

![Checking](/images/4.email-receiving-solution/007-checking.png)