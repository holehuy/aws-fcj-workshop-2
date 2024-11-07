---
title : "Verify SES domain identity"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

### Overal

To enable SES to receive emails, you need to have a domain and create a SES domain identity, followed by verifying it.

### Content

1. Access to **AWS console** -> search and choose **Amazon Simple Email Service**

2. Select **Create identity** -> Choose Identity Type **Domain**
   
3. Enter the domain you are managing along with the required information as shown in the image, and then click **Create Identity**
![Identity](/images/2.prerequisite/012-create-identity-ses.png)

4. Note that to receive emails, the DNS must be configured with an MX record for that domain. Refer to [this documentation](https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html#just-verify-domain-proc) if you are managing the domain in a DNS other than **Route53**. If the domain is managed in **Route53**, the verification process will take just a moment.

![Verified Identity](/images/2.prerequisite/013-verified-identity.png)

5. Configure the DNS MX record so that SES can receive your emails. Depending on the region you are configuring SES in, the inbound value will differ. Refer to the [documentation](https://docs.aws.amazon.com/general/latest/gr/ses.html#ses_inbound_endpoints) to get the value corresponding to your region. Here, I have selected  `ap-southest-1`

![Add MX Record](/images/4.email-receiving-solution/002-mx-record.png)
