# Phishing Email Analysis Lab
This project documents the analysis of a phishing email obtained from the PhishingPot repository. The investigation focused on email header analysis, authentication validation, attachment analysis, URL investigation, and indicator extraction to determine the nature and objectives of the phishing campaign.

---

## Objectives

- Analyze email headers
- Validate SPF, DKIM, and DMARC
- Identify sender infrastructure
- Examine phishing content
- Analyze malicious attachments
- Extract indicators of compromise (IOCs)
- Document findings in a structured report

---

## Investigation Summary

The analyzed email used a cryptocurrency themed lure claiming the recipient could withdraw Bitcoin. The message originated from a legitimate Gmail account and passed SPF, DKIM, and DMARC authentication checks. Investigation of the attachment and embedded content revealed phishing related activity intended to deceive users into interacting with fraudulent resources.

---

## Tools Used

- VirusTotal
- Hybrid Analysis
- MXToolbox
- IpInfo

---

## Skills Demonstrated

- Email Header Analysis
- Threat Intelligence
- IOC Extraction
- Phishing Investigation
- Attachment Analysis
- Technical Reporting
- Security Documentation

---

## Repository Structure

```
Email-Case-Study/
├── Raw-phishing-eml/
│   └── Raw-phishing-eml.eml
├── Email-Analysis/
│   ├── Technical-Analysis.md
│   ├── Executive-Summary.md
│   ├── IoCs.md
│   └── Conclusion.md
└── Screenshots/
```

---

## Investigation Artifacts

- Executive Summary
- Technical Analysis
- Indicators of Compromise
- Conclusion
- Evidence Screenshots

---

## MITRE ATT&CK Mapping

| Technique | Description |
|------------|------------|
| T1566.001 | Phishing: Spearphishing Attachment |
| T1204 | User Execution |

---

## Lessons Learned

- Email authentication does not guarantee legitimacy
- Trusted cloud services can be abused
- Social engineering remains highly effective
- Attachments should be analyzed before execution

---

## References

- PhishingPot Repository
- VirusTotal
- Hybrid Analysis
- MITRE ATT&CK
