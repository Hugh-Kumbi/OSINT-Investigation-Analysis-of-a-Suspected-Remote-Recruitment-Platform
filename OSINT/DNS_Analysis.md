# DNS Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document analyzes the Domain Name System (DNS) configuration observed for the domains identified during the investigation.

The objective is to document the current DNS infrastructure supporting each domain and identify technical characteristics that may assist further analysis.

DNS observations are point-in-time findings and may change after collection.

---

# Scope

Domains analyzed:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

---

# Collection Methodology

DNS information was collected using passive and publicly accessible DNS lookup services.

The following record types were reviewed where available:

- A
- AAAA
- MX
- NS
- SOA
- TXT
- CNAME

Supporting infrastructure observations included:

- Autonomous System (ASN)
- Hosting provider
- Geographic location
- Name server provider

No active exploitation or unauthorized interaction with the infrastructure was performed.

---

# Domain Analysis

---

# Domain: occupationoasis.com

## Name Servers

| Server |
|--------|
| ns-149.awsdns-18.com    |
| ns-865.awsdns-44.net    |
| ns-1883.awsdns-43.co.uk |
| ns-1422.awsdns-49.org   |

### Observation

The domain uses Amazon Route 53 authoritative name servers.

---

## SOA Record

| Property | Value |
|----------|-------|
| Primary Name Server | ns-865.awsdns-44.net         |
| Responsible Contact | awsdns-hostmaster.amazon.com |
| Serial              | 1                            |
| Refresh             | 7200                         |
| Retry               | 900                          |
| Expire              | 1209600                      |
| Minimum TTL         | 86400                        |

---

## A Records

Observed root A record:

- 18.239.36.77

Observed WWW A records:

- 65.8.180.42
- 65.8.180.52
- 65.8.180.92
- 65.8.180.104

---

## AAAA Records

No AAAA records were observed during collection.

---

## MX Records

No MX records were observed during collection.

---

## TXT Records

No TXT records were observed during collection.

---

## CNAME Records

No CNAME records were observed during collection.

---

## Infrastructure

| Property | Value |
|----------|-------|
| ASN               | AS16509                |
| Provider          | Amazon.com, Inc.       |
| Observed Location | Amsterdam, Netherlands |

---

## Assessment

The observed DNS configuration indicates the use of Amazon Web Services (AWS), including Route 53 name servers and Amazon-owned IP address space.

The absence of observed MX and TXT records suggests that the domain was not advertising email infrastructure or DNS-based verification records at the time of collection.

No conclusions regarding operational intent are drawn from these observations alone.

---

# Domain: linkroles.my

## Name Servers

| Server |
|--------|
| alina.ns.cloudflare.com |
| bob.ns.cloudflare.com   |

### Observation

The domain uses Cloudflare authoritative name servers.

---

## SOA Record

| Property | Value |
|----------|-------|
| Primary Name Server | alina.ns.cloudflare.com |
| Responsible Contact | dns.cloudflare.com      |
| Serial              | 2409939902              |
| Refresh             | 10000                   |
| Retry               | 2400                    |
| Expire              | 604800                  |
| Minimum TTL         | 1800                    |

---

## A Records

Observed root A records:

- 188.114.97.0

Observed WWW A records:

- 104.21.30.243
- 172.67.174.52

---

## AAAA Records

Observed:

- 2a06:98c1:3120::0
- 2a06:98c1:3121::0

---

## MX Records

No MX records were observed during collection.

---

## TXT Records

No TXT records were observed during collection.

---

## CNAME Records

No CNAME records were observed during collection.

---

## Infrastructure

| Property | Value |
|----------|-------|
| ASN                | AS13335                                      |
| Provider           | Cloudflare                                   |
| Observed Locations | Medellín (Colombia), Embsay (United Kingdom) |

---

## Assessment

The observed DNS configuration indicates that the domain is fronted by Cloudflare infrastructure.

Cloudflare can provide services such as reverse proxying, caching, DDoS mitigation, and TLS termination. Based on the available DNS records alone, it is not possible to determine which specific Cloudflare services are being used.

---

# Domain: unitelmatch.top

