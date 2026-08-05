# Technology Stack Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.1

---

# Objective

This document identifies the technologies observed during the investigation, including publicly visible web technologies, infrastructure components, and operational technologies encountered during recruiter interactions.

The objective is to establish a technical profile of the infrastructure supporting the observed recruitment workflow while distinguishing between evidence collected from website fingerprinting and observations made during the investigation.

---

# Scope

Domains analyzed:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

Operational observations:

- Recruiter onboarding process
- Platform interactions
- Browser fingerprinting
- Screenshots
- Training session observations

---

# Collection Methodology

Technology identification was performed using publicly available and passive techniques, including:

- Wappalyzer
- BuiltWith
- Browser inspection
- DNS Analysis
- Certificate Analysis
- Reverse DNS
- Manual platform observations
- Recruiter interactions

No authenticated administrative access or intrusive testing was performed.

---

# Application Technologies

## occupationoasis.com

### Web Framework

- Nuxt.js

### Static Site Generator

- Nuxt.js

### JavaScript Framework

- Vue.js
- Nuxt.js

### Analytics

- Google Analytics

### Tag Manager

- Google Tag Manager

### Performance Features

- Priority Hints

### Assessment

The website appears to be built using the Vue.js ecosystem through the Nuxt.js framework. No traditional Content Management System (CMS) was identified during the investigation.

---

## linkroles.my

### Automated Fingerprinting

No technologies were identified by Wappalyzer during the time of collection.

### Assessment

At the time of analysis, automated fingerprinting tools were unable to identify the application's technology stack.

This observation may reflect limitations of automated fingerprinting, Cloudflare protection mechanisms, dynamic content loading, or characteristics of the site's implementation. No conclusions are drawn from this observation.

---

## unitelmatch.top

### JavaScript Framework

- Vue.js

### Analytics

- Cloudflare Browser Insights

### Real User Monitoring (RUM)

- Cloudflare Browser Insights

### Miscellaneous

- HTTP/3
- QUIC

### Assessment

The application uses the Vue.js JavaScript framework together with Cloudflare Browser Insights for performance monitoring.

---

# Infrastructure Technologies

## occupationoasis.com

Observed infrastructure technologies include:

| Technology | Observation |
|------------|-------------|
| Hosting Platform          | Amazon Web Services     |
| DNS                       | Amazon Route 53         |
| CDN                       | Amazon CloudFront       |
| Object Storage            | Amazon S3               |
| TLS Certificate Authority | AWS Certificate Manager |
| Certificate Protocol      | TLS 1.3                 |

### Assessment

The observed technology stack is consistent with a website deployed entirely within the Amazon Web Services ecosystem.

---

## linkroles.my

Observed infrastructure technologies include:

| Technology | Observation |
|------------|-------------|
| CDN                  | Cloudflare                         |
| DNS Provider         | Cloudflare                         |
| Certificate Provider | Google Trust Services / Cloudflare |

### Assessment

The website is protected behind Cloudflare infrastructure. The origin hosting environment could not be determined using passive techniques.

---

## unitelmatch.top

Observed infrastructure technologies include:

| Technology | Observation |
|------------|-------------|
| CDN                | Cloudflare                  |
| DNS Provider       | Cloudflare                  |
| Analytics          | Cloudflare Browser Insights |
| HTTP Protocol      | HTTP/3                      |
| Transport Protocol | QUIC                        |

### Assessment

The observed infrastructure indicates deployment behind Cloudflare's edge network with modern transport protocols enabled.

---

# Content Management System (CMS)

No publicly identifiable Content Management System (CMS) was observed during the investigation.

The investigation did not identify evidence of common CMS platforms such as:

- WordPress
- Joomla
- Drupal
- Magento
- Shopify
- Wix
- Squarespace

This reflects only the technologies observable during collection and does not exclude the possibility of custom-built applications.

---

# Network Technologies

The following networking technologies were observed.

