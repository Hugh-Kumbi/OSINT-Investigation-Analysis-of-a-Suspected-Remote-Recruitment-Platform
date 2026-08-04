# Investigation Timeline

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Purpose

This timeline documents the sequence of events observed throughout the investigation.

It records recruiter interactions, investigator actions, technical observations, infrastructure changes, and evidence collection in chronological order.

Dates and times are presented using the best available evidence. Where exact timestamps are unavailable, approximate dates are clearly identified.

---

# Timeline

| Event ID | Date / Time | Event | Evidence |
|----------|-------------|-------|----------|
| EVT-001 | July 2026 | Remote position identified on Occupation Oasis | EV-001 |
| EVT-002 | July 2026 | Application submitted | EV-001 |
| EVT-003 | Shortly after application | Recruiter initiated contact | EV-002 |
| EVT-004 | Same conversation | Remote e-commerce position explained | EV-003 |
| EVT-005 | Same conversation | Compensation model discussed | EV-004 |
| EVT-006 | Same conversation | Recruiter introduced linkroles.my | EV-009 |
| EVT-007 | Same session | Account registration completed | EV-006 |
| EVT-008 | Same session | Store profile created | EV-007 |
| EVT-009 | Same session | Identity verification requested | EV-008 |
| EVT-010 | During OSINT investigation | Google Safe Browsing warning observed | EV-012 |
| EVT-011 | After warning | Recruiter introduced unitelmatch.top | EV-013 |
| EVT-012 | Following platform transition | OSINT investigation expanded to include new domain | EV-015 |

---

# Detailed Timeline

---

## EVT-001 – Remote Position Identified

### Description

The investigator located a remote employment opportunity advertised through Occupation Oasis.

### Investigator Action

Reviewed the advertised position and submitted an application.

### Evidence

- EV-001

### Confidence

High

---

## EVT-002 – Recruiter Contact

### Description

Following the application, a recruiter initiated direct communication regarding the advertised position.

The recruiter introduced a remote e-commerce opportunity involving online store management.

### Investigator Action

Maintained all communications and preserved screenshots.

### Evidence

- EV-002

### Confidence

High

---

## EVT-003 – Position Explanation

### Description

The recruiter described the proposed workflow, including:

- store management
- order processing
- customer interaction
- commission-based compensation

### Investigator Action

Documented all stated responsibilities.

### Evidence

- EV-003
- EV-004

### Confidence

High

---

## EVT-004 – Registration Portal Introduced

### Description

The recruiter instructed the investigator to register an account using:

linkroles.my

The investigator completed registration for documentation purposes.

### Investigator Action

Captured screenshots of the onboarding process.

### Evidence

- EV-006
- EV-009

### Confidence

High

---

## EVT-005 – Store Configuration

### Description

Following registration, the platform required creation of a storefront profile.

Observed fields included:

- Store Name
- Store Description
- Supporting documentation

### Investigator Action

Captured screenshots without submitting genuine personal information.

### Evidence

- EV-007

### Confidence

High

---

## EVT-006 – Identity Verification Request

### Description

The onboarding workflow requested identity verification documentation.

Examples included:

- government-issued identification
- utility bill

### Investigator Action

The investigator did not provide authentic identity documents.

Instead, the request was documented as part of the investigation.

### Evidence

- EV-008

### Confidence

High

---

## EVT-007 – Google Safe Browsing Warning

### Description

While conducting passive OSINT analysis, the investigator observed a Google Safe Browsing warning associated with the onboarding platform.

### Investigator Action

Preserved the browser warning and suspended further interaction with the original platform pending investigation.

### Evidence

- EV-012

### Confidence

High

---

## EVT-008 – Platform Transition

### Description

Following the browser warning, the recruiter instructed the investigator to continue using a different domain:

unitelmatch.top

### Investigator Action

Documented the newly introduced domain and added it to the investigation scope.

### Evidence

- EV-013

### Confidence

High

---

## EVT-009 – Investigation Expansion

### Description

The investigation expanded beyond recruiter communications to include:

- WHOIS analysis
- DNS analysis
- Infrastructure analysis
- Technology fingerprinting
- Certificate Transparency
- Reputation analysis

### Investigator Action

Created dedicated documentation for each investigative workstream.

### Evidence

- EV-011
- EV-015

### Confidence

High

---

# Infrastructure Evolution

```text
OccupationOasis.com
        │
Application Submitted
        │
Recruiter Contact
        │
linkroles.my
        │
Account Registration
        │
Store Creation
        │
Identity Verification Requested
        │
Google Safe Browsing Warning
        │
Recruiter Introduces
unitelmatch.top
        │
Expanded Technical Investigation
```

---

# Evidence Summary

| Evidence ID | Description |
|-------------|-------------|
| EV-001 | Occupation Oasis job advertisement |
| EV-002 | Initial recruiter communication |
| EV-003 | Job description |
| EV-004 | Compensation discussion |
| EV-006 | Registration portal |
| EV-007 | Store profile page |
| EV-008 | Identity verification request |
| EV-009 | linkroles.my URL |
| EV-011 | WHOIS records |
| EV-012 | Google Safe Browsing warning |
| EV-013 | unitelmatch.top introduction |
| EV-015 | OSINT findings for replacement domain |

---

# Timeline Assessment

The investigation identified a structured onboarding workflow that progressed through multiple stages, including recruiter engagement, account registration, storefront setup, and identity verification requests.

A notable development occurred when the initial onboarding platform was replaced with a different domain after the investigator observed a Google Safe Browsing warning. The platform transition was communicated directly by the recruiter and was incorporated into the ongoing technical investigation.

The timeline documents observed events only and does not attribute intent beyond what is supported by the collected evidence.

---

# Related Documents

- [Campaign_Overview.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Campaign_Overview.md)
- [Methodology.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Methodology.md)
- [Investigation_Log.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Investigation_Log.md)
- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [Infrastructure_Evolution.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure_Evolution.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Project Status:**    ✅ COMPLETE        
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     
**Classification:**    Educational Cybersecurity Investigation Documentation