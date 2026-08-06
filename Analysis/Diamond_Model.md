# Diamond Model of Intrusion Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Framework:** Diamond Model of Intrusion Analysis

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document applies the Diamond Model of Intrusion Analysis to organize the evidence collected throughout the investigation.

The Diamond Model provides a structured method for describing relationships between:

- Adversary
- Infrastructure
- Capability
- Victim

The model is intended to improve analytical understanding of the observed campaign and does not attribute malicious intent beyond the available evidence.

---

# Scope

This analysis covers:

- Recruiter interactions
- Recruitment workflow
- Infrastructure observations
- Technical analysis
- Social engineering techniques
- Platform transitions
- Financial workflow observations

---

# Methodology

The Diamond Model was populated using only evidence collected during the investigation.

Each analytical element includes:

- Observations
- Supporting evidence
- Confidence assessment

Where evidence was insufficient, analytical gaps are explicitly documented.

---

# Diamond Model Overview

```
                     Adversary
                          ▲
                          │
                          │
Capability ◄──────────────┼──────────────► Infrastructure
                          │
                          │
                          ▼
                        Victim
```

---

# Adversary

## Observations

The investigation identified an individual acting as a recruiter who initiated communication after the analyst submitted a legitimate job application.

Observed behaviors included:

- Initiating recruiter contact
- Conducting structured onboarding
- Scheduling training sessions
- Guiding platform registration
- Explaining the purported business model
- Directing migration to an alternative domain after a browser warning

No attempt was made to determine the recruiter's true identity.

---

## Characteristics

Observed characteristics included:

- Professional communication
- Consistent availability
- Step-by-step instruction
- Structured onboarding
- Emphasis on legitimacy
- Use of multiple online platforms

---

## Intelligence Gaps

The investigation could not determine:

- True identity
- Geographic location
- Organizational affiliation
- Number of individuals involved
- Operational hierarchy

---

## Confidence

**Medium**

The behaviors are directly observed; the identity and organizational structure remain unknown.

---

# Infrastructure

## Domains

The investigation identified the following domains:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

---

## Hosting

Observed infrastructure included:

- Amazon Web Services
- Amazon CloudFront
- Cloudflare

---

## DNS

Observed providers:

- Amazon Route 53
- Cloudflare DNS

---

## Certificates

Observed providers:

- AWS Certificate Manager
- Google Trust Services
- Let's Encrypt

---

## Operational Transition

The recruiter instructed the analyst to migrate from:

`linkroles.my`

to

`unitelmatch.top`

after a browser warning interrupted the onboarding process.

---

## Confidence

**High**

All infrastructure observations are supported by technical evidence.

---

# Capability

## Technical Capabilities

Observed capabilities included:

- Multiple web platforms
- Cloud-hosted infrastructure
- TLS certificates
- DNS management
- Modern web frameworks
- Platform onboarding workflow

---

## Operational Capabilities

Observed operational capabilities included:

- Structured recruitment process
- Guided onboarding
- Multiple communication stages
- Domain transition
- Customer support workflow
- Cryptocurrency-related observations

---

## Social Engineering Capabilities

Observed techniques included:

- Rapport building
- Opportunity framing
- Incremental commitment
- Guided decision-making
- Authority cues
- Financial incentive messaging

---

## Financial Workflow

During onboarding, the analyst observed:

- OKX Wallet
- Cryptocurrency-related screenshots
- Commission-based explanations
- Daily settlement descriptions

The analyst did not participate in financial transactions.

---

## Intelligence Gaps

Unknowns include:

- Back-end platform architecture
- Internal administrative systems
- Payment processing implementation
- Business relationships
- Scale of operations

---

## Confidence

**High**

Observed capabilities are supported by technical analysis and recruiter interactions.

---

# Victim

## Target Profile

The analyst was targeted after applying for a remote employment opportunity.

The campaign specifically addressed individuals seeking:

- Remote work
- Flexible employment
- Online income opportunities

