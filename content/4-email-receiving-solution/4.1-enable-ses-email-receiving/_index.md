---
title : "Enable SES email receiving"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Enable Email Receiving và giải pháp extract email attachments bằng Lambda Function

![Diagram](/images/4.email-receiving-solution/001-diagram.png)

Based on the diagram above, we will deploy a CloudFormation stack to deploy the system.

{{% notice info %}}
Note, you must complete the request in the preparation step (verify SES domain identity) to be able to perform this practice part.
{{% /notice %}}

1. Access [Link](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/quickcreate?templateURL=https://cfn-template-hlhuy.s3.ap-southeast-1.amazonaws.com/template-ses-receiving-email.yml&stackName=SESReceivingEmail) to create CloudFormation Stack.

2. Fill in the necessary information:
   - **AttachmentBucketARN**: specifies an S3 bucket for the lambda function to extract attachments and store them in. In this case, the RNA of the **Staging Bucket**
   - **EmailRecipient**: specifies the email address and attachments. For example `receiver@example.com`

![Create Stack](/images/4.email-receiving-solution/003-create-stack.png)
 
3. Check the **I acknowledge ...** box and click the **Create Stack** button

![Acknowledged](/images/4.email-receiving-solution/004-acknowledge.png)

4. After the Stack is successfully created, the detailed screen is as follows:

![Detail](/images/4.email-receiving-solution/005-stack-overview.png)
An S3 bucket to store raw emails will be created.

![Raw bucket](/images/4.email-receiving-solution/008-output.png)

5. Enable Email receiving rule set
- Access the SES console screen
- Go to the **Email receiving** tab in the **Configuration** section
- Check the rule set and **Set as active**

![Enable rule set](/images/4.email-receiving-solution/006-enable-rule-set.png)

6. Check raw email bucket
- ​​Access S3 and select the Bucket created in (4)
- If there is an object **AMAZON_SES_SETUP_NOTIFICATION** then we have basically successfully configured SES Email Receiving

![Checking](/images/4.email-receiving-solution/007-checking.png)