## Overview
Case ID: PHISH-001
Classification: Phishing
Severity: High
- This document contains indicators of compromise identified during the phishing email investigation.

---

## Email Indicators
| Type | Value |
| --- | --- |
| **Sender Email** | ``michelleleeoma7@gmail.com`` |
| **Return-Path** | ``michelleleeoma7@gmail.com`` |
| **Subject Line** | ``GO.Get.Bitcoin.0.7495.BTC`` |
| **Message-ID** | ``<CAN3R5gNyH1sZMDbYkKQJNwY+trdZ-ERZ4JpMKOynO13NftK4Yg@mail.gmail.com>`` |

---

## Infrastructure Indicators
| Type | Value |
| --- | --- |
| **Sender IP Address** | ``209.85.219.182`` |
| **Originating Mail Server** | ``mail-ot1-f182.google.com`` |
| **ASN** | AS15169 (Google LLC) |
| **Country** | United States |

---

## URL Indicators
| Type | Value |
| --- | --- |
| **Phishing URL** | ``hxxps://bit[.]ly/3V8v9ku`` |
| **Domain** | ``bit[.]ly`` |
| **URL Shortener** | ``bit[.]ly`` |

---

## File Indicators
| Type | Value |
| --- | --- |
| **File Name** | ``Bitcoin.Balance.0.7495.BTC6BbPOzRwkSNiLISGdqP0N.pdf`` |
| **File Type** | PDF (``%PDF-1.3``) |
| **SHA256** | ``f1d70491c74c768986139ea2bab8441de7e5681b3409f85d0b265b6230a1a0e4`` |

---

## IOC Confidence

| Indicator | Confidence |
|------------|------------|
| **Sender Email** | Medium |
| **Bitly URL** | High |
| **PDF SHA256** | High |

## Detection Notes
- Monitor inbound emails containing shortened URLs
- Flag cryptocurrency‑themed phishing lures
- Monitor suspicious PDF attachments from external senders
- Investigate repeated sender infrastructure usage

---

## Detection Opportunities
- Alert on inbound emails containing Bitly links.
- Alert on cryptocurrency-themed subject lines.
- Alert on PDF attachments containing shortened URLs.
- Investigate messages originating from the identified sender address.
