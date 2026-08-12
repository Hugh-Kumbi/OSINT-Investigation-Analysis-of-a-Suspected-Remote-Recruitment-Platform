    # Confidence Assessment

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Cyber Threat Intelligence (CTI)

**Status:** Investigation Complete

**Version:** 1.0

---

# Objective

This document evaluates the confidence level associated with the findings presented throughout this investigation.

Confidence assessments distinguish between directly observed evidence and analytical judgments. They also identify assumptions, uncertainties, and limitations that may affect the overall reliability of the investigation.

The goal is to provide transparency regarding how conclusions were reached and where additional evidence would strengthen future assessments.

---

# Confidence Methodology

The following confidence scale is used throughout this investigation.

| Confidence | Definition |
|------------|------------|
| **High**   | Supported by multiple independent sources or direct observations with minimal uncertainty.               |
| **Medium** | Supported by credible evidence but includes analytical interpretation or unresolved uncertainties.       |
| **Low**    | Limited supporting evidence or conclusions based primarily on inference requiring additional validation. |

---

# Sources of Evidence

The investigation relied on multiple independent evidence sources, including:

- Recruiter conversations
- Analyst observations
- Website screenshots
- Browser security warnings
- WHOIS records
- DNS records
- Reverse DNS lookups
- Certificate Transparency logs
- Technology fingerprinting
- Public reputation services
- Passive OSINT

No conclusions were based on a single unsupported source.

---

# Evidence Reliability

| Evidence Source | Reliability | Notes |
|-----------------|-------------|-------|
| Recruiter conversations       | High   | First-hand observations recorded during the investigation.               |
| Screenshots                   | High   | Captured directly by the analyst.                                        |
| DNS records                   | High   | Retrieved from authoritative public sources.                             |
| WHOIS records                 | High   | Public registry information.                                             |
| Certificate Transparency logs | High   | Independent certificate records.                                         |
| Technology fingerprinting     | Medium | Dependent on publicly observable characteristics.                        |
| Browser warning               | High   | Directly observed during the investigation.                              |
| Public reputation services    | Medium | May change over time and should be interpreted alongside other evidence. |

---

# Assessment of Major Findings

## Finding 1 — Multi-Domain Operational Workflow

### Assessment

The recruitment process involved three separate domains:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

### Supporting Evidence

- Recruiter instructions
- Platform screenshots
- DNS analysis
- WHOIS analysis
- Timeline reconstruction

### Confidence

**High**

### Rationale

The domains were directly observed during the investigation and independently verified through technical analysis.

---

## Finding 2 — Structured Recruiter-Led Onboarding

### Assessment

The recruiter followed a structured process designed to guide the analyst through account creation and platform onboarding.

### Supporting Evidence

- Conversation transcripts
- Timeline
- Screenshots
- Analyst notes

### Confidence

**High**

### Rationale

The analyst directly participated in the onboarding process and documented each stage.

---

## Finding 3 — Browser Warning Followed by Domain Migration

### Assessment

A browser warning for `linkroles.my` was immediately followed by recruiter instructions to continue using `unitelmatch.top`.

### Supporting Evidence

- Browser warning
- Recruiter messages
- Timeline
- Screenshots

### Confidence

**High**

### Rationale

The sequence was directly observed and recorded.

The investigation does not infer why the migration occurred beyond the observable evidence.

---

## Finding 4 — Cryptocurrency Introduced During Training

### Assessment

Cryptocurrency-related material formed part of the onboarding process.

### Supporting Evidence

- OKX Wallet interface
- Cryptocurrency screenshots
- Recruiter explanations

### Confidence

**High**

### Rationale

The analyst directly observed cryptocurrency-related content during training.

No financial participation occurred.

---

## Finding 5 — Use of Legitimate Cloud Infrastructure

### Assessment

The observed platforms relied on infrastructure provided by Amazon Web Services and Cloudflare.

### Supporting Evidence

- DNS analysis
- ASN lookup
- Certificate analysis
- Technology fingerprinting

### Confidence

**High**

### Rationale

Infrastructure ownership is directly supported by technical evidence.

However, the use of legitimate cloud services is not, by itself, evidence of malicious activity.

---

## Finding 6 — Coordinated Campaign

### Assessment

The observed workflow appears coordinated across multiple domains and recruiter interactions.

