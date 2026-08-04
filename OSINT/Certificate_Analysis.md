# Certificate Analysis

**Case ID:** OSINT-2026-001

**Investigation Title:** Analysis of a Suspected Multi-Domain Remote Recruitment Platform

**Classification:** Open Source Intelligence (OSINT) / Cyber Threat Intelligence (CTI)

**Status:** Active Investigation

**Version:** 1.0

---

# Objective

This document analyzes the publicly observable SSL/TLS certificates associated with the domains identified during the investigation.

Certificate Transparency (CT) logs provide visibility into publicly trusted certificates that have been issued for a domain. They can assist in identifying:

- Certificate Authorities (CAs)
- Certificate issuance timelines
- Subject Alternative Names (SANs)
- Wildcard certificates
- Related hostnames
- Infrastructure changes over time

The observations in this document are based on Certificate Transparency records collected during the investigation.

---

# Scope

Domains analyzed:

- occupationoasis.com
- linkroles.my
- unitelmatch.top

---

# Collection Methodology

Certificate information was collected from publicly accessible Certificate Transparency logs.

Observed attributes include:

- Certificate Authority (CA)
- Validity period
- Certificate status
- Subject Alternative Names (SANs)
- Wildcard certificate usage
- Certificate issuance timeline

No certificate validation bypasses or active testing were performed.

---

# Domain: occupationoasis.com

## Certificate Summary

| Status | Valid From | Valid To | Issuer |
|--------|------------|----------|--------|
| Valid   | 29 Jun 2026 | 12 Jan 2027 | Amazon RSA 2048  |
| Expired | 21 Feb 2024 | 21 May 2024 | Let's Encrypt R3 |
| Expired | 23 Dec 2023 | 22 Mar 2024 | Let's Encrypt R3 |

---

## Subject Alternative Names (SANs)

Observed SANs:

- occupationoasis.com
- *.occupationoasis.com
- www.occupationoasis.com

---

## Certificate Authorities Observed

- Amazon RSA
- Let's Encrypt R3

---

## Certificate Transparency Observations

CT log entries were observed in:

- Tiger
- Nimbus
- Argon
- Xenon

These logs demonstrate that publicly trusted certificates have been issued for the domain over multiple years.

---

## Assessment

The certificate history indicates that the domain transitioned from Let's Encrypt certificates in 2023–2024 to an Amazon-issued certificate in 2026.

The presence of a wildcard certificate (`*.occupationoasis.com`) indicates support for securing multiple subdomains.

No additional subdomains were identified from the available CT data beyond those covered by the wildcard certificate.

---

# Domain: linkroles.my

## Certificate Summary

| Status | Valid From | Valid To | Issuer |
|--------|------------|----------|--------|
| Valid  | 19 Jul 2026 | 17 Oct 2026 | Google Trust Services WE1    |
| Valid  | 19 Jul 2026 | 17 Oct 2026 | SSL Corporation (Cloudflare) |
| Valid  | 19 Jul 2026 | 17 Oct 2026 | Google Trust Services WE1    |

---

## Subject Alternative Names (SANs)

Observed SANs:

- linkroles.my
- *.linkroles.my
- www.linkroles.my

---

## Certificate Authorities Observed

- Google Trust Services WE1
- Cloudflare (SSL Corporation)

---

## Certificate Transparency Observations

CT log entries were observed in:

- Tiger
- Wyvern
- TrustAsia

Multiple certificates were issued on the same day, consistent with certificate provisioning for Cloudflare-managed infrastructure.

---

## Assessment

The observed certificates indicate that the domain uses publicly trusted certificates issued through Google Trust Services and Cloudflare.

Wildcard certificates covering `*.linkroles.my` were observed, allowing TLS protection for multiple subdomains.

Based solely on the available CT records, no additional subdomains beyond those represented by the wildcard certificate were identified.

---

# Domain: unitelmatch.top

## Certificate Summary

| Status | Valid From | Valid To | Issuer |
|--------|------------|----------|--------|
| Valid  | 23 Jul 2026 | 21 Oct 2026 | Google Trust Services WE1 |
| Valid  | 23 Jul 2026 | 21 Oct 2026 | Google Trust Services WE1 |
| Valid  | 23 Jul 2026 | 21 Oct 2026 | Let's Encrypt YE2         |

