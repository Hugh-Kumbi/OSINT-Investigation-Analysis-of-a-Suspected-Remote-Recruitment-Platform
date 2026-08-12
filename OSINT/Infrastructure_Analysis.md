# Infrastructure Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document analyzes the hosting and network infrastructure associated with the domains identified during the investigation.

The objective is to document publicly observable infrastructure characteristics, identify similarities and differences between the domains, and establish a technical baseline for later threat intelligence assessments.

Infrastructure observations are based entirely on publicly available information collected during the investigation.

---

# Scope

Domains analyzed:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

---

# Collection Methodology

Infrastructure information was collected using publicly available sources, including:

- WHOIS records
- DNS lookups
- Reverse DNS lookups
- Certificate Transparency logs
- ASN information
- Hosting provider identification

No active probing or unauthorized interaction with the infrastructure was performed.

---

# Domain: occupationoasis.com

## Domain Registration

| Property | Value |
|----------|-------|
| Creation Date | 29 Jun 2026                 |
| Updated Date  | 29 Jun 2026                 |
| Registrar     | Amazon Registrar, Inc.      |
| WHOIS Privacy | Enabled (`Whoisprivacy: 1`) |

### Assessment

The domain was registered through Amazon Registrar and WHOIS privacy protection was enabled at the time of collection.

---

## Hosting Infrastructure

| Property | Value |
|----------|-------|
| Hosting Provider | Amazon Web Services (AWS)                           |
| DNS Provider     | Amazon Route 53                                     |
| ASN              | AS16509                                             |
| CDN              | Amazon CloudFront (observed)                        |
| IPv4             | 18.239.36.77                                        |
| WWW Addresses    | 65.8.180.42, 65.8.180.52, 65.8.180.92, 65.8.180.104 |

---

## Reverse DNS

Observed hostnames:

- server-18-239-36-15.ams58.r.cloudfront.net
- server-18-239-36-62.ams58.r.cloudfront.net
- server-18-239-36-99.ams58.r.cloudfront.net

### Observation

The reverse DNS entries correspond to Amazon CloudFront edge infrastructure located in Amsterdam.

The reverse lookup for `18.239.36.77` did not return a hostname during collection.

---

## Infrastructure Assessment

Observed infrastructure is consistent with an AWS-hosted website using:

- Amazon Registrar
- Amazon Route 53
- Amazon CloudFront
- Amazon-owned IP address space

These observations indicate a largely Amazon-managed deployment.

---

# Domain: linkroles.my

## Domain Registration

| Property | Value |
|----------|-------|
| Creation Date | 19 Jul 2026                           |
| Updated Date  | 19 Jul 2026                           |
| Registrar     | Gname.com Pte. Ltd.                   |
| WHOIS Privacy | Enabled (Registrant details redacted) |

### Assessment

WHOIS information was extensively redacted, limiting attribution based on registration records.

---

## Hosting Infrastructure

| Property | Value |
|----------|-------|
| Hosting Provider | Cloudflare (observed edge infrastructure) |
| DNS Provider     | Cloudflare                                |
| ASN              | AS13335                                   |
| IPv4             | 188.114.97.0                              |
| IPv6             | 2a06:98c1:3120::0, 2a06:98c1:3121::0      |

---

## Reverse DNS

Observed results:

- 188.114.97.0      → no descriptive hostname returned
- 188.114.96.0      → no descriptive hostname returned
- 2a06:98c1:3120::0 → no descriptive hostname returned
- 2a06:98c1:3121::0 → no descriptive hostname returned
- 108.162.192.61    → alina.ns.cloudflare.com

### Observation

Most Cloudflare edge addresses did not resolve to descriptive reverse DNS hostnames. One observed address resolved to the authoritative Cloudflare name server `alina.ns.cloudflare.com`.

This is consistent with Cloudflare-managed infrastructure.

---

## Infrastructure Assessment

The observed infrastructure indicates that Cloudflare provides:

- Authoritative DNS
- Reverse proxy / edge infrastructure
- TLS certificate management (supported by Certificate Analysis)

The origin infrastructure behind Cloudflare could not be identified using the collected evidence.

---

# Domain: unitelmatch.top

## Domain Registration

| Property | Value |
|----------|-------|
| Creation Date | 23 Jul 2026                           |
| Updated Date  | 23 Jul 2026                           |
| Registrar     | GLOBAL ASSET DOMAINS INC.             |
| WHOIS Privacy | Enabled (Registrant details redacted) |

### Assessment

WHOIS information was extensively redacted, preventing identification of the registrant through publicly available records.

---

## Hosting Infrastructure