### Supporting Evidence

- Timeline reconstruction
- Infrastructure analysis
- Recruiter communications

### Confidence

**Medium**

### Rationale

The workflow was consistent and structured.

However, the investigation observed only a single recruiter and cannot determine the size or organizational structure behind the campaign.

---

## Finding 7 — Threat Actor Attribution

### Assessment

The investigation cannot reliably attribute the campaign to a specific individual or organization.

### Supporting Evidence

Limited.

### Confidence

**Low**

### Rationale

The recruiter identity could not be independently verified.

Infrastructure alone is insufficient for attribution.

---

# Direct Observations vs Analytical Inference

## Direct Observations

The following findings were directly observed:

- Recruiter communications
- Platform registration
- Browser warning
- Domain migration
- Cryptocurrency demonstrations
- DNS records
- Certificate information
- WHOIS records
- Technology stack
- Infrastructure providers

Confidence:

**High**

---

## Analytical Inferences

The following assessments involve interpretation of the available evidence:

- Campaign coordination
- Operational maturity
- Use of staged social engineering
- Behavioral progression
- Detection opportunities
- Infrastructure relationships

Confidence:

**Medium**

---

## Unresolved Questions

The following areas remain unresolved:

- Recruiter identity
- Organizational structure
- Backend systems
- Cryptocurrency wallets
- Campaign scale
- Additional infrastructure

Confidence:

**Low**

---

# Potential Sources of Bias

The investigation considered the following potential biases:

## Observer Bias

The analyst participated directly in the onboarding process.

Mitigation:

Technical observations were independently verified wherever possible.

---

## Confirmation Bias

There was a possibility of interpreting observations to fit an expected outcome.

Mitigation:

Only evidence directly supported by screenshots, communications, or technical analysis was included.

No unsupported claims were made.

---

## Availability Bias

The investigation relied entirely on publicly accessible information and first-hand observations.

Mitigation:

Conclusions were limited to observable evidence.

---

# Investigation Limitations

This investigation did not include:

- Internal server logs
- Law enforcement intelligence
- Blockchain analytics
- Payment records
- Backend access
- Malware samples
- Source code
- Administrative interfaces
- Private infrastructure information

Consequently, attribution and campaign scope remain limited.

---

# Confidence by Analysis Area

| Analysis Area | Confidence |
|---------------|------------|
| Recruiter Communications    | High   |
| Timeline Reconstruction     | High   |
| DNS Analysis                | High   |
| WHOIS Analysis              | High   |
| Certificate Analysis        | High   |
| Technology Stack            | High   |
| Infrastructure Analysis     | High   |
| Social Engineering Analysis | High   |
| MITRE ATT&CK Mapping        | Medium |
| Diamond Model               | Medium |
| Detection Opportunities     | Medium |
| Campaign Attribution        | Low    |
| Cryptocurrency Attribution  | Low    |
| Campaign Scale              | Low    |

---

# Overall Confidence Assessment

The investigation's strongest conclusions relate to:

- Technical infrastructure
- Recruiter interactions
- Campaign chronology
- Domain relationships
- Social engineering workflow

These conclusions are supported by multiple independent evidence sources and direct analyst observations.

Conclusions regarding attribution, campaign scale, and organizational structure remain tentative due to the absence of corroborating evidence.

---

# Analytical Assessment

Overall confidence in the technical findings is **High**.

Confidence in behavioral assessments is **Medium**, reflecting the analytical interpretation required to connect individual observations into a coherent campaign narrative.

Confidence in attribution is **Low**, as the investigation intentionally avoided speculation beyond the available evidence.

This assessment reflects a fundamental principle of cyber threat intelligence: conclusions should be proportional to the quality and quantity of the available evidence.

---

# Related Documents

- [Methodology.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/docs/Methodology.md)
- [Findings.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/docs/Findings.md)
- [Intelligence_Gaps.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Intelligence_Gaps.md)
- [Attack_Lifecycle.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Attack_Lifecycle.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Social_Engineering_Analysis.md)
- [Diamond_Model.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Diamond_Model.md)
- [MITRE_ATT&CK_Mapping.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/MITRE_ATT%26CK_Mapping.md)
- [Detection_Opportunities.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Detection_Opportunities.md)
- [Indicators_of_Compromise.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Indicators_of_Compromise.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store     
