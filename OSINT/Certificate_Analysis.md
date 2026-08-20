# Certificate Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.2

---

# Objective

This document analyses the TLS/SSL certificates observed across the domains associated with the investigation. The objective is to identify certificate issuance patterns, certificate authorities, Subject Alternative Names (SANs), Certificate Transparency (CT) logs, and relationships that may indicate shared infrastructure or operational practices.

The analysis is based on Certificate Transparency (crt.sh), Censys, browser observations, and passive OSINT.

---

# Domains Analysed

| Domain | Observed Role |
|--------|---------------|
| occupationoasis.com | Recruitment website       |
| linkroles.my        | First operational portal  |
| unitelmatch.top     | Second operational portal |
| unitelmatch.cc      | Third operational portal  |
| unitelmatch.cyou    | Backup operational portal |

---

# Certificate Summary

| Domain | Certificate Authority | Certificate Type | Validity | Observations |
|--------|-----------------------|------------------|----------|--------------|
| occupationoasis.com | Amazon RSA 2048 M01               | AWS Managed        | ~7 months | AWS infrastructure |
| linkroles.my        | Google Trust Services (WE1/WR1)   | Cloudflare Managed | ~3 months | Dual certificates  |
| unitelmatch.top     | Google Trust Services (WE1/WR1)   | Cloudflare Managed | ~3 months | Dual certificates  |
| unitelmatch.cc      | Google Trust Services (WE1/WR1)   | Cloudflare Managed | ~3 months | Dual certificates  |
| unitelmatch.cyou    | Google Trust Services (WE1/WR1)   | Cloudflare Managed | ~3 months | Dual certificates  |

---

# Recruitment Infrastructure

## occupationoasis.com

### Certificate Authority

Amazon RSA 2048 M01

### Validity

29 June 2026

↓

12 January 2027

Approximately seven months.

### Subject Alternative Names

- occupationoasis.com
- *.occupationoasis.com

### Certificate Protocol

TLS 1.3

### Observations

Unlike the operational portals, the recruitment website uses an AWS-managed certificate consistent with Amazon CloudFront hosting.

Historical Certificate Transparency logs also identified expired Let's Encrypt certificates from 2023 and 2024, indicating the domain has undergone multiple certificate renewals prior to the current campaign.

---

# Operational Infrastructure

## linkroles.my

Certificate Authorities

- Google Trust Services WE1
- Google Trust Services WR1

### Validity

19 July 2026

↓

17 October 2026

Approximately three months.

### SANs

- linkroles.my
- *.linkroles.my
- www.linkroles.my

---

## unitelmatch.top

Certificate Authorities

- Google Trust Services WE1
- Google Trust Services WR1
- Let's Encrypt YE2

### Validity

23 July 2026

↓

21 October 2026

Approximately three months.

### SANs

- unitelmatch.top
- *.unitelmatch.top
- www.unitelmatch.top

---

## unitelmatch.cc

Certificate Authorities

- Google Trust Services WE1
- Google Trust Services WR1

### Validity

23 July 2026

↓

21 October 2026

Approximately three months.

### SANs

- www.unitelmatch.cc

Certificate SHA256 fingerprints were collected and preserved as indicators of compromise.

---

## unitelmatch.cyou

Certificate Authorities

- Google Trust Services WE1
- Google Trust Services WR1

### Validity

24 July 2026

↓

22 October 2026

Approximately three months.

### SANs

- www.unitelmatch.cyou

crt.sh recorded both RSA and ECDSA certificates shortly after domain creation.

---

# Certificate Transparency Analysis

Certificate Transparency logs revealed several consistent characteristics across the operational domains.

Observed patterns include:

- Automated certificate issuance.
- Google Trust Services as the primary certificate authority.
- Dual RSA and ECDSA certificates.
- Certificates logged immediately after domain registration.
- Approximately three-month validity periods.
- Certificates issued for individual operational domains rather than a shared wildcard certificate.

These characteristics are consistent with Cloudflare-managed certificate provisioning.

---

# Certificate Timeline