| Property | Value |
|----------|-------|
| Hosting Provider | Cloudflare (observed edge infrastructure) |
| DNS Provider     | Cloudflare                                |
| ASN              | AS13335                                   |
| IPv4             | 188.114.96.0                              |
| IPv6             | 2a06:98c1:3120::0, 2a06:98c1:3121::0      |

---

## Reverse DNS

Observed results:

- 104.21.22.200  → no descriptive hostname returned
- 172.67.206.231 → no descriptive hostname returned

### Observation

No descriptive reverse DNS hostnames were returned for the observed edge addresses during collection.

This is consistent with traffic being routed through Cloudflare's edge network rather than exposing origin infrastructure.

---

## Infrastructure Assessment

The observed infrastructure is technically similar to that of `linkroles.my`, including:

- Cloudflare DNS
- Cloudflare edge network
- AS13335
- IPv6 support
- WHOIS privacy protection

These similarities are documented as technical observations. Additional evidence would be required to determine whether the domains are operationally related.

---

# Comparative Infrastructure Analysis

| Feature | occupationoasis.com | linkroles.my | unitelmatch.top |
|---------|---------------------|--------------|-----------------|
| Registrar     | Amazon Registrar              | Gname.com  | GLOBAL ASSET DOMAINS INC. |
| WHOIS Privacy | Yes                           | Yes        | Yes                       |
| DNS Provider  | Amazon Route 53               | Cloudflare | Cloudflare                |
| CDN / Edge    | Amazon CloudFront             | Cloudflare | Cloudflare                |
| ASN           | AS16509                       | AS13335    | AS13335                   |
| IPv6          | No                            | Yes        | Yes                       |
| Reverse DNS   | CloudFront hostnames observed | Limited    | Limited                   |

---

# Infrastructure Observations

The following observations are supported by the collected evidence:

1. **Different Registration Providers**
   - `occupationoasis.com` was registered through Amazon Registrar.
   - `linkroles.my` and `unitelmatch.top` use different registrars.

2. **WHOIS Privacy**
   - All three domains had WHOIS privacy or redacted registration details enabled at the time of collection.

3. **Cloudflare Usage**
   - Both `linkroles.my` and `unitelmatch.top` use Cloudflare DNS and Cloudflare's network (AS13335).

4. **AWS Usage**
   - `occupationoasis.com` uses Amazon Route 53, Amazon CloudFront, and Amazon-owned IP address space.

5. **Reverse DNS**
   - Reverse DNS entries for `occupationoasis.com` clearly identify CloudFront infrastructure.
   - Reverse DNS lookups for the Cloudflare-protected domains returned limited information, consistent with Cloudflare's edge architecture.

These observations describe the infrastructure as observed during the investigation and do not independently establish ownership or operational relationships.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-022-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-01.png), [EV-022-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-02.png), [EV-022-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-03.png), [EV-022-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-022-04.png) | WHOIS records – occupationoasis.com  |
| [EV-023-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-023-01.png), [EV-023-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-023-02.png) | WHOIS records – linkroles.my         |
| [EV-024-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-024-01.png), [EV-024-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-024-02.png), [EV-024-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-024-03.png) | WHOIS records – unitelmatch.top      |
| [EV-026-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-01.png), [EV-026-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-02.png), [EV-026-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-03.png), [EV-026-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-04.png), [EV-026-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-05.png), [EV-026-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-06.png), [EV-026-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-07.png), [EV-026-08](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-08.png), [EV-026-09](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-09.png), [EV-026-10](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-10.png), [EV-026-11](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-11.png), [EV-026-12](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-12.png), [EV-026-13](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-13.png), [EV-026-14](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-14.png), [EV-026-15](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-15.png), [EV-026-16](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-026-16.png) | Reverse DNS results                  |
| [EV-027-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-01.png), [EV-027-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-02.png), [EV-027-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-03.png), [EV-027-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-04.png), [EV-027-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-05.png), [EV-027-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-06.png), [EV-027-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-027-07.png) | ASN and hosting provider information |

---

# Confidence Assessment

| Finding | Confidence |
|---------|------------|
| occupationoasis.com uses Amazon infrastructure | High |
| linkroles.my uses Cloudflare infrastructure    | High |
| unitelmatch.top uses Cloudflare infrastructure | High |
| WHOIS privacy enabled for all domains          | High |
| Cloudflare obscures origin infrastructure      | High |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/DNS_Analysis.md)
- [Passive_DNS.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Passive_DNS.md)
- [Certificate_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Certificate_Analysis.md)
- [Technology_Stack.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Technology_Stack.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Findings.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/docs/Findings.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     