| Technology | Observation |
|------------|-------------|
| Amazon CloudFront | occupationoasis.com           |
| Cloudflare CDN    | linkroles.my, unitelmatch.top |
| Amazon Route 53   | occupationoasis.com           |
| Cloudflare DNS    | linkroles.my, unitelmatch.top |
| IPv6 Support      | linkroles.my, unitelmatch.top |
| TLS 1.3           | occupationoasis.com           |
| HTTP/3            | unitelmatch.top               |
| QUIC              | unitelmatch.top               |

---

# Authentication Technologies

No publicly observable authentication technologies were identified.

Examples not observed include:

- Microsoft Entra ID
- OAuth
- Auth0
- Okta
- SAML

Testing authenticated functionality was outside the scope of this investigation.

---

# Payment and Financial Technologies

## Cryptocurrency

During the recruiter-led onboarding session, cryptocurrency-related activity was observed.

The investigator observed screenshots within a conversation labelled **"Customer Support"** that appeared to show cryptocurrency transfer confirmations.

The investigation documents only the presence of these screenshots and does not independently verify the transactions.

---

## Coincheck

During the training session, the recruiter appeared to access a Coincheck account while demonstrating the workflow.

The investigator observed the interface but did not interact with the account.

The observation documents the apparent use of Coincheck during the onboarding process and does not establish ownership of the account or the purpose of the transactions.

---

## Financial Workflow

The recruiter described a workflow involving:

- Online store management
- Order processing
- Commission-based earnings
- Daily settlements
- Cryptocurrency-related activity observed during training

The technical implementation of the payment process could not be independently verified.

---

# Operational Technologies

The following operational technologies were observed during recruiter interactions.

| Technology | Observation |
|------------|-------------|
| Recruiter Messaging Platform | Used throughout onboarding and communication         |
| Amazon Web Services          | Hosting infrastructure for occupationoasis.com       |
| Cloudflare                   | DNS and edge infrastructure for onboarding platforms |
| Coincheck                    | Observed during recruiter-led training               |
| Cryptocurrency               | Transfer screenshots observed during training        |

---

# Technology Comparison Matrix

| Technology | occupationoasis.com | linkroles.my | unitelmatch.top |
|------------|---------------------|--------------|-----------------|
| Vue.js                      | ✓           | Not observed   | ✓ |
| Nuxt.js                     | ✓           | Not observed   | Not observed   |
| Google Analytics            | ✓           | Not observed   | Not observed   |
| Google Tag Manager          | ✓           | Not observed   | Not observed   |
| Cloudflare Browser Insights | ✗           | Not observed   | ✓              |
| AWS Certificate Manager     | ✓           | ✗              | ✗              |
| Amazon CloudFront           | ✓           | ✗              | ✗              |
| Amazon S3                   | ✓           | ✗              | ✗              |
| Cloudflare CDN              | ✗           | ✓              | ✓              |
| HTTP/3                      | Not observed | Not observed   | ✓              |
| QUIC                        | Not observed | Not observed   | ✓              |
| TLS 1.3                     | ✓            | Not identified | Not identified |
| CMS Identified              | No | No | No |

---

# Technology Assessment

The investigation identified two distinct technology environments.

## Recruitment Website

The initial recruitment website (`occupationoasis.com`) is hosted within the Amazon Web Services ecosystem and uses a modern Vue.js/Nuxt.js application architecture.

Observed supporting technologies include:

- Amazon Route 53
- Amazon CloudFront
- Amazon S3
- Google Analytics
- Google Tag Manager
- AWS Certificate Manager

---

## Operational Platforms

The onboarding platforms (`linkroles.my` and `unitelmatch.top`) are protected by Cloudflare infrastructure.

While `unitelmatch.top` exposed a Vue.js application and Cloudflare Browser Insights, `linkroles.my` could not be fingerprinted using automated tools during the investigation.

---

## Operational Workflow

During recruiter-led onboarding, the investigator additionally observed:

- Cryptocurrency-related activity
- Apparent use of Coincheck
- Screenshots depicting cryptocurrency transfers within a "Customer Support" conversation

