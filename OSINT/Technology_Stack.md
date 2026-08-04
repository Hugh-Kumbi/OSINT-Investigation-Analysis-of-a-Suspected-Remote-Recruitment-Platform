# Technology Stack Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document identifies technologies observed during the investigation, including publicly visible web technologies and operational technologies encountered during recruiter interactions.

The purpose is to establish a technical profile of the infrastructure supporting the observed recruitment workflow.

Technology identification is based solely on evidence collected during the investigation.

---

# Scope

Domains analyzed:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

Operational observations:

- Recruiter onboarding process
- Platform interactions
- Screenshots
- Training session observations

---

# Collection Methodology

Technology identification was performed using:

- DNS Analysis
- Certificate Analysis
- Reverse DNS
- Browser observations
- Recruiter interactions
- Platform screenshots
- Manual inspection

No authenticated administrative access or intrusive testing was performed.

---

# Web Technology Summary

| Technology | occupationoasis.com | linkroles.my | unitelmatch.top |
|------------|---------------------|--------------|-----------------|
| CDN | Amazon CloudFront | Cloudflare | Cloudflare |
| DNS | Amazon Route 53 | Cloudflare | Cloudflare |
| SSL Provider | Amazon | Google Trust Services / Cloudflare | Google Trust Services / Let's Encrypt |
| IPv6 Support | No | Yes | Yes |
| Wildcard Certificates | Yes | Yes | Yes |
| CMS Identified | None observed | None observed | None observed |

---

# Content Management System (CMS)

No publicly identifiable Content Management System (CMS) was observed during the investigation.

Manual inspection and available technical evidence did not identify technologies such as:

- WordPress
- Joomla
- Drupal
- Magento
- Shopify
- Wix
- Squarespace

This observation reflects the evidence available at the time of collection and does not exclude the possibility of custom-built or undisclosed platforms.

---

# Hosting Technologies

## occupationoasis.com

Observed technologies include:

- Amazon Route 53
- Amazon CloudFront
- Amazon-issued TLS certificates
- Amazon IP address space (AS16509)

---

## linkroles.my

Observed technologies include:

- Cloudflare DNS
- Cloudflare edge infrastructure
- Google Trust Services certificates
- Cloudflare-managed TLS

---

## unitelmatch.top

Observed technologies include:

- Cloudflare DNS
- Cloudflare edge infrastructure
- Google Trust Services certificates
- Let's Encrypt certificates

---

# Network Technologies

The investigation identified the following networking technologies:

| Technology | Observation |
|------------|-------------|
| CDN | Amazon CloudFront and Cloudflare observed |
| Reverse Proxy | Cloudflare edge network observed |
| IPv6 | Supported by Cloudflare-hosted domains |
| DNS Hosting | Amazon Route 53 and Cloudflare |

---

# Authentication Technologies

No publicly observable authentication technologies were identified.

Examples not observed include:

- OAuth
- Microsoft Entra ID
- Okta
- Auth0
- SAML providers

Additional authenticated testing was outside the scope of this investigation.

---

# Payment and Financial Technologies

## Observed During Recruiter Interaction

The following observations were made during the onboarding and training process.

### Cryptocurrency

During the recruiter-led training session, cryptocurrency transactions were observed.

The investigator noted screenshots within a conversation labeled **"Customer Support"** that appeared to show cryptocurrency transfer confirmations.

The investigation documents only the presence of these screenshots and does not independently verify the transactions.

---

### Coincheck

During the same training session, the recruiter appeared to use a Coincheck account while demonstrating aspects of the workflow.

The investigator observed the interface during screen sharing or guided instruction.

No interaction with the Coincheck account was performed by the investigator.

The observation does not establish ownership of the account or the purpose of the transactions.

---

### Financial Workflow

The recruiter described a workflow involving:

- online store operations
- order processing
- commission payments
- cryptocurrency-related activity observed during training

The technical implementation of the payment process could not be independently verified during the investigation.

---

# Operational Technologies

The investigation observed the following operational technologies being used during the recruitment workflow.

| Technology | Observation |
|------------|-------------|
| Recruiter messaging platform | Used for onboarding and communication |
| Cloudflare | Infrastructure protection |
| Amazon Web Services | Infrastructure hosting |
| Coincheck | Observed during recruiter training session |
| Cryptocurrency | Screenshots of transfers observed |

---

# Technology Assessment

The investigation identified two distinct technology environments.

## Recruitment Website

The initial recruitment platform (`occupationoasis.com`) primarily relied on Amazon Web Services infrastructure.

## Operational Platforms

The onboarding platforms (`linkroles.my` and `unitelmatch.top`) relied on Cloudflare infrastructure with publicly trusted TLS certificates.

No publicly identifiable CMS was observed for any of the investigated domains.

The recruiter training session additionally included observations of cryptocurrency-related activity and the apparent use of Coincheck.

These observations are documented as part of the operational workflow and are not sufficient to determine the purpose or legitimacy of the transactions.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| EV-027 | DNS analysis |
| EV-028 | Certificate analysis |
| EV-029 | Recruiter training screenshots |
| EV-030 | Coincheck observations |
| EV-031 | Customer Support conversation screenshots |

---

# Confidence Assessment

| Finding | Confidence |
|---------|------------|
| Amazon infrastructure observed for occupationoasis.com   | High   |
| Cloudflare infrastructure observed for linkroles.my      | High   |
| Cloudflare infrastructure observed for unitelmatch.top   | High   |
| No identifiable CMS observed                             | Medium |
| Cryptocurrency-related activity observed during training | High   |
| Coincheck interface observed during training             | High   |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/DNS_Analysis.md)
- [Certificate_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Certificate_Analysis.md)
- [Infrastructure.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Social_Engineering_Analysis.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)

---

## Document Information

**Last Updated:**      July 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     
