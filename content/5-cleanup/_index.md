+++
title = "Clean up resources"
date = 2022
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

We will take the following steps to delete the resources we created in this exercise.

### Empty S3 Buckets

Go to [S3 service admin interface](https://console.aws.amazon.com/s3/home)
- Select S3 Bucket to empty
- Click **Empty** button
- Confirm

### Disable email rule set

Go to [SES service management interface](https://console.aws.amazon.com/ses/home)
- Click **Email Receiving**.
- Select rule set
- Select Set as inactive
- Confirm
  
![In Active rule set](/images/5-cleanup/001-inactive-rule-set.png)

### Xoá CloudFormation Stack

Go to [CloudFormation service management interface](https://console.aws.amazon.com/cloudformation/home)
- Select the Stack to delete
- Click **Delete**

![Delete Stacks](/images/5-cleanup/002-delete-stacks.png)

![Delete Stack](/images/5-cleanup/003-delete-stacks.png)
