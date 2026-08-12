# Reputation Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document evaluates the publicly observable reputation of the domains identified during the investigation.

Reputation data was collected from publicly available security services, search engines, browser security mechanisms, and analyst observations.

The objective is to document externally observable trust indicators without drawing conclusions beyond the available evidence.

---

# Scope

Domains analyzed:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

---

# Collection Methodology

The following reputation sources were consulted where applicable:

- Google Safe Browsing
- Browser security warnings
- Search engine results
- URL reputation services
- Community reputation
- VirusTotal
- URLScan

No active interaction with the domains beyond normal browser access was performed.

---

# Domain: occupationoasis.com

## Search Engine Visibility

The domain was publicly accessible and indexed during the investigation.

No browser security warnings were observed during normal access.

---

## Browser Reputation

No browser-generated security warnings were observed during collection.

---

## Public Reputation

No publicly observable reputation indicators identifying the domain as malicious were identified during the investigation.

This observation should not be interpreted as evidence of legitimacy.

---

## Assessment

At the time of collection, publicly observable reputation information for `occupationoasis.com` appeared neutral.

No positive or negative reputation signals sufficient to influence attribution were identified.

---

# Domain: linkroles.my

## Search Engine Visibility

The domain was publicly accessible during the investigation.

---

## Browser Reputation

During the investigation, Google displayed a browser security warning indicating that the website was considered potentially dangerous.

Following this warning, the recruiter directed the analyst to a different domain (`unitelmatch.top`) to continue the onboarding process.

This sequence of events was directly observed by the analyst.

---

## Public Reputation

The analyst observed a browser-based warning associated with the domain.

No independent conclusion regarding the underlying reason for the warning is made in this report.

---

## Assessment

The observed browser warning represents a notable reputation signal because it directly influenced the operational workflow.

The recruiter responded by directing the analyst to an alternative domain after the warning appeared.

This observation is documented factually without attributing intent.

---

# Domain: unitelmatch.top

## Search Engine Visibility

The domain was publicly accessible during the investigation.

---

## Browser Reputation

No browser-generated security warnings were observed during the period of collection.

---

## Public Reputation

No publicly observable reputation indicators identifying the domain as malicious were identified during the investigation.

This observation should not be interpreted as evidence of legitimacy.

---

## Assessment

At the time of collection, the domain did not generate observable browser security warnings.

No additional public reputation indicators were identified.

---

# Reputation Timeline

| Date | Observation |
|------|-------------|
| Recruitment              | Analyst applied for remote role on occupationoasis.com                    |
| During onboarding        | Analyst redirected to linkroles.my                                        |
| Browser warning observed | Google displayed a dangerous site warning for linkroles.my                |
| Following warning        | Recruiter directed analyst to unitelmatch.top                             |

---

# Comparative Reputation Assessment

| Feature | occupationoasis.com | linkroles.my | unitelmatch.top |
|---------|---------------------|--------------|-----------------|
| Browser Warning Observed | No                  | Yes                      | No                              |
| Search Visibility        | Yes                 | Yes                      | Yes                             |
| Operationally Used       | Initial recruitment | Initial onboarding       | Replacement onboarding platform |
| Reputation Observation   | Neutral             | Browser warning observed | Neutral                         |

---

# Operational Observations

The analyst observed the following workflow:

1. Initial contact occurred through the recruitment website.

2. The onboarding process was conducted through `linkroles.my`.

3. After Google displayed a browser warning for `linkroles.my`, the recruiter instructed the analyst to continue using `unitelmatch.top`.

This sequence was directly observed during the investigation.

No inference is made regarding the reason for the change beyond the documented observations.

---

# Reputation Intelligence Assessment

The collected evidence indicates differing observable reputation profiles across the investigated domains.

`occupationoasis.com` did not generate browser security warnings during the investigation.

`linkroles.my` generated a Google browser warning that interrupted the onboarding process. Following this event, the recruiter immediately instructed the analyst to migrate to `unitelmatch.top`.

`unitelmatch.top` did not generate comparable browser warnings during the observation period.

These observations are limited to the investigation period and should not be interpreted as definitive indicators of legitimacy or maliciousness.

---

# Key Observations

The following observations are supported by collected evidence:

1. A Google browser warning was observed for `linkroles.my`.

2. Following the warning, the recruiter directed the analyst to `unitelmatch.top`.

3. No comparable browser warning was observed for `occupationoasis.com`.

4. No comparable browser warning was observed for `unitelmatch.top` during the investigation.

5. The operational workflow changed immediately after the browser warning was encountered.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-037-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-037-01.png) | Browser warning for linkroles.my                              |
| [EV-038-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-038-01.png) | Recruiter instructions directing migration to unitelmatch.top    |
| [EV-039-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-039-01.png) | Browser observations during investigation                      |
| [EV-040-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-040-01.png) | Search engine observations                              |

---

# Confidence Assessment

| Finding | Confidence |
|---------|------------|
| Google browser warning observed for linkroles.my                    | High |
| Recruiter redirected analyst to unitelmatch.top                     | High |
| No browser warning observed for occupationoasis.com                 | High |
| No browser warning observed for unitelmatch.top during collection   | High |
| Reputation observations accurately reflect the investigation period | High |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Domain_Analysis.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/DNS_Analysis.md)
- [Certificate_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Certificate_Analysis.md)
- [Infrastructure_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Infrastructure_Analysis.md)
- [Technology_Stack.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Technology_Stack.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Social_Engineering_Analysis.md)
- [Investigation_Timeline.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/docs/Investigation_Timeline.md)
- [Findings.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/docs/Findings.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store     
