# Infrastructure Evolution

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Recruitment Campaign

**Classification:** Cyber Threat Intelligence (CTI)

**Version:** 1.1

---

# Purpose

This document tracks the evolution of the campaign's technical infrastructure throughout the investigation.

Rather than relying on a single operational platform, the recruiter introduced multiple domains over time. These transitions occurred during active communication with the investigator and illustrate how the onboarding workflow continued despite changes in web infrastructure.

The analysis documents only observed infrastructure changes and does not attribute ownership or operational control beyond the available evidence.

---

# Infrastructure Timeline

| Order | Domain | Purpose | Transition Reason |
|------:|--------|---------|-------------------|
| 1 | occupationoasis.com | Initial recruitment website | Initial contact |
| 2 | linkroles.my | First onboarding portal | Recruiter-guided registration |
| 3 | unitelmatch.top | Replacement onboarding portal | Introduced after issues with the previous platform |
| 4 | unitelmatch.cc | Updated onboarding portal | Introduced by recruiter as the next platform |
| 5 | unitelmatch.cyou | Backup onboarding portal | Introduced after Google Safe Browsing warning |

---

# Infrastructure Evolution

```text
Recruitment Website
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
Platform Migration
        │
        ▼
unitelmatch.top
        │
        ▼
Platform Update
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

# Infrastructure Characteristics

Throughout the investigation the following recurring characteristics were observed.

## Cloud Hosting

- Amazon Web Services (AWS)
- Amazon CloudFront
- Cloudflare

---

## Modern Web Technologies

Observed technologies included:

- Vue.js
- Nuxt.js
- HTTP/3
- QUIC
- TLS 1.3
- Google Analytics
- Google Tag Manager
- Cloudflare Browser Insights

---

## SSL Certificates

Observed certificate authorities:

- AWS Certificate Manager
- Google Trust Services
- Let's Encrypt

The use of valid SSL certificates indicates encrypted communications but does not establish legitimacy.

---

## Domain Registration

Observed domains were registered within a relatively short time period.

| Domain | Creation Date |
|---------|---------------|
| occupationoasis.com | 2026-06-29 |
| linkroles.my | 2026-07-19 |
| unitelmatch.top | 2026-07-23 |
| unitelmatch.cc | Pending Analysis |
| unitelmatch.cyou | Pending Analysis |

---

# Operational Evolution

The campaign infrastructure evolved while maintaining a consistent recruiter-led workflow.

Observed changes included:

- Introduction of replacement portals.
- Continued recruiter guidance.
- Migration following browser security warnings.
- Consistent onboarding experience across domains.
- Continued use of cloud-hosted infrastructure.

---

# Key Observations

The investigation documented:

- Five operational domains.
- Multiple infrastructure transitions.
- Continued recruiter communication during platform migration.
- Browser security warnings followed by replacement domains.
- Similar operational purposes across all observed portals.

These observations suggest infrastructure evolution while maintaining a consistent onboarding workflow.

---

# Intelligence Gaps

Further collection is recommended for:

- WHOIS records for unitelmatch.cc
- WHOIS records for unitelmatch.cyou
- DNS records
- SSL certificates
- Technology stack
- Reputation
- Passive DNS history

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-002-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-002-01.png) | Recruiter communication |
| [EV-009-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-009-01.png) | Initial registration platform |
| [EV-012-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-012-01.png) | Google Safe Browsing warning |
| [EV-013-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-013-01.png) | Replacement platform communicated by recruiter |

---

# Related Documents

- domain_relationships.md
- infrastructure.md
- certificate_analysis.md
- Investigation_Timeline.md
- Campaign_Overview.md
---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store