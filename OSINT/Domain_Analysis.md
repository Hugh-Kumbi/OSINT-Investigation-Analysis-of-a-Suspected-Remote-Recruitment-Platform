# Domain Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

---

# Objective

Identify, document, and compare the internet domains observed during the recruitment workflow.

This analysis focuses on domain registration, ownership characteristics, infrastructure relationships, and observed operational roles.

---

# Executive Summary

During the investigation, three primary domains were identified.

Each served a distinct purpose within the observed recruitment workflow.

| Domain | Observed Role | Investigation Status |
|--------|---------------|----------------------|
| occupationoasis.com | Remote job advertisement platform                                    | Investigated        |
| linkroles.my        | Initial onboarding and registration portal                           | Investigated        |
| unitelmatch.top     | Replacement operational platform introduced during the investigation | Under Investigation |

The analyst observed a transition from one operational platform to another after the initial registration portal became problematic.

The reason for this transition has not been independently verified.

---

# Domain Inventory

## Domain 1

### occupationoasis.com

**Observed Purpose**

Remote recruitment website where the analyst initially applied for employment.

---

## Domain 2

### linkroles.my

**Observed Purpose**

Platform used during the initial onboarding process.

The recruiter instructed the analyst to register an account using this domain.

---

## Domain 3

### unitelmatch.top

**Observed Purpose**

Platform introduced later in the investigation after issues were encountered with the original onboarding portal.

The recruiter instructed the analyst to continue using this domain.

---

# Infrastructure Evolution

Observed workflow:

```

OccupationOasis.com

↓

Recruiter Contact

↓

linkroles.my

↓

Google Safe Browsing Warning Observed

↓

Recruiter directs analyst

↓

unitelmatch.top

```

---

# Technical Observations

At the time of writing:

- Three independent domains have been identified.
- Multiple platforms were used throughout the recruitment workflow.
- The operational platform changed during the investigation.
- Additional infrastructure analysis is ongoing.

These observations are factual descriptions of the investigation and should not be interpreted as evidence of malicious activity without additional corroborating evidence.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-001-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-01.png), [EV-001-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-02.png), [EV-001-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-03.png), [EV-001-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-04.png) | Occupation Oasis job advertisement            |
| [EV-002-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-002-01.png)      | Recruiter communication                       |
| [EV-009-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-009-01.png)      | linkroles.my registration URL                 |
| [EV-012-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-012-01.png)      | Google Safe Browsing warning                  |
| [EV-03-15](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-003-15.png)      | Recruiter message introducing unitelmatch.top |

---

# Confidence Assessment

**Confidence:** High

The findings are supported by:

- Recruiter communications
- Screenshots
- Browser observations
- URLs collected during the investigation

---

# Related Documents

- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/DNS_Analysis.md)
- [Infrastructure.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Infrastructure_Evolution.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure_Evolution.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store     