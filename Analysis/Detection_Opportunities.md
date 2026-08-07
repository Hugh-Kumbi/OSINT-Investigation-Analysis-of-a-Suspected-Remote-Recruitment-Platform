# Detection Opportunities

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document identifies potential detection opportunities derived from the investigation.

Rather than relying solely on domain-based indicators, the focus is on detecting behavioral patterns, infrastructure characteristics, and operational workflows that could indicate similar recruitment campaigns in the future.

The recommendations are intended for Security Operations Center (SOC) analysts, threat hunters, and detection engineers.

---

# Scope

Detection opportunities are derived from:

- Recruiter interactions
- DNS analysis
- Infrastructure analysis
- Reputation analysis
- Social engineering observations
- Technology stack analysis
- MITRE ATT&CK mapping

---

# Detection Strategy

Detection opportunities are grouped into:

- Network Detection
- DNS Detection
- Proxy/Web Gateway Detection
- SIEM Correlation
- Endpoint Detection
- Threat Hunting
- User Awareness

---

# Detection Opportunity 1 — Newly Registered Domains

## Observation

Two operational domains (`linkroles.my` and `unitelmatch.top`) were registered only days before being used during the onboarding process.

## Detection Logic

Alert when users interact with domains registered within a defined time window (for example, the previous 30–90 days), particularly when those domains are associated with employment or financial workflows.

## MITRE ATT&CK

- T1583.001 – Acquire Infrastructure: Domains

## Data Sources

- Passive DNS
- WHOIS
- DNS Logs
- Proxy Logs

## Detection Priority

**High**

---

# Detection Opportunity 2 — Multiple Related Domains

## Observation

The onboarding process transitioned across multiple domains while maintaining a consistent workflow.

Observed sequence:

```
occupationoasis.com
        ↓
linkroles.my
        ↓
unitelmatch.top
```

## Detection Logic

Identify users accessing multiple newly observed domains that share similar themes, branding, or operational workflows within a short time period.

## MITRE ATT&CK

- T1583.001
- T1204

## Detection Priority

**High**

---

# Detection Opportunity 3 — Domain Migration

## Observation

The recruiter instructed the analyst to move to another domain immediately after a browser warning.

## Detection Logic

Alert on rapid user transitions from one external domain to another after access failures or security warnings.

## Data Sources

- Browser telemetry
- Proxy logs
- DNS logs
- Web gateway logs

## Detection Priority

**High**

---

# Detection Opportunity 4 — Browser Security Warnings

## Observation

Google displayed a warning for `linkroles.my`.

## Detection Logic

Monitor enterprise browser telemetry for Safe Browsing or SmartScreen warnings and correlate them with user browsing activity.

## Data Sources

- Chrome Enterprise
- Microsoft Defender
- Browser security events
- Web proxy

## Detection Priority

**High**

---

# Detection Opportunity 5 — Cryptocurrency Platforms During Recruitment

## Observation

During onboarding, cryptocurrency-related activity and the OKX Wallet platform were observed.

## Detection Logic

Flag workflows in which users transition directly from recruitment platforms to cryptocurrency exchanges or wallet services.

## Data Sources

- Proxy logs
- DNS logs
- CASB
- Browser telemetry

## Detection Priority

**Medium**

---

# Detection Opportunity 6 — Multiple Cloud Providers

## Observation

The infrastructure used both Amazon Web Services and Cloudflare.

## Detection Logic

Cloud infrastructure alone is **not** suspicious.

Instead, correlate cloud-hosted infrastructure with:

- newly registered domains
- recruitment themes
- browser warnings
- rapid domain transitions

## Detection Priority

**Low**

---

# Detection Opportunity 7 — Recruiter-Led Sequential Navigation

## Observation

The recruiter instructed the analyst step-by-step throughout the onboarding process.

## Detection Logic

Monitor for repeated navigation patterns involving:

- account creation
- profile completion
- financial onboarding
- repeated redirection

This detection is more suitable for user awareness or browser telemetry than traditional network signatures.

## Detection Priority

**Medium**

---

# SIEM Correlation Opportunities

## Example Correlation Rule

Alert when all of the following occur within 24 hours:

- User accesses a newly registered domain.
- Browser records a security warning.
- User accesses a second domain.
- User accesses cryptocurrency-related websites.

Risk Score:

High

---

# Example Splunk SPL

```spl
index=proxy

| stats count by user,url

| lookup newly_registered_domains domain OUTPUT registration_date

| where registration_date > relative_time(now(), "-30d")

| table _time,user,url
```

