## Overview
The investigated email was identified as a cryptocurrency themed phishing attempt designed to convince the recipient they had an available Bitcoin balance of 0.7495 BTC (~$15,661). The attacker used a fraudulent PDF attachment and a Bitly‑shortened URL to redirect victims to external scam infrastructure. Although the message passed all authentication checks (SPF, DKIM, DMARC), the financial lure, urgency, and suspicious attachment clearly indicated malicious intent.

---

## Threat Summary
The attacker delivered the phishing email through a legitimate Gmail account, leveraging trusted cloud infrastructure to bypass filtering controls. The email used a high value financial lure and a 24‑hour urgency deadline to pressure the victim into opening the attached PDF. The PDF contained a large embedded image mimicking a Bitcoin balance statement and included a Bitly shortened URL redirecting users to suspicious external infrastructure.

The attack relied entirely on social engineering, not malware. No exploit code or malicious payloads were present. The attacker’s objective was to steal cryptocurrency, credentials, or payment information by tricking the user into interacting with the fake withdrawal site.

---

## Key Findings
- SPF, DKIM, and DMARC authentication successfully passed
- Sender leveraged legitimate Gmail infrastructure
- Email used a cryptocurrency‑themed financial lure
- PDF attachment contained phishing and scam related content
- Embedded Bitly URL redirected to suspicious external infrastructure
- No malware execution behavior was identified
- VirusTotal and Hybrid Analysis classified the PDF as phishing/scam
- Attack relied on user execution, not technical exploitation

---

## Risk Assessment
Severity: High
Impact: High
Likelihood: High

This phishing attempt poses a high security risk due to its strong social engineering lure, financial fraud potential, and use of trusted infrastructure.

- Successful user interaction could result in cryptocurrency theft, credential compromise, or unauthorized access to financial accounts.

Because the PDF is clean and non‑malicious, it is more likely to bypass security controls and be opened by unsuspecting users. The organizational risk includes financial loss, credential compromise, and further targeted phishing attempts.

---

## Final Determination
Based on header analysis, infrastructure investigation, URL analysis, and attachment assessment, the email was determined to be a malicious phishing attempt designed to redirect victims to a fraudulent cryptocurrency withdrawal portal. The primary threat vector was social engineering via a PDF attachment and a Bitly shortened URL.

---

## Recommendations
- - Block the shortened phishing redirect URL: hxxps://bit[.]ly/3V8v9ku
- Warn users about cryptocurrency‑themed phishing scams
- Monitor for additional emails from the sender address and similar lures
- Enhance email filtering to flag financial‑lure PDFs and URL shorteners
- Implement attachment sandboxing for PDF files from external senders
- Educate users on the risks of shortened URLs and unsolicited financial claims
- Review logs for any user interactions with the Bitly link