```text
29 Jun 2026

occupationoasis.com
Amazon RSA

────────────────────────────

19 Jul 2026

linkroles.my
Google Trust Services

↓

23 Jul 2026

unitelmatch.top
Google Trust Services

↓

23 Jul 2026

unitelmatch.cc
Google Trust Services

↓

24 Jul 2026

unitelmatch.cyou
Google Trust Services
```

---

# Certificate Comparison

| Feature | OccupationOasis | LinkRoles | UnitelMatch.top | UnitelMatch.cc | UnitelMatch.cyou |
|---------|-----------------|-----------|-----------------|----------------|------------------|
| AWS Certificate       | ✓ | ✗ | ✗ | ✗ | ✗ |
| Google Trust Services | ✗ | ✓ | ✓ | ✓ | ✓ |
| Let's Encrypt History | ✓ | ✗ | ✓ | ✗ | ✗ |
| Dual Certificates     | ✗ | ✓ | ✓ | ✓ | ✓ |
| Wildcard SAN          | ✓ | ✓ | ✓ | ✗ | ✗ |
| HTTP/3                | ✗ | ✓ | ✓ | ✓ | ✓ |
| Cloudflare Managed    | ✗ | ✓ | ✓ | ✓ | ✓ |

---

# Certificate Issuance Pattern

The operational portals exhibit a consistent certificate lifecycle:

1. Domain registered.
2. Cloudflare DNS configured.
3. TLS certificates issued within hours of registration.
4. Dual RSA and ECDSA certificates generated.
5. Certificates published to Certificate Transparency logs.
6. Approximately three-month certificate validity.

This repeated pattern was observed across all operational portals.

---

# Certificate Relationship Analysis

The investigation identified two distinct certificate ecosystems.

## Recruitment Infrastructure

- AWS-managed certificates.
- Amazon CloudFront integration.
- Longer certificate validity.
- Independent certificate lifecycle.

## Operational Infrastructure

- Google Trust Services.
- Cloudflare-managed certificates.
- Automated issuance.
- Short validity periods.
- Consistent provisioning process.
- Uniform certificate architecture.

These observations indicate a common TLS deployment strategy across the operational portals.

---

# Analytical Assessment

The certificate analysis supports the broader infrastructure assessment.

Observed technical consistencies include:

- Common certificate authority.
- Automated certificate issuance.
- Similar certificate validity periods.
- Cloudflare-managed provisioning.
- Uniform TLS configuration.
- Consistent Certificate Transparency logging behaviour.

These characteristics strengthen the correlation between the operational domains while remaining insufficient on their own to establish ownership or attribution.

---

# Screenshots

Include:

## crt.sh

- Certificate search results for each domain.
- Certificate timelines.
- SAN listings.

## Censys

- Certificate observations.
- Certificate fingerprints.
- TLS protocol information.

## Browser

- Certificate viewer.
- TLS connection details.
- Issuer information.

## Certificate Transparency

- Logged certificate entries.
- Validity periods.
- Dual certificate observations.

---

# CHANGELOG

## Version 1.2

- Added certificate analysis for `unitelmatch.cc`.
- Added certificate analysis for `unitelmatch.cyou`.
- Expanded comparison from three to five domains.
- Added certificate issuance timeline.
- Documented Cloudflare-managed certificate provisioning.
- Added certificate relationship analysis.
- Included certificate lifecycle observations.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-019-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-019-01.png) | Certificate Transparency results – occupationoasis.com |
| [EV-020-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-020-01.png) | Certificate Transparency results – linkroles.my        |
| [EV-021-01](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Screenshots/EV-021-01.png) | Certificate Transparency results – unitelmatch.top     |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Domain_Analysis.md)
- [Domain_Relationships.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Domain_Relationships.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/DNS_Analysis.md)
- [Passive_DNS.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Passive_DNS.md)
- [Infrastructure_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Infrastructure_Analysis.md)
- [Technology_Stack.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Technology_Stack.md)
- [Reputation_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Reputation_Analysis.md)
- [Infrastructure_Evolution.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Infrastructure_Evolution.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store     