Purpose:

Identify user activity involving recently registered domains.

---

# Example Microsoft Sentinel (KQL)

```kusto
DeviceNetworkEvents
| where RemoteUrl contains ".top"
   or RemoteUrl contains ".my"
| summarize Count=count() by DeviceName, RemoteUrl
```

Purpose:

Identify connections to domains matching observed campaign patterns.

---

# Example Sigma Rule

```yaml
title: Access to Newly Registered Recruitment Domains

id: cti-osint-001

status: experimental

logsource:
  category: proxy

detection:

  selection:

    url|contains:

      - occupationoasis

      - linkroles

      - unitelmatch

  condition: selection

level: medium

tags:

- attack.resource-development

- attack.initial-access
```

Purpose:

Demonstrate how campaign-specific domains could be monitored.

---

# Threat Hunting Opportunities

Potential hunt hypotheses include:

### Hunt 1

Users accessing multiple newly registered domains within one browsing session.

---

### Hunt 2

Users visiting recruitment websites followed by cryptocurrency exchanges.

---

### Hunt 3

Repeated browser security warnings followed by successful access to alternative domains.

---

### Hunt 4

Employees interacting with websites hosted behind Cloudflare shortly after domain registration.

Cloudflare itself should **not** be treated as malicious; this hunt should rely on correlation with other indicators.

---

### Hunt 5

Domains lacking MX records but requesting account registration.

---

# User Awareness Opportunities

Training material should encourage users to:

- Verify recruiter identities independently.
- Be cautious when redirected to alternative domains.
- Treat browser security warnings seriously.
- Independently verify remote job platforms before creating accounts.
- Report unexpected requests involving cryptocurrency or financial onboarding.

---

# Detection Limitations

The following were **not observed** during the investigation:

- Malware delivery
- Command-and-control traffic
- Exploit activity
- Payload downloads
- Credential theft
- File execution
- Persistence mechanisms

As a result, traditional endpoint detection signatures are unlikely to identify campaigns of this nature.

Behavioral analytics and user awareness provide greater detection value.

---

# ATT&CK Data Sources

| ATT&CK Data Source | Relevance |
|--------------------|-----------|
| DNS | High |
| Network Traffic | High |
| Web Requests | High |
| Browser Telemetry | High |
| User Account Creation | Medium |
| Cloud Service Logs | Medium |
| Email | Low (not observed) |
| File Monitoring | Low (not observed) |
| Process Creation | Not observed |

---

# Detection Prioritization

| Detection Opportunity | Priority |
|------------------------|----------|
| Newly Registered Domains | High |
| Domain Migration | High |
| Browser Security Warnings | High |
| SIEM Correlation | High |
| Threat Hunting | Medium |
| Cryptocurrency Workflow Correlation | Medium |
| Cloud Infrastructure Correlation | Low |
| Static IOC Matching | Low |

---

# Analytical Assessment

The investigation demonstrates that this type of campaign is better detected through **behavioral correlation** than through static indicators.

While domains and IP addresses may change, the observed workflow exhibited several consistent characteristics:

- Use of recently registered domains.
- Structured recruiter-led onboarding.
- Migration between operational domains.
- Reliance on legitimate cloud infrastructure.
- Browser warning followed by immediate platform transition.
- Introduction of cryptocurrency during onboarding.

Organizations implementing behavioral analytics, DNS monitoring, browser telemetry, and user awareness programs would be better positioned to identify similar campaigns than those relying solely on blocklists.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| EV-067 | Domain registration analysis |
| EV-068 | DNS and infrastructure analysis |
| EV-069 | Browser warning observations |
| EV-070 | Recruiter communications |
| EV-071 | Social engineering workflow |
| EV-072 | Cryptocurrency observations |

---

# Confidence Assessment

| Detection Category | Confidence |
|--------------------|------------|
| DNS-based detections | High |
| Behavioral detections | High |
| Browser telemetry | High |
| Threat hunting hypotheses | Medium |
| Endpoint detections | Low (limited evidence) |
| Malware detections | Not Applicable |

---

# Related Documents

- [Indicators_of_Compromise.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Indicators_of_Compromise.md)
- [Social_Engineering_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Social_Engineering_Analysis.md)
- [MITRE_ATT&CK_Mapping.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/MITRE_ATT%26CK_Mapping.md)
- [Diamond_Model.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Analysis/Diamond_Model.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     