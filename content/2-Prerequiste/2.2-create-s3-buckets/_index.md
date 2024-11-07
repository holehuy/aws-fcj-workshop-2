---
title : "Create S3 Buckets"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Overal

Based on the architecture diagram of the lab, we need to have 4 S3 Buckets:

- Raw Email Bucket (will be created by CloudFormation)
- Staging Bucket
- Production Bucket
- Quarantine Bucket

### Create S3 buckets

1. Access the **AWS Management Console** interface:
   - Locate and click on **S3**
   - Choose **S3**

![Search S3](/images/2.prerequisite/004-search-s3.png)

2. Click **Create Bucket**

![Click Create Bucket](/images/2.prerequisite/005-create-bucket-button.png)

3. Please enter the bucket name (note that the bucket name must be unique).

![Click Create Bucket](/images/2.prerequisite/006-create-bucket-name.png)

4. Verify that all buckets are created

{{% notice info %}}
Proceed with the above steps to create all 3 S3 buckets for the lab.
{{% /notice %}}

![S3 buckets](/images/2.prerequisite/014-create-bucket.png)