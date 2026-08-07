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
|-------|----------------|
| Job application             | Victim         |
| Recruiter contact           | Adversary      |
| Recruitment website         | Infrastructure |
| Guided onboarding           | Capability     |
| Browser warning             | Infrastructure |
| Domain migration            | Infrastructure |
| Training session            | Capability     |
| Cryptocurrency observations | Capability     |

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
| [EV-002-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-002-01.png), [EV-003-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-01.png), [EV-003-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-02.png), [EV-003-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-03.png), [EV-003-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-04.png), [EV-003-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-05.png), [EV-003-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-06.png), [EV-003-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-07.png), [EV-003-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-08.png), [EV-003-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-09.png), [EV-003-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-10.png), [EV-003-11](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-11.png), [EV-003-12](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-12.png), [EV-003-13](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-13.png), [EV-003-14](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-14.png), [EV-003-15](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-15.png), [EV-003-16](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-16.png), [EV-003-17](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-17.png), [EV-003-18](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-18.png), [EV-004-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-01.png), [EV-004-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-02.png), [EV-004-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-03.png), [EV-004-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-04.png), [EV-004-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-05.png), [EV-004-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-06.png), [EV-005-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-01.png), [EV-005-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-02.png), [EV-005-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-03.png), [EV-005-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-04.png), [EV-005-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-05.png), [EV-005-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-06.png), [EV-005-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-07.png) | Recruiter communications             |
| [EV-022-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-01.png), [EV-022-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-02.png), [EV-022-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-03.png), [EV-022-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-04.png), [EV-023-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-023-01.png), [EV-023-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-023-02.png), [EV-024-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-024-01.png), [EV-024-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-024-02.png), [EV-024-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-024-03.png), [EV-025-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-025-01.png), [EV-025-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-025-02.png), [EV-025-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-025-03.png), [EV-025-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-025-04.png), [EV-025-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-025-05.png), [EV-025-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-025-06.png), [EV-016-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-01.png), [EV-016-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-02.png), [EV-016-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-03.png), [EV-016-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-04.png), [EV-016-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-05.png), [EV-016-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-06.png), [EV-016-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-07.png), [EV-017-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-01.png), [EV-017-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-02.png), [EV-017-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-03.png), [EV-017-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-04.png), [EV-018-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-01.png), [EV-018-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-02.png), [EV-018-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-03.png), [EV-018-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-04.png), [EV-018-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-05.png), [EV-018-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-06.png), [EV-018-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-07.png), [EV-018-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-08.png), [EV-018-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-09.png), [EV-018-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-10.png), [EV-019-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-019-01.png), [EV-020-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-020-01.png), [EV-021-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-021-01.png) | Domain analysis                      |
| [EV-043-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-01.png), [EV-043-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-02.png), [EV-043-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-03.png), [EV-043-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-04.png), [EV-043-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-05.png), [EV-043-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-06.png), [EV-043-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-07.png), [EV-043-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-08.png), [EV-043-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-09.png), [EV-043-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-10.png), [EV-043-19](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-19.png), [EV-043-20](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-20.png), [EV-043-21](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-21.png), [EV-043-22](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-22.png), [EV-043-23](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-23.png), [EV-043-24](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-24.png), [EV-043-25](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-25.png), [EV-043-26](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-26.png), [EV-043-27](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-27.png), [EV-043-28](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-28.png), [EV-043-29](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-29.png), [EV-043-30](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-30.png), [EV-043-31](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-31.png), [EV-043-32](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-32.png), [EV-043-33](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-33.png), [EV-043-34](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-34.png), [EV-043-35](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-35.png), [EV-043-36](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-36.png), [EV-043-37](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-37.png), [EV-043-38](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-38.png), [EV-043-39](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-39.png), [EV-043-40](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-40.png), [EV-043-41](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-043-41.png) | Infrastructure analysis              |
| [EV-028-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-01.png), [EV-028-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-02.png), [EV-028-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-03.png), [EV-028-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-028-04.png), [EV-029-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-029-01.png), [EV-029-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-029-02.png), [EV-029-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-029-03.png), [EV-030-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-030-01.png), [EV-030-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-030-02.png), [EV-030-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-030-03.png) | Technology stack analysis            |
| [EV-044-01](), [EV-044-02](), [EV-044-03](), [EV-044-04](), [EV-044-05](), [EV-044-06](), [EV-044-07](), [EV-044-08](), [EV-044-09](), [EV-044-10](), [EV-044-11](), [EV-044-12](), [EV-044-13](), [EV-044-14](), [EV-044-15](), [EV-044-16](), [EV-044-17](), [EV-044-18](), [EV-044-19](), [EV-044-20](), [EV-044-21](), [EV-044-22](), [EV-044-23](), [EV-044-24](), [EV-044-25](), [EV-044-26](), [EV-044-27](), [EV-044-28](), [EV-044-29](), [EV-044-30](), [EV-044-31](), [EV-044-32](), [EV-044-33](), [EV-044-34](), [EV-044-35](), [EV-044-36](), [EV-044-37](), [EV-044-38](), [EV-044-39](), [EV-044-40](), [EV-044-41](), [EV-044-42](), [EV-044-43](), [EV-044-44](), [EV-044-45](), [EV-044-46](), [EV-044-47](), [EV-044-48](), [EV-044-49](), [EV-044-50](), [EV-044-51](), [EV-044-52](), [EV-044-53](), [EV-044-54](), [EV-044-55](), [EV-044-56](), [EV-044-57](), [EV-044-58](), [EV-044-59](), [EV-044-60](), [EV-044-61](), [EV-044-62](), [EV-044-63](), [EV-044-64](), [EV-044-65](), [EV-044-66](), [EV-044-67](), [EV-044-68](), [EV-044-69](), [EV-044-70](), [EV-044-71](), [EV-044-72](), [EV-044-73](), [EV-044-74](), [EV-044-75](), [EV-044-76](), [EV-044-77](), [EV-044-78](), [EV-044-79](), [EV-044-80](), [EV-044-81](), [EV-044-82](), [EV-044-83](), [EV-044-84](), [EV-044-85](), [EV-044-86](), [EV-044-87](), [EV-044-88](), [EV-044-89](), [EV-044-90]() | Social engineering observations      |
| [EV-012-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-012-01.png), [EV-012-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-013-01.png) | Browser warning and platform migration | Browser warning and domain migration |
| [EV-036-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-01.png), [EV-036-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-02.png), [EV-036-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-03.png) | OKX Wallet observations and Cryptocurrency screenshots           |

---

# Confidence Assessment

| Diamond Vertex | Confidence |
|----------------|------------|
| Adversary      | Medium     |
| Infrastructure | High       |
| Capability     | High       |
| Victim         | High       |

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