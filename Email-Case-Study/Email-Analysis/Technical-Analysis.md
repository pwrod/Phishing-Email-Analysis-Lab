# Technical Analysis

## Email Metadata
- Subject: GO.Get.Bitcoin.0.7495.BTC
- Sender: Shanti Denker <michelleleeoma7@gmail.com>
- Recipient: kevin031982@yahoo.com
- Message-ID: <CAN3R5gNyH1sZMDbYkKQJNwY+trdZ-ERZ4JpMKOynO13NftK4Yg@mail.gmail.com>
- Return-Path: michelleleeoma7@gmail.com
- Date: Sun, 25 Dec 2022 20:12:53 -0800

---

## Header Analysis
### SPF Analysis
SPF authentication passed, indicating the email was sent from infrastructure authorized by the sending domain.
### DKIM Analysis

DKIM validation passed, confirming the message contents were cryptographically signed and were not altered during transit.
### DMARC Analysis
DMARC validation passed due to alignment between the authenticated domain and the visible sender domain.

Although all authentication mechanisms passed, the email was still identified as malicious. This demonstrates that phishing campaigns can abuse legitimate email infrastructure and valid authentication mechanisms.
### Mail Routing: Originates from Gmail web, then via Google SMTP, then Microsoft protection, then internal Exchange

---

## Sender Infrastructure Analysis
The sender IP address belongs to Google LLC infrastructure associated with Gmail mail transfer agents.

No malicious reputation indicators were identified for the originating infrastructure itself. This suggests the phishing email was distributed through a legitimate Gmail account rather than attacker-controlled mail servers.

This technique helps attackers evade reputation-based filtering by abusing trusted cloud email providers.

---

## Anti-Spam Analysis
- Spam score: X-MS-Exchange-Organization-SCL: 5 (Likely spam)
Despite passing SPF, DKIM, and DMARC validation, behavioral and content-based indicators likely contributed to the elevated spam score.

---

## Plaintext Body Analysis
- Body Text: Withdraw your 15,661$, have only 24 hours
and Professor Dumbledore.
The email used a cryptocurrency-themed financial lure claiming the recipient could withdraw a large Bitcoin balance.

The message incorporated urgency by imposing a 24-hour deadline, a common social engineering tactic designed to pressure recipients into acting before evaluating legitimacy.

The inclusion of "Professor Dumbledore" appears nonsensical and may indicate automated spam generation or an attempt to bypass content-based spam filters.

---

## URL Analysis

The email contained a Bitly-shortened URL:

- hxxps://bit[.]ly/3V8v9ku

URL analysis revealed the shortened link redirected to a cryptocurrency-themed scam website.

The use of URL shortening services helps attackers obscure final destinations and evade user suspicion.

---

## Attachment Analysis
| Attribute | Value |
| --- | --- |
| **Filename** | ``Bitcoin.Balance.0.7495.BTC6BbPOzRwkSNiLISGdqP0N.pdf`` |
| **SHA256** | ``f1d70491c74c768986139ea2bab8441de7e5681b3409f85d0b265b6230a1a0e4`` |
| **VirusTotal Report** | [View Analysis](https://www.virustotal.com/gui/file/f1d70491c74c768986139ea2bab8441de7e5681b3409f85d0b265b6230a1a0e4) |
| **Hybrid Analysis Report** | [View Sandbox Report](http://hybrid-analysis.com/sample/f1d70491c74c768986139ea2bab8441de7e5681b3409f85d0b265b6230a1a0e4) |
| **Type** | PDF (``%PDF-1.3``) |
| **Pages** | 11 |
| **Content** | One embedded JPEG image (social‑engineering content) |

-Behaviorial Analysis: Classified as phishing/scam PDF, no exploit behavior, redirected users to a suspicious cryptocurrency-themed website, designed for financial fraud, not malware delivery

-Structural Analysis: No JavaScript, no embedded executables, no launch actions, no encryption, and one large JPEG image (fake Bitcoin balance)

---

## Indicators of Compromise
| IOC Type | Value | Description |
|---|---|---|
| URL | hxxps://bit[.]ly/3V8v9ku | Phishing redirect URL |
| SHA256 | f1d70491c74... | PDF attachment hash |
| Email Address | michelleleeoma7@gmail[.]com | Sender address |

---
## MITRE ATT&CK MAPPING
| Technique ID | Name | Reason |
| --- | --- | --- |
| **T1566** | Phishing | Email lure promising Bitcoin withdrawal |
| **T1566.002** | Spearphishing via Service | Delivered via Gmail |
| **T1204** | User Execution | Requires user to open PDF and click link |
| **T1598** | Phishing for Information | Attempts to steal crypto credentials or money |
| **T1583.006** | Acquire Infrastructure: Web Services | Use of Gmail + Bitly as attacker infrastructure |
---
## Risk Assessment
- Severity: High (High‑value financial lure + malicious redirect + scam PDF. High potential for financial loss.)
- Impact: High (Irreversible financial transactions)
- Likelihood: High