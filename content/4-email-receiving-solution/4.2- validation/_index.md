---
title : "Validation"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

### Validate

1. Send an email with an attachment to the recipient email address configured in the previous step.
![Send Mail](/images/4.email-receiving-solution/009-send-mail-test.png)
2. If the attachment is not malware, after scanning, the file will be stored in **Production Bucket**. Otherwise, the file will be quarantined in **Quarantine Bucket**.
![Production Object](/images/4.email-receiving-solution/010-production.png)

![Tags Object](/images/4.email-receiving-solution/011-tags.png)