## Name Servers

| Server |
|--------|
| alina.ns.cloudflare.com |
| bob.ns.cloudflare.com   |

### Observation

The domain uses the same authoritative Cloudflare name servers observed for linkroles.my.

---

## SOA Record

| Property | Value |
|----------|-------|
| Primary Name Server | alina.ns.cloudflare.com |
| Responsible Contact | dns.cloudflare.com      |
| Serial              | 2410260643              |
| Refresh             | 10000                   |
| Retry               | 2400                    |
| Expire              | 604800                  |
| Minimum TTL         | 1800                    |

---

## A Records

Observed root A record:

- 188.114.96.0

Observed WWW A records:

- 104.21.22.200
- 172.67.206.231

---

## AAAA Records

Observed:

- 2a06:98c1:3120::0
- 2a06:98c1:3121::0

---

## MX Records

No MX records were observed during collection.

---

## TXT Records

No TXT records were observed during collection.

---

## CNAME Records

No CNAME records were observed during collection.

---

## Infrastructure

| Property | Value |
|----------|-------|
| ASN                | AS13335                                      |
| Provider           | Cloudflare                                   |
| Observed Locations | Medellín (Colombia), Embsay (United Kingdom) |

---

## Assessment

The DNS configuration closely resembles that of linkroles.my, including the use of identical authoritative name servers, the same autonomous system (AS13335), and Cloudflare infrastructure.

These similarities are documented as technical observations only. Additional evidence would be required to determine whether the domains are operationally related.

---

# Comparative Analysis

| Feature | occupationoasis.com | linkroles.my | unitelmatch.top |
|---------|---------------------|--------------|-----------------|
| DNS Provider  | Amazon Route 53 | Cloudflare | Cloudflare      |
| ASN           | AS16509         | AS13335    | AS13335         |
| MX Observed   | No              | No         | No              | 
| TXT Observed  | No              | No         | No              |
| IPv6 Observed | No              | Yes        | Yes             |
| WWW A Records | Yes             | Yes        | Yes             |

---

# Key Observations

The following observations are supported by the DNS data collected during the investigation:

1. **Different DNS Providers**
   - `occupationoasis.com` uses Amazon Route 53.
   - `linkroles.my` and `unitelmatch.top` use Cloudflare.

2. **Shared Cloudflare Infrastructure**
   - `linkroles.my` and `unitelmatch.top` share the same authoritative name servers (`alina.ns.cloudflare.com` and `bob.ns.cloudflare.com`) and are associated with the same ASN (AS13335).

3. **Email Infrastructure**
   - No MX records were observed for any of the three domains at the time of collection.

4. **TXT Records**
   - No TXT records were observed, meaning no SPF, DKIM, DMARC, or other TXT-based verification records were visible during the collection period.

These are point-in-time observations and should not be interpreted as definitive indicators of legitimacy or maliciousness.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-016-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-01.png), [EV-016-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-02.png), [EV-016-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-03.png), [EV-016-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-04.png), [EV-016-05](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-05.png), [EV-016-06](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-06.png), [EV-016-07](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-016-07.png) | DNS lookup – occupationoasis.com |
| [EV-017-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-01.png), [EV-017-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-02.png), [EV-017-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-03.png), [EV-017-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-017-04.png) | DNS lookup – linkroles.my        |
| [EV-018-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-01.png), [EV-018-02](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-02.png), [EV-018-03](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-03.png), [EV-018-04](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-018-04.png) | DNS lookup – unitelmatch.top     |

---

# Confidence Assessment

| Finding | Confidence |
|---------|------------|
| Amazon Route 53 used by occupationoasis.com                             | High |
| Cloudflare used by linkroles.my                                         | High |
| Cloudflare used by unitelmatch.top                                      | High |
| Shared Cloudflare name servers between linkroles.my and unitelmatch.top | High |
| No MX records observed during collection                                | High |
| No TXT records observed during collection                               | High |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [Passive_dns.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Passive_DNS.md)
- [Certificate_analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Certificate_Analysis.md)
- [Infrastructure.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Infrastructure_Evolution.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure_Evolution.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     
