---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

### Malware and Amazon S3

When working with AWS, we often run various types of workloads, including [Amazon Simple Storage Service](https://aws.amazon.com/vi/s3/) (S3), a highly durable and scalable object storage service used for storing and processing data, including critical information.

Protecting data from malware uploaded to S3 is a crucial task that businesses may require. The challenging aspect of handling malware is not the scanning process itself, but rather the ability to quickly detect malware and respond in a timely manner.

[Trend Micro](http://www.trendmicro.com/aws) can be integrated into this process to alert users about malware. We can combine it with [AWS Security Hub](https://aws.amazon.com/security-hub/) for centralized management and to take remediation actions, such as isolating malware, blocking IP addresses, or restricting access for violating users.

### Malware and Email Attachments

In today's business environment, receiving and processing emails is also very important. Not only can users send emails, but Amazon SES also allows them to set rules for receiving and automatically processing emails.

Automating the email processing workflow enhances productivity and can be applied to various business scenarios (such as automatically importing data through attachments or categorizing emails).

We also need a solution to protect customers and systems from emails containing malware. In addition to AWS's built-in malware scanning capabilities in SES email receiving rules, this lab introduces another method: storing emails in S3 and using Trend Micro to scan the attachments.

### Trend Micro Cloud One

[Trend Micro](http://www.trendmicro.com/aws) is an AWS partner in the security domain. [Trend Micro Cloud One](https://cloudone.trendmicro.com/) is a security services platform for the cloud, enabling AWS customers to secure cloud workloads easily and simply.

![Diagram](/images/1.introduce/trend-micro-services.png) 

[Cloud One File Storage Security](https://cloudone.trendmicro.com/docs/file-storage-security/what-is-fss/) is one of the security services within Trend Micro Cloud One. **File Storage Security** protects workflows by using event-driven scanning functions, such as malware scanning, integrated into your custom workflows, and supports multiple cloud storage platforms, not just AWS.