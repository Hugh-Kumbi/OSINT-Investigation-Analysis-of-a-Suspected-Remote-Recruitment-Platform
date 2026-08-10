# Attack Lifecycle Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Cyber Threat Intelligence (CTI)

**Framework:** Adapted Cyber Kill Chain / Campaign Lifecycle

**Status:** Investigation Complete

**Version:** 1.0

---

# Objective

This document reconstructs the observed campaign as a chronological lifecycle.

Unlike the MITRE ATT&CK mapping, which categorizes adversary behaviors, this analysis focuses on the sequence of events observed during the investigation.

Only stages directly supported by collected evidence are included.

---

# Scope

This lifecycle covers:

- Initial recruitment
- Recruiter communications
- Platform onboarding
- Domain migration
- Cryptocurrency introduction
- Investigation termination

---

# Methodology

The lifecycle was reconstructed using:

- Recruiter conversations
- Investigation timeline
- Screenshots
- Technical analysis
- Infrastructure observations
- Analyst notes

No assumptions were made regarding stages that were not directly observed.

---

# Campaign Lifecycle Overview

```text
Job Application
      │
      ▼
Recruiter Contact
      │
      ▼
Rapport Building
      │
      ▼
Employment Opportunity Presented
      │
      ▼
Training Scheduled
      │
      ▼
Platform Registration
      │
      ▼
Guided Onboarding
      │
      ▼
Browser Warning
      │
      ▼
Migration to Alternate Domain
      │
      ▼
Training Continues
      │
      ▼
Cryptocurrency Introduced
      │
      ▼
Evidence Collection
      │
      ▼
Investigation Closed
```

---

# Stage 1 — Initial Contact

## Observation

The analyst submitted an application through **occupationoasis.com** for a remote employment opportunity.

A recruiter subsequently initiated contact, referencing the application and establishing context for further discussion.

## Supporting Evidence

- Recruiter conversation
- Campaign timeline

## Confidence

**High**

---

# Stage 2 — Rapport Building

## Observation

The recruiter established a conversational relationship before introducing operational details.

Topics included:

- Current employment
- Desired work arrangement
- Salary expectations
- Availability

## Assessment

The conversation resembled a legitimate recruitment process, increasing perceived credibility before onboarding activities began.

## Confidence

**High**

---

# Stage 3 — Opportunity Presentation

## Observation

The recruiter introduced a remote e-commerce opportunity involving:

- Online store management
- Dropshipping
- Commission-based earnings
- Flexible working hours

The recruiter emphasized ease of work and potential income.

## Confidence

**High**

---

# Stage 4 — Training Preparation

## Observation

Rather than requesting immediate participation, the recruiter scheduled a future training session.

This created a structured recruitment experience.

## Confidence

**High**

---

# Stage 5 — Platform Registration

## Observation

The analyst was instructed to:

- Create an account
- Register a store
- Complete onboarding forms
- Submit store information

Registration initially occurred through:

**linkroles.my**

## Confidence

**High**

---

# Stage 6 — Guided Onboarding

## Observation

The recruiter remained actively involved throughout onboarding.

Instructions included:

- Which buttons to click
- How to complete forms
- When to wait for approval
- How to navigate the platform

The analyst completed only actions necessary for observation and documentation.

## Confidence

**High**

---

# Stage 7 — Operational Disruption

## Observation

During onboarding, Google displayed a browser security warning when accessing **linkroles.my**.

The recruiter acknowledged the issue and instructed the analyst to continue using a different platform.

## Confidence

**High**

---

# Stage 8 — Domain Migration

## Observation

The recruiter directed the analyst to:

**unitelmatch.top**

Training resumed using the new domain with minimal interruption.

## Assessment

This demonstrated operational flexibility and continuity.

The investigation does not infer the reason for the migration beyond the observed sequence of events.

## Confidence

**High**

---

# Stage 9 — Cryptocurrency Introduction

## Observation

During the training session, the analyst observed:

- OKX Wallet
- Screenshots of cryptocurrency transfers
- Customer support conversations containing cryptocurrency-related images
- Explanations of commission payments

No financial transactions were initiated by the analyst.

## Confidence

**High**

---

# Stage 10 — Investigation and Evidence Collection

## Observation

Throughout the engagement, the analyst:

- Collected screenshots
- Recorded recruiter communications
- Performed passive OSINT
- Conducted infrastructure analysis
- Avoided providing sensitive information
- Did not participate in cryptocurrency transactions

## Confidence

**High**

---

# Stage 11 — Investigation Closure

## Observation

Following completion of evidence collection, the investigation concluded.

All subsequent analysis was performed offline using the collected evidence.

## Confidence

**High**

---

# Comparison with the Cyber Kill Chain

| Cyber Kill Chain Phase | Observed | Notes |
|------------------------|----------|-------|
| Reconnaissance        | Partial      | Recruiter leveraged an existing job application.                                             |
| Weaponization         | Not Observed | No malware or exploit preparation identified.                                                |
| Delivery              | Partial      | Recruitment messages and onboarding links served as the delivery mechanism.                  |
| Exploitation          | Not Observed | No software vulnerabilities were exploited.                                                  |
| Installation          | Not Observed | No malware or persistence mechanisms observed.                                               |
| Command and Control   | Not Observed | No C2 infrastructure identified.                                                             |
| Actions on Objectives | Partial      | The campaign sought continued user engagement through onboarding and platform participation. |