---

## Subject Alternative Names (SANs)

Observed SANs:

- unitelmatch.top
- *.unitelmatch.top
- www.unitelmatch.top

---

## Certificate Authorities Observed

- Google Trust Services WE1
- Let's Encrypt YE2

---

## Certificate Transparency Observations

CT log entries were observed in:

- Tiger
- TrustAsia

The certificates were issued within a short time window, suggesting coordinated certificate deployment.

---

## Assessment

The observed certificates include both Google Trust Services and Let's Encrypt-issued certificates.

Wildcard coverage for `*.unitelmatch.top` indicates support for multiple secured subdomains.

No additional subdomains beyond those covered by the wildcard certificate were identified from the collected CT logs.

---

# Comparative Analysis

| Feature | occupationoasis.com | linkroles.my | unitelmatch.top |
|---------|---------------------|--------------|-----------------|
| Wildcard Certificate    | Yes        | Yes                             | Yes |
| WWW Certificate         | Yes        | Yes                             | Yes |
| Root Domain Certificate | Yes        | Yes                             | Yes |
| Google Trust Services   | No         | Yes                             | Yes |
| Amazon Certificate      | Yes        | No                              | No  |
| Let's Encrypt           | Historical | No (observed during collection) | Yes |
| Cloudflare Certificate  | No         | Yes                             | No  |

---

# Timeline Observations

| Domain | Earliest Observed Certificate | Latest Observed Certificate |
|--------|-------------------------------|-----------------------------|
| occupationoasis.com | Dec 2023 | Jan 2027 |
| linkroles.my        | Jul 2026 | Oct 2026 |
| unitelmatch.top     | Jul 2026 | Oct 2026 |

---

# Key Observations

The following observations are supported by the collected Certificate Transparency data:

1. **Wildcard Certificate Usage**
   - All three domains have wildcard certificates, enabling TLS coverage for subdomains.

2. **Shared Certificate Providers**
   - `linkroles.my` and `unitelmatch.top` both use Google Trust Services-issued certificates.
   - `occupationoasis.com` currently uses an Amazon-issued certificate.

3. **Certificate Issuance Timing**
   - Certificates for `linkroles.my` and `unitelmatch.top` were issued in July 2026 within days of one another.

4. **Historical Evolution**
   - `occupationoasis.com` shows a longer certificate history dating back to December 2023.
   - `linkroles.my` and `unitelmatch.top` have a more recent observable certificate history beginning in July 2026.

These observations describe the certificate ecosystem and do not, by themselves, establish operational relationships or intent.

---

# Evidence

| Evidence ID | Description |
|-------------|-------------|
| [EV-019-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-019-01.png) | Certificate Transparency results – occupationoasis.com |
| [EV-020-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-020-01.png) | Certificate Transparency results – linkroles.my        |
| [EV-021-01](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/Evidence/Screenshots/EV-021-01.png) | Certificate Transparency results – unitelmatch.top     |

---

# Confidence Assessment

| Finding | Confidence |
|---------|------------|
| Wildcard certificates observed for all three domains                      | High |
| occupationoasis.com currently uses an Amazon-issued certificate           | High |
| linkroles.my uses Google Trust Services and Cloudflare certificates       | High |
| unitelmatch.top uses Google Trust Services and Let's Encrypt certificates | High |
| Certificate issuance dates documented                                     | High |

---

# Related Documents

- [Domain_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Domain_Analysis.md)
- [DNS_Analysis.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/DNS_Analysis.md)
- [Passive_DNS.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Passive_DNS.md)
- [Infrastructure.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure.md)
- [Technology_Stack.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Technology_Stack.md)
- [Reputation.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Reputation.md)
- [Infrastructure_Evolution.md](https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform/blob/main/OSINT/Infrastructure_Evolution.md)

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Project Status:**    ✅ COMPLETE        
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/OSINT-Investigation-Analysis-of-a-Suspected-Remote-Recruitment-Platform     