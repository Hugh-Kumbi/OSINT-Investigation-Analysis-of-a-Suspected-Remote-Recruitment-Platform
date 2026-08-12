# Domain Relationships

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Recruitment Campaign

**Classification:** Open Source Intelligence (OSINT)

**Status:** Investigation Updated

**Version:** 1.1

---

# Purpose

This document correlates the domains identified throughout the investigation.

Rather than analyzing each domain individually, this document focuses on their observed relationships, operational roles, infrastructure similarities, and chronological use during recruiter-led onboarding.

The document does **not** attribute ownership or control of the domains. It records only relationships supported by observed evidence and technical analysis.

---

# Observed Domains

| Domain | Role During Investigation | Status |
|--------|---------------------------|--------|
| occupationoasis.com | Initial recruitment platform  | Observed                       |
| linkroles.my        | Initial onboarding portal     | Replaced                       |
| unitelmatch.top     | Replacement onboarding portal | Replaced                       |
| unitelmatch.cc      | Subsequent onboarding portal  | Replaced after browser warning |
| unitelmatch.cyou    | Backup onboarding portal      | Active during investigation    |

---

# Campaign Domain Progression

The recruiter introduced multiple portals throughout the onboarding process.

```text
occupationoasis.com
        │
        ▼
linkroles.my
        │
 Google Safe Browsing Warning
        │
        ▼
unitelmatch.top
        │
 Google Safe Browsing Warning
        │
        ▼
unitelmatch.cc
        │
 Google Safe Browsing Warning
        │
        ▼
unitelmatch.cyou
```

Each transition occurred during active communication with the recruiter.

---

# Operational Roles

## occupationoasis.com

Observed as the initial recruitment website.

Purpose:

- Job advertisement
- Initial recruiter contact
- Candidate acquisition

No onboarding activities were performed directly through this domain.

---

## linkroles.my

Observed as the first operational platform.

Purpose:

- User registration
- Store creation
- Initial onboarding
- Guided training

Later replaced during the investigation.

---

## unitelmatch.top

Observed as the replacement onboarding platform.

Purpose:

- Continued onboarding
- Store management
- Training
- Platform access

The analyst observed cryptocurrency-related activity while using this portal.

---

## unitelmatch.cc

Observed as a subsequent onboarding platform introduced by the recruiter.

Purpose:

- Continued access to the platform
- Ongoing onboarding

The analyst observed a Google Safe Browsing warning when attempting to access the site.

The recruiter subsequently supplied another portal.

---

## unitelmatch.cyou

Observed as a backup onboarding portal.

Purpose:

- Continued access after browser warning
- Replacement platform
- Ongoing training

The recruiter instructed the analyst to continue using this domain while the reported issue with the previous portal was being investigated.

---

# Timeline of Domain Introduction

| Approximate Order | Domain | How Introduced |
|-------------------|--------|----------------|
| 1 | occupationoasis.com | Public job advertisement                                   |
| 2 | linkroles.my        | Recruiter onboarding instructions                          |
| 3 | unitelmatch.top     | Replacement after browser warning                          |
| 4 | unitelmatch.cc      | Recruiter introduced upgraded portal                       |
| 5 | unitelmatch.cyou    | Recruiter supplied backup portal following browser warning |

---

# Infrastructure Comparison

| Domain | Hosting / CDN | Registrar | Certificate | Notes |
|--------|---------------|-----------|-------------|-------|
| occupationoasis.com | AWS / CloudFront | Amazon Registrar     | AWS Certificate Manager               | Nuxt.js, Vue.js           |
| linkroles.my        | Cloudflare       | Gname.com            | Google Trust Services / Cloudflare    | Vue.js                    |
| unitelmatch.top     | Cloudflare       | Global Asset Domains | Google Trust Services / Let's Encrypt | Vue.js                    |
| unitelmatch.cc      | Cloudflare       | Dynadot Inc          | Google Trust Services /  SSL.com      | Vue.js                    |
| unitelmatch.cyou    | Cloudflare       | Global Asset Domains | SSL.com / Google Trust Services       | Nuxt.js, Vue.js           |

---

# Shared Characteristics

The investigation identified several recurring characteristics across the observed infrastructure.

## Recently Registered Domains

Several onboarding portals were newly registered shortly before their use.

This observation is documented in the WHOIS analysis.

---

## Commercial Cloud Infrastructure

Observed providers included:

- Amazon Web Services
- Amazon CloudFront
- Cloudflare

These services are commonly used by legitimate organizations as well as malicious actors.

Their presence alone is not evidence of malicious activity.

---

## Modern Web Technologies

Observed technologies included:

- Vue.js
- Nuxt.js
- Cloudflare CDN
- Amazon CloudFront
- Google Tag Manager
- Google Analytics
- Browser Insights
- HTTP/3
- QUIC
- TLS 1.3

---

## Valid SSL Certificates

Observed certificate authorities included:

- Google Trust Services
- AWS Certificate Manager
- Let's Encrypt

The presence of valid certificates demonstrates encrypted communications but does not indicate the legitimacy of the platform.

---

## Domain Rotation

The investigation documented repeated migration between onboarding portals.

Observed sequence:

```text
linkroles.my

↓

unitelmatch.top

↓

unitelmatch.cc

↓

unitelmatch.cyou
```

Each transition was initiated by the recruiter.

---

# Behavioral Relationships

Observed recruiter behavior remained consistent despite domain changes.

Common patterns included:

- Guided onboarding
- Scheduled training
- Store registration
- Progressive trust building
- Immediate provision of replacement portals
- Continued communication following browser security warnings

These behaviors remained stable across all observed domains.

---

# Analytical Assessment

Based on the available evidence, the investigation assesses that the identified domains formed part of a single recruiter-led onboarding workflow.

This assessment is supported by:

- Chronological recruiter communications
- Consistent onboarding procedures
- Repeated migration between portals
- Similar operational purpose
- Comparable technical characteristics

The investigation does not attribute ownership or operational control of the domains beyond these observed relationships.

---

# Intelligence Gaps

Additional analysis remains outstanding for:

- unitelmatch.cc
- unitelmatch.cyou

Recommended collection activities include:

- WHOIS
- DNS
- Passive DNS
- Reverse DNS
- SSL certificates
- Certificate Transparency
- Technology stack
- Reputation
- Historical DNS
- Historical certificates

These findings should be incorporated into Version 1.2 if additional evidence becomes available.

---

# Confidence Assessment

| Assessment | Confidence |
|------------|------------|
| Domains participated in the same onboarding workflow              | High   |
| Domains were introduced sequentially by the recruiter             | High   |
| Recruiter supplied replacement portals following browser warnings | High   |
| Infrastructure exhibits recurring technical characteristics       | Medium |
| Domains share common operational management                       | Medium |
| Attribution to a specific threat actor or organization            | Low    |

---

# Related Documents

- [Passive_DNS.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Passive_DNS.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/DNS_Analysis.md)
- [Infrastructure_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Infrastructure_Analysis.md)
- [Certificate_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Certificate_Analysis.md)
- [Technology_Stack.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Technology_Stack.md)
- [Reputation_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Reputation_Analysis.md)
- [Investigation_Timeline.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/docs/Investigation_Timeline.md)
- [Campaign_Overview.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/docs/Campaign_Overview.md)
- [Attack_Lifecycle.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Attack_Lifecycle.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store 