---

# Behavioral Progression

The campaign exhibited a gradual increase in user commitment:

1. Job application acknowledged.
2. Recruiter established rapport.
3. Employment opportunity presented.
4. Training session scheduled.
5. Platform registration requested.
6. Guided onboarding completed.
7. Browser warning encountered.
8. Alternate platform introduced.
9. Cryptocurrency-related workflow demonstrated.

Each stage built upon the previous one, reducing friction and increasing engagement.

---

# Defensive Opportunities by Lifecycle Stage

| Lifecycle Stage | Defensive Opportunity |
|-----------------|-----------------------|
| Recruiter Contact           | Verify recruiter identity independently.                                                |
| Opportunity Presentation    | Research company reputation before proceeding.                                          |
| Platform Registration       | Assess domain age and reputation.                                                       |
| Guided Onboarding           | Monitor unusual account creation on newly registered domains.                           |
| Browser Warning             | Treat browser warnings as high-confidence security signals.                             |
| Domain Migration            | Investigate unexpected changes in onboarding platforms.                                 |
| Cryptocurrency Introduction | Exercise additional caution when cryptocurrency becomes part of an employment workflow. |

---

# Analytical Assessment

The observed campaign followed a structured and consistent progression from recruitment through onboarding.

Rather than relying on technical exploitation, the campaign emphasized user interaction, recruiter guidance, and incremental commitment.

The immediate migration to a second operational domain after a browser warning demonstrated adaptability within the observed workflow.

No evidence was collected indicating malware delivery, exploitation of software vulnerabilities, or post-compromise activity.

Accordingly, the lifecycle is best characterized as a recruiter-led social engineering campaign supported by coordinated web infrastructure.

---

# Key Findings

1. The campaign unfolded through a clearly defined sequence of recruiter-led interactions.
2. Multiple domains supported different stages of the onboarding process.
3. Browser security warnings preceded a transition to an alternate platform.
4. Cryptocurrency-related activity was introduced only after user engagement had been established.
5. The investigation remained entirely observational and did not involve financial participation or unauthorized activity.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-002-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-002-01.png), [EV-003-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-01.png), [EV-003-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-02.png), [EV-003-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-03.png), [EV-003-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-04.png), [EV-003-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-05.png), [EV-003-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-06.png), [EV-003-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-07.png), [EV-003-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-08.png), [EV-003-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-09.png), [EV-003-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-10.png), [EV-003-11](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-11.png), [EV-003-12](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-12.png), [EV-003-13](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-13.png), [EV-003-14](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-14.png), [EV-003-15](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-15.png), [EV-003-16](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-16.png), [EV-003-17](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-17.png), [EV-003-18](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-18.png), [EV-004-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-01.png), [EV-004-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-02.png), [EV-004-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-03.png), [EV-004-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-04.png), [EV-004-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-05.png), [EV-004-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-004-06.png), [EV-005-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-01.png), [EV-005-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-02.png), [EV-005-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-03.png), [EV-005-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-04.png), [EV-005-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-05.png), [EV-005-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-06.png), [EV-005-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-07.png) | Recruiter communications          |
| EV-081 | Investigation timeline            |
| [EV-005-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-01.png), [EV-005-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-02.png), [EV-005-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-03.png), [EV-005-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-04.png), [EV-005-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-05.png), [EV-005-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-06.png), [EV-005-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-005-07.png) | Chat              | Registration instructions     | Collected |
| [EV-006-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-006-01.png), [EV-006-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-006-02.png), [EV-006-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-006-03.png), [EV-006-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-006-04.png), [EV-006-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-006-05.png) | Platform registration screenshots |
| [EV-012-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-012-01.png) | Browser warning                   |
| [EV-006-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-006-01.png), [EV-013-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-013-01.png) | Domain migration observations, [EV-013-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-013-02.png)     |
| [EV-036-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-01.png), [EV-036-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-02.png), [EV-036-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-036-03.png) | Cryptocurrency observations       |
| [EV-034-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-01.png), [EV-034-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-02.png), [EV-034-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-03.png), [EV-034-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-04.png), [EV-034-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-05.png), [EV-034-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-06.png), [EV-034-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-07.png), [EV-034-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-08.png), [EV-034-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-034-09.png) | Technical infrastructure analysis |

---

# Confidence Assessment

| Lifecycle Stage | Confidence |
|-----------------|------------|
| Initial Contact | High |
| Rapport Building | High |
| Opportunity Presentation | High |
| Platform Registration | High |
| Guided Onboarding | High |
| Browser Warning | High |
| Domain Migration | High |
| Cryptocurrency Introduction | High |
| Campaign Conclusion | High |

---

# Related Documents

- [Campaign_Overview.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Campaign_Overview.md)
- [Investigation_Timeline.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Investigation_Timeline.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Social_Engineering_Analysis.md)
- [MITRE_ATT&CK_Mapping.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/MITRE_ATT%26CK_Mapping.md)
- [Diamond_Model.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Diamond_Model.md)
- [Indicators_of_Compromise.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Indicators_of_Compromise.md)
- [Detection_Opportunities.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Detection_Opportunities.md)
- [Intelligence_Gaps.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Intelligence_Gaps.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)
- [Lessons_Learned.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Lessons_Learned.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     