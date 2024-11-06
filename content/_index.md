---
title : "Email Receiving with Amazon SES & S3 Malware Scanning"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Email Receiving with Amazon SES & S3 Malware Scanning via Trend Micro Cloud One

### Overall
In this lab, we will explore the process of receiving emails using **[Amazon Simple Email Service](https://aws.amazon.com/ses/)** and storing them in **[Amazon S3](https://aws.amazon.com/vi/s3/)**. Additionally, we will set up a malware scanning workflow for email attachments using **[Trend Micro Cloud One](http://www.trendmicro.com/aws)**.

![ConnectPrivate](/images/diagram.png) 

### Objectives

1. **Setup Amazon SES Receiving Email** - Configure SES to receive emails from a verified domain (identity).
2. **Store emails in Amazon S3** - Set up an S3 bucket to store the received emails.
3. **Extract email's attachments using Lambda Function** - Configure S3 event trigger Lambda Function to process attachments.
4. **Scan for Malware with Trend Micro Cloud One** - Integrate a malware scanning solution to protect data from potential threats.

### Content

{{% children  %}}