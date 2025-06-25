# Task-2-phishing-email-analysis
* analyze a sample phishing email and identify characteristics that indicate its a phishing attempt

# Supicious Email sample 

From: Divya Singh - Suzuki <info@sportzcontests.com>  
To: Sumit Tadavi <sumit13rocks@gmail.com>  
Subject: Your request has been accepted by Suzuki!

Hi Sumit Tadavi,

Suzuki this Side!

Please click here to complete your Application.  
just a few minutes.

Please contact me at the earliest.

Click Here To Contact

Regards,  
Divya Singh


# Phishing Indicators (contend based)

* Misleading Sender Name
  Email claims to be from "Suzuki", but domain is @sportzcontests.com,which is unrelated to Suzuki

* Suspicious call to action
  "Click here to complete the application" is vague and has no context. Link destination is hidden

* Poor grammer and language
  Phrases like "Suzuki this side" and lowercase "just a few minutes" show unprofessional grammer

* Urgency without context
  "Please contact me at the earliest" adds pressure without explining why

* Unexpected email
  Your weren't expecting any application response form Suzuki. Tjis is a read flag

* Impersonation Risk
  The name "Suzuki" is used to trick user into trusting the source
  
# Header Analysis (Technical Indicators)

* DMARC (Domain-based Message Authentication, Reporting, and Conformance)
  DMARC works alongside SPF (Sender Policy Framework) and DKIM (DomainKeys Identified Mail) to verify that incoming emails claiming to be from your domain are actually authorized. If an email fails these checks,    DMARC tells the receiving server what to do.
  *DMARC FAILURE "did not validate possiable spoofing"
  
* DKIM  (Domain Key Identifield Mail)
  This field shows what different kind of authentication is required to identify an email whether the email that has send to us by the sender is the authanticated version or it has been tempared with
  *DKIM failure "not configured or signature not verified integrity of message can't be trusted"
  
# Tools That Can Be Used 

* MxToolbox Header Analyzer
* Google Admin Toolbox – Messageheader
* Mailheader.org
  I have use Mxtoolbox to identify wether this email is spam email or not while analysising the header part

# Mitigation Strategies
 For Individuals:
* Don't click on suspicious links.
* Verify the sender by contacting the company directly.
* Report the phishing email using your email client's “Report Phishing” option.
* Enable Multi-Factor Authentication (MFA).

Submitted by : Sumit Tadavi
 For Organizations:
* Use DMARC, SPF, and DKIM to prevent spoofing.
* Deploy email security gateways to filter phishing emails.
* Conduct regular security awareness training with phishing simulations.
* Log and monitor suspicious email activity.
     
