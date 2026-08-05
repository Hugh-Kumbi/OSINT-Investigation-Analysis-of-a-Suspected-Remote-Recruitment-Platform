# Methodology

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Version:** 1.0

---

# Purpose

This document describes the methodology used throughout the investigation.

The objective of establishing a documented methodology is to ensure that evidence collection, analysis, reporting, and conclusions are performed in a consistent, repeatable, and evidence-based manner.

The methodology combines industry-recognized cybersecurity investigation practices with passive Open Source Intelligence (OSINT) techniques appropriate for publicly accessible information.

---

# Investigation Principles

The investigation was conducted according to the following principles:

- Evidence before conclusion
- Passive information gathering
- Repeatable methodology
- Documentation of every significant action
- Clear separation of facts, observations, assessments, and hypotheses
- Respect for legal and ethical boundaries
- Protection of personal information through redaction where appropriate

No conclusions are presented unless supported by collected evidence.

---

# Scope

The investigation focuses on publicly observable information relating to a remote recruitment workflow.

Activities included:

- Recruiter communication analysis
- Website observation
- Domain intelligence
- Infrastructure analysis
- Passive reputation analysis
- Website technology identification
- Social engineering assessment

The investigation excludes:

- Unauthorized access
- Authentication bypass
- Exploitation of vulnerabilities
- Malware execution
- Active network scanning against third-party infrastructure
- Service disruption

---

# Investigation Lifecycle

The investigation followed the lifecycle below.

```text
Case Initiation
        │
        ▼
Evidence Preservation
        │
        ▼
Recruiter Communication Analysis
        │
        ▼
OSINT Collection
        │
        ▼
Domain Intelligence
        │
        ▼
Infrastructure Analysis
        │
        ▼
Technology Fingerprinting
        │
        ▼
Reputation Assessment
        │
        ▼
Social Engineering Analysis
        │
        ▼
Risk Assessment
        │
        ▼
Reporting
```

---

# Phase 1 – Case Initiation

The investigation began after the analyst applied for a remote position advertised through the Occupation Oasis recruitment platform.

A case file was created to document:

- Investigation scope
- Objectives
- Evidence
- Findings
- Timeline

Every subsequent activity was recorded within the investigation log.

---

# Phase 2 – Evidence Preservation

Evidence was preserved immediately upon collection whenever possible.

Examples include:

- Recruiter communications
- Screenshots
- Registration URLs
- Onboarding instructions
- WHOIS results
- DNS records
- Browser observations

Evidence was assigned unique identifiers to maintain traceability throughout the investigation.

Example:

| Evidence ID | Description |
|-------------|-------------|
| [EV-001-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-01.png), [EV-001-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-02.png), [EV-001-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-03.png), [EV-001-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-001-04.png) | Occupation Oasis job advertisement |
| [EV-002-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-002-01.png) | Initial recruiter communication |
| [EV-009-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-009-01.png) | Registration URL |
| [EV-012-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-012-01.png) | Google Safe Browsing warning |

---

# Phase 3 – Open Source Intelligence Collection

Passive OSINT techniques were used to collect publicly available information relating to the identified infrastructure.

Information sources included:

- WHOIS
- DNS records
- Certificate Transparency logs
- Passive DNS
- VirusTotal
- URLScan
- Google Safe Browsing
- Wappalyzer
- BuiltWith
- Censys
- Shodan 

No authenticated access to third-party systems was attempted.

---

# Phase 4 – Infrastructure Analysis

Each identified domain was analyzed independently.

Areas examined included:

- Registration details
- Registrar
- Domain age
- Hosting provider
- DNS configuration
- TLS certificates
- Technology stack
- Publicly visible infrastructure

Changes in infrastructure over time were documented separately to establish an operational timeline.

---

# Phase 5 – Social Engineering Analysis

Recruiter communications were analyzed to identify recurring themes and techniques observed during the recruitment process.

The analysis focused on:

- Recruitment workflow
- Trust-building techniques
- Financial incentives
- Onboarding process
- Identity verification requests
- Platform transitions

Descriptions are limited to observed behaviors and do not infer intent without supporting evidence.

---

# Phase 6 – Risk Assessment

Each finding was evaluated using a qualitative risk model based on:

- Likelihood
- Potential impact
- Supporting evidence
- Confidence level

Risk assessments are intended to assist readers in prioritizing areas for further investigation rather than to provide definitive conclusions.

---

# Analytical Standards

Throughout the investigation, information is categorized using the following terminology.

## Verified Fact

Information directly supported by collected evidence.

Examples include:

- URLs
- Screenshots
- WHOIS records
- Recruiter messages

---

## Observation

An event personally witnessed during the investigation.

Example:

> The analyst observed a Google Safe Browsing warning when attempting to access the onboarding platform.

---

## Assessment

An analytical interpretation derived from one or more verified facts.

Assessments are clearly identified and include a confidence rating.

---

## Hypothesis

A possible explanation that has not yet been verified.

Hypotheses are presented separately from findings and require additional evidence before being accepted.

---

# Confidence Rating

Each assessment is assigned a confidence level.

| Confidence | Definition |
|------------|------------|
| High   | Supported by multiple independent sources or direct evidence collected during the investigation. |
| Medium | Supported by limited evidence or a combination of observations and OSINT results.                |
| Low    | Preliminary assessment requiring additional corroboration.                                       |

Confidence reflects the strength of the available evidence, not the severity of the finding.

---

# Evidence Handling

Evidence integrity is maintained through:

- Unique evidence identifiers
- Chronological documentation
- Preservation of original screenshots where possible
- Separation of original evidence from analytical notes
- Clear references between findings and supporting evidence

Personally identifiable information unrelated to the investigation is redacted before publication.

---

# Limitations

This investigation has several limitations.

- Only publicly accessible information was collected.
- Infrastructure may change over time.
- WHOIS records may use privacy protection services.
- Reputation services may not reflect real-time changes.
- No access to internal systems or proprietary records was available.

Accordingly, the investigation should be viewed as a point-in-time assessment based on the evidence available during the investigation period.

---

# Ethical Considerations

This investigation was conducted in accordance with responsible cybersecurity research practices.

The investigator did not:

- Attempt unauthorized access
- Exploit vulnerabilities
- Interfere with services
- Impersonate third parties
- Collect unnecessary personal information

The purpose of this investigation is educational, analytical, and professional, demonstrating structured OSINT and threat intelligence techniques.

---

# References

This methodology is informed by publicly available cybersecurity guidance, including:

- NIST Special Publication 800-61 Rev. 2 – *Computer Security Incident Handling Guide*
- NIST Special Publication 800-86        – *Guide to Integrating Forensic Techniques into Incident Response*
- MITRE ATT&CK Framework
- Diamond Model of Intrusion Analysis
- OSINT best practices for passive intelligence collection

These references informed the investigation approach but were adapted to fit the scope of a passive, evidence-based OSINT case study.

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     