---

## Targeting Method

The recruiter referenced the existing job application to establish credibility.

The communication progressed gradually through:

- Initial contact
- Rapport building
- Opportunity presentation
- Platform registration
- Guided onboarding

---

## Required Actions

The analyst was instructed to:

- Register accounts
- Complete onboarding forms
- Submit store information
- Navigate platform interfaces

---

## Analyst Actions

During the investigation, the analyst:

- Collected evidence
- Documented observations
- Avoided providing sensitive personal information
- Avoided financial transactions
- Maintained an observational role

---

## Confidence

**High**

Victim interactions were directly observed and documented.

---

# Diamond Relationships

## Adversary → Infrastructure

Observed relationship:

The recruiter directed the analyst through multiple domains and online platforms during onboarding.

Confidence: **High**

---

## Infrastructure → Capability

Observed relationship:

Cloud-hosted infrastructure supported the recruitment workflow, onboarding process, and platform transitions.

Confidence: **High**

---

## Capability → Victim

Observed relationship:

Structured onboarding, guided instruction, and staged communication were used to encourage continued participation.

Confidence: **High**

---

## Victim → Adversary

Observed relationship:

The analyst engaged only to document and observe the recruitment workflow.

No financial participation occurred.

Confidence: **High**

---

# Event Timeline within the Diamond Model

| Stage | Diamond Vertex |
|--------|----------------|
| Job application | Victim |
| Recruiter contact | Adversary |
| Recruitment website | Infrastructure |
| Guided onboarding | Capability |
| Browser warning | Infrastructure |
| Domain migration | Infrastructure |
| Training session | Capability |
| Cryptocurrency observations | Capability |

---

# Intelligence Gaps

The investigation was unable to determine:

- Campaign ownership
- Organizational structure
- Geographic origin
- Number of operators
- Hosting origin behind Cloudflare
- Internal payment systems
- Back-end administration
- Additional campaign infrastructure

These gaps represent opportunities for future investigation should additional evidence become available.

---

# Analytical Assessment

The Diamond Model illustrates a coordinated relationship between observed infrastructure, recruiter behavior, and the onboarding workflow.

The investigation documented:

- Multiple coordinated domains
- Cloud-hosted infrastructure
- Structured recruiter interactions
- Progressive onboarding
- Observable platform migration
- Financial workflow demonstrations

No malware delivery, exploitation of software vulnerabilities, or post-compromise activity was observed during the investigation.

Accordingly, the campaign appears to rely primarily on user interaction and structured social engineering rather than technical exploitation.

This assessment reflects only the evidence collected during the investigation.

---

# Key Findings

1. Multiple domains supported different stages of the observed workflow.

2. Cloud infrastructure enabled rapid platform deployment and transition.

3. The recruiter maintained continuous interaction throughout onboarding.

4. Platform migration occurred immediately after a browser warning.

5. Cryptocurrency-related activity formed part of the demonstrated workflow.

6. The analyst remained in an observational role and did not participate in financial transactions.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| EV-052 | Recruiter communications |
| EV-053 | Domain analysis |
| EV-054 | Infrastructure analysis |
| EV-055 | Technology stack analysis |
| EV-056 | Social engineering observations |
| EV-057 | Browser warning and domain migration |
| EV-058 | OKX Wallet observations |
| EV-059 | Cryptocurrency screenshots |

---

# Confidence Assessment

| Diamond Vertex | Confidence |
|----------------|------------|
| Adversary | Medium |
| Infrastructure | High |
| Capability | High |
| Victim | High |

---

# Related Documents

- [Campaign_Overview.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Campaign_Overview.md)
- [Investigation_Timeline.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Investigation_Timeline.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Social_Engineering_Analysis.md)
- [MITRE_ATT&CK_Mapping.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/MITRE_ATT%26CK_Mapping.md)
- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [Infrastructure.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure.md)
- [Technology_Stack.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Technology_Stack.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     