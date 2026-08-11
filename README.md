# Operation Phantom Store

> **Analysis of a Suspected Multi-Domain Recruitment Campaign**

A structured Open Source Intelligence (OSINT) and Cyber Threat Intelligence (CTI) investigation into a recruiter-led online campaign that evolved across multiple web domains. The investigation combines passive OSINT collection, infrastructure analysis, behavioral analysis, and threat intelligence methodologies to document the campaign and identify defensive opportunities.

---

**Case ID:** OSINT-2026-001  
**Project Type:** Cyber Threat Intelligence (CTI) Case Study  
**Version:** 1.1  
**Status:** Complete (Version 1.1)

---

![Version](https://img.shields.io/badge/version-1.1-blue)
![Status](https://img.shields.io/badge/status-Complete-success)
![OSINT](https://img.shields.io/badge/OSINT-Investigation-green)
![CTI](https://img.shields.io/badge/Cyber%20Threat%20Intelligence-Case%20Study-red)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

# Overview

This repository documents an end-to-end cyber threat intelligence investigation into a suspected online recruitment campaign encountered during a real-world job application process.

Rather than immediately disengaging, I conducted a structured, evidence-driven investigation using passive Open Source Intelligence (OSINT) techniques, behavioral analysis, and established Cyber Threat Intelligence (CTI) methodologies.

The investigation focused on documenting recruiter interactions, analyzing technical infrastructure, identifying recurring behavioral patterns, and developing defensive recommendations without engaging in intrusive or unauthorized activity.

As the investigation progressed, additional infrastructure was identified and incorporated into **Version 1.1**, expanding the documented campaign from three to five operational domains.

---

# Investigation Objectives

The objectives of this investigation were to:

- Document the recruiter-led onboarding process.
- Identify and analyze campaign infrastructure.
- Perform passive OSINT collection.
- Correlate technical and behavioral observations.
- Apply structured intelligence frameworks.
- Identify Indicators of Compromise (IOCs).
- Develop detection opportunities for defenders.
- Produce professional intelligence reporting.

---

# Skills Demonstrated

## Open Source Intelligence (OSINT)

- DNS Analysis
- Passive DNS
- WHOIS Analysis
- Reverse DNS
- Certificate Transparency
- SSL Certificate Analysis
- Technology Fingerprinting
- Infrastructure Analysis
- Domain Correlation
- Reputation Analysis

---

## Cyber Threat Intelligence (CTI)

- Intelligence Lifecycle
- Campaign Analysis
- Behavioral Analysis
- Social Engineering Assessment
- Infrastructure Correlation
- Confidence Assessment
- Intelligence Gap Analysis
- Structured Reporting

---

## Detection Engineering

- Indicator Development
- Detection Opportunities
- Defensive Recommendations
- ATT&CK Mapping
- Threat Hunting Concepts

---

## Security Operations

- Threat Analysis
- IOC Documentation
- Timeline Reconstruction
- Evidence Management
- Technical Documentation

---

# Campaign Overview

The investigation identified five operational domains introduced throughout recruiter-led onboarding.

| Domain | Observed Purpose | Status |
|--------|------------------|--------|
| occupationoasis.com | Recruitment platform          | Observed                           |
| linkroles.my        | Initial onboarding portal     | Replaced                           |
| unitelmatch.top     | Replacement onboarding portal | Replaced                           |
| unitelmatch.cc      | Upgraded onboarding portal    | Replaced following browser warning |
| unitelmatch.cyou    | Backup onboarding portal      | Active during investigation        |

---

# Campaign Progression

```text
Job Advertisement
        │
        ▼
occupationoasis.com
        │
        ▼
Recruiter Contact
        │
        ▼
linkroles.my
        │
        ▼
Google Safe Browsing Warning
        │
        ▼
unitelmatch.top
        │
        ▼
Additional Training
        │
Google Safe Browsing Warning
        │
        ▼
unitelmatch.cc
        │
 Google Safe Browsing Warning
        │
        ▼
unitelmatch.cyou
```

---

# Repository Structure

```text
.
├── README.md
│
├── docs
│   ├── Campaign_Overview.md
│   ├── Methodology.md
│   ├── Investigation_Timeline.md
│   ├── Findings.md
│   ├── Lessons_Learned.md
│   ├── Evidence_Register.md
│   └── Executive_Report.pdf
│
├── osint
│   ├── Passive_DNS.md
│   ├── DNS_Analysis.md
│   ├── Certificate_Analysis.md
│   ├── Infrastructure.md
│   ├── Technology_Stack.md
│   ├── Reputation.md
│   └── Domain_Relationships.md
│
├── analysis
│   ├── Social_Engineering_Analysis.md
│   ├── MITRE_ATT&CK_Mapping.md
│   ├── Diamond_Model.md
│   ├── Attack_Lifecycle.md
│   ├── Indicators_of_Compromise.md
│   ├── Detection_Opportunities.md
│   ├── Intelligence_Gaps.md
│   └── Confidence_Assessment.md
│
├── evidence
│   ├── Screenshots/
│   ├── Recruiter_Chat/
│   └── Browser_Warnings/
│
└── assets
    ├── Campaign_Flow.png
    ├── Infrastructure_Diagram.png
    ├── MITRE_ATT&CK.png
    ├── Diamond_Model.png
    └── Timeline.png
```

---

# Methodology

The investigation followed a structured intelligence lifecycle.

1. Evidence Collection
2. Passive OSINT Collection
3. Infrastructure Analysis
4. Behavioral Analysis
5. Threat Intelligence Mapping
6. IOC Development
7. Detection Engineering
8. Reporting

Only passive intelligence collection methods were used.

No unauthorized access, exploitation, credential harvesting, or intrusive scanning was performed.

---

# Intelligence Frameworks Applied

- MITRE ATT&CK
- Diamond Model of Intrusion Analysis
- Cyber Threat Intelligence Lifecycle
- Attack Lifecycle Analysis

These frameworks were used to organize observations and support evidence-based analytical assessments.

---

# Key Findings

The investigation identified:

- A structured recruiter-led onboarding process.
- Progressive trust-building through staged interactions.
- Five operational domains introduced throughout the campaign.
- Repeated migration to replacement domains following browser security warnings.
- Use of commercial cloud infrastructure (AWS and Cloudflare).
- Modern JavaScript frameworks (Vue.js and Nuxt.js).
- Valid SSL certificates from trusted Certificate Authorities.
- Cryptocurrency-related activity observed during later onboarding stages.
- No malware delivery or technical exploitation observed.
- A campaign primarily driven by social engineering techniques.

---

# Defensive Recommendations

Organizations should consider monitoring for:

- Newly registered onboarding domains.
- Repeated domain migration during user onboarding.
- Recruiters encouraging users to ignore browser security warnings.
- Cryptocurrency requests during employment onboarding.
- Repeated infrastructure changes associated with recruitment workflows.

---

# Ethical Statement

This investigation was conducted exclusively for educational, research, and defensive cybersecurity purposes.

All observations were obtained through passive OSINT techniques and voluntary recruiter communications.

No unauthorized access, exploitation, or interference with any systems occurred during the investigation.

---

# Future Work

Potential future enhancements include:

- Continuous Certificate Transparency monitoring.
- Passive DNS historical analysis.
- Infrastructure relationship visualization.
- Blockchain analytics.
- Sigma rule development.
- SIEM detection content.
- Infrastructure monitoring for newly observed domains.

---

# Disclaimer

This repository documents an evidence-based investigation of a suspected online recruitment campaign.

The inclusion of any domain, IP address, infrastructure provider, or technology does **not** imply malicious ownership or intent. Observations and analytical assessments are based solely on information collected during the investigation and publicly available data.

No attribution is made beyond what is supported by documented evidence.

---

# License

This project is licensed under the MIT License unless otherwise stated.

---

# Author

**Hugh Chanetsa**

Cybersecurity Professional

Specializing in:

- Security Operations (SOC)
- Threat Detection
- Vulnerability Management
- Active Directory Security
- Incident Response
- Threat Intelligence
- Open Source Intelligence (OSINT)

### Certifications

- ISC² Certified in Cybersecurity (CC)
- Google Cybersecurity Professional Certificate
- CompTIA Security+ (In Progress)

---

## Portfolio

This repository forms part of a broader cybersecurity portfolio demonstrating practical, hands-on investigations and security research.

Future updates will include additional evidence, findings, and technical analysis as the investigation progresses.