These observations are documented as part of the operational workflow and are not sufficient, on their own, to determine the purpose or legitimacy of the transactions.

---

# Key Observations

The following observations are supported by the evidence collected:

1. `occupationoasis.com` employs a modern Vue.js/Nuxt.js application hosted entirely within Amazon Web Services.

2. `linkroles.my` and `unitelmatch.top` rely on Cloudflare for DNS and edge infrastructure.

3. `unitelmatch.top` exposes a Vue.js application and Cloudflare Browser Insights, while `linkroles.my` could not be fingerprinted by Wappalyzer during collection.

4. No publicly identifiable Content Management System (CMS) was observed for any of the three domains.

5. Recruiter interactions included observable cryptocurrency-related activity and apparent use of the Coincheck platform as part of the onboarding workflow.

These observations describe technologies visible during the investigation and should not be interpreted as indicators of malicious activity without additional corroborating evidence.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-028-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-01.png), [EV-028-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-02.png), [EV-028-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-03.png), [EV-028-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-04.png) | Wappalyzer results – occupationoasis.com |
| [EV-029-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-029-01.png), [EV-029-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-029-02.png), [EV-029-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-029-03.png) | Wappalyzer results – linkroles.my        |
| [EV-030-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-030-01.png), [EV-030-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-030-02.png), [EV-030-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-030-03.png) | Wappalyzer results – unitelmatch.top     |
| [EV-032-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-01.png),[EV-032-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-02.png), [EV-032-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-03.png), [EV-032-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-04.png), [EV-032-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-05.png), [EV-032-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-06.png), [EV-032-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-07.png), [EV-032-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-08.png), [EV-032-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-09.png), [EV-032-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-10.png), [EV-032-11](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-11.png), [EV-032-12](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-032-12.png) | DNS and infrastructure analysis                 |
| [EV-033-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-01.png), [EV-033-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-02.png), [EV-033-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-03.png), [EV-033-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-04.png), [EV-033-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-05.png), [EV-033-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-06.png), [EV-033-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-07.png), [EV-033-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-08.png), [EV-033-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-09.png), [EV-033-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-10.png), [EV-033-11](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-11.png), [EV-033-12](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-033-12.png) | Certificate analysis                     |
| [EV-003-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-01.png), [EV-003-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-02.png), [EV-003-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-03.png), [EV-003-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-04.png), [EV-003-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-05.png), [EV-003-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-06.png), [EV-003-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-07.png), [EV-003-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-08.png), [EV-003-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-09.png), [EV-003-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-10.png), [EV-003-11](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-11.png), [EV-003-12](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-12.png), [EV-003-13](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-13.png), [EV-003-14](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-14.png), [EV-003-15](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-15.png), [EV-003-16](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-16.png), [EV-003-17](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-17.png), [EV-003-18](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-18.png) | Recruiter training screenshots           |
| [EV-035-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-035-01.png), [EV-035-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-035-02.png), [EV-035-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-035-03.png), [EV-035-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-035-04.png), [EV-035-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-035-05.png) | Coincheck observations                   |
| [EV-036-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-01.png), [EV-036-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-02.png), [EV-036-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-03.png) | Cryptocurrency transfer screenshots      |

---

# Confidence Assessment

| Finding | Confidence |
|---------|------------|
| AWS technology stack identified for occupationoasis.com  | High   |
| Cloudflare infrastructure identified for linkroles.my    | High   |
| Cloudflare infrastructure identified for unitelmatch.top | High   |
| Vue.js identified on occupationoasis.com                 | High   |
| Vue.js identified on unitelmatch.top                     | High   |
| No identifiable CMS observed                             | Medium |
| Cryptocurrency-related activity observed during training | High   |
| Coincheck interface observed during training             | High   |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [Passive_DNS.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Passive_DNS.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/DNS_Analysis.md)
- [Certificate_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Certificate_Analysis.md)
- [Infrastructure.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Social_Engineering_Analysis.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)
---

## Document Information

**Last Updated:**      July 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     
