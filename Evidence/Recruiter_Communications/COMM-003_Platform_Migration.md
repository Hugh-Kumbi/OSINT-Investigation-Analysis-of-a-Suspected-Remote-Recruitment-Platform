# COMM-003 — Platform Migration

## Evidence Metadata

| Field | Value |
|-------|-------|
| **Evidence ID**       | COMM-003                                                                                             |
| **Evidence Type**     | Recruiter Communication                                                                              |
| **Campaign Phase**    | Platform Migration                                                                                   |
| **Collection Method** | Direct Communication                                                                                 |
| **Source**            | [Recruiter Chat Transcript](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Recruiter_Communications/Recruiter_Chat_Transcript.md)                                                                            |
| **Integrity**         | Original conversation preserved. Formatting converted to Markdown only.                              |
| **Related Domains**   | linkroles.my, unitelmatch.top, unitelmatch.cc, unitelmatch.cyou                                      |
| **Related Analysis**  | [Infrastructure_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Infrastructure_Analysis.md), [Domain_Relationships.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Domain_Relationships.md), [Certificate_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Certificate_Analysis.md), [Reputation_Analysis.md](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Reputation_Analysis.md) |

---

# Executive Summary

This evidence documents one of the most significant developments observed during the investigation: the repeated migration between onboarding platforms following browser security warnings and accessibility issues.

Rather than discontinuing the onboarding process after security warnings were encountered, the recruiter consistently provided replacement domains and instructed the analyst to continue using the newly supplied infrastructure. This recurring behavior established a clear pattern of infrastructure replacement throughout the campaign.

The repeated introduction of newly observed domains represents a key behavioral and operational characteristic of the campaign.

---

# Investigation Relevance

This evidence supports the following investigation artifacts:

- Campaign Overview
- Investigation Timeline
- Infrastructure Analysis
- Domain Relationships
- Certificate Analysis
- Reputation Analysis
- Social Engineering Analysis
- Findings
- Indicators of Compromise

---

# Campaign Phase

**Phase:** Platform Migration

### Primary Objectives Observed

- Browser security warning encountered.
- Recruiter acknowledges platform issue.
- Alternative onboarding platform introduced.
- User instructed to continue using replacement infrastructure.
- Operational continuity maintained despite infrastructure changes.

---

# Key Observations

- Browser security warnings appeared during onboarding.
- Recruiter rapidly supplied replacement domains.
- Previously used infrastructure was abandoned.
- Multiple onboarding platforms served the same operational purpose.
- User was encouraged to continue without interruption.
- Platform replacement became an observable campaign behavior.

---

# Transcript

> **Note**
>
> The following transcript has been preserved in its original form. Only formatting has been modified to improve readability within this repository. No conversational content has been altered, omitted, or reordered.

---

# Phase: Platform Migration

**Date:** 2026.07.23 – 2026.08.04  
**Participants:** チェ・ジュン (Choi Jun) and Hugh K (Hugh Chanetsa)

---

## Conversation Log

### 2026.07.23 Thursday

**11:08** チェ・ジュン:  
おはよう！☀️🌸今日も心地よく、笑顔で過ごせますように😆

**12:21** チェ・ジュン:  
[https://www.unitelmatch.top](https://www.unitelmatch.top/) 今日、あなたは自分のネットショップにログインして確認しましたか？

**13:32** チェ・ジュン:  
今日はシステムがアップグレードされました。これを使って先にあなたのオンラインショップにログインして確認できます

---

### 2026.08.04 Tuesday

**12:06** チェ・ジュン:  
[https://www.unitelmatch.cc](https://www.unitelmatch.cc/)

**19:35** Hugh K:  
Yes, I am ready. I tried to login but google is saying that [https://www.unitelmatch.cc](https://www.unitelmatch.cc/) is a dangerous site

**19:35** Hugh K:  
What does that mean?

**19:36** チェ・ジュン:  
技術スタッフに質問する必要があるので、少々お待ちください。

**19:37** Hugh K:  
Okay cool

**19:38** チェ・ジュン:  
[https://www.unitelmatch.cyou](https://www.unitelmatch.cyou/)

**19:38** チェ・ジュン:  
まずはこちらのバックアップリンクを使ってストアにログインしてください。技術的な回答をお待ちしています。

**19:39** チェ・ジュン:  
Tell me when you log in

**19:54** チェ・ジュン:  
？？

**20:14** チェ・ジュン:  
That's just the platform upgrading, it's nothing to worry about. Are you checking your messages?

---

# Analyst Notes

## Behavioral Assessment

Rather than attempting to troubleshoot or resolve browser security warnings, the recruiter immediately redirected the analyst to replacement infrastructure.

This response indicates that operational continuity was prioritized over retaining a consistent platform. The repeated migration pattern suggests that the campaign was designed to tolerate infrastructure disruption by maintaining multiple operational domains capable of serving the same onboarding function.

---

## Infrastructure Evolution

The investigation identified the following progression:

| Order | Domain | Status |
|-------|--------|--------|
| 1 | occupationoasis.com | Initial recruitment platform  |
| 2 | linkroles.my        | Initial onboarding portal     |
| 3 | unitelmatch.top     | Replacement onboarding portal |
| 4 | unitelmatch.cc      | Subsequent replacement portal |
| 5 | unitelmatch.cyou    | Additional operational portal |

This sequence demonstrates a structured pattern of infrastructure replacement rather than isolated domain changes.

---

## Infrastructure Indicators

Observed characteristics include:

- Multiple onboarding domains serving identical functions.
- Rapid replacement following browser security warnings.
- Continued recruiter guidance throughout each migration.
- Consistent onboarding workflow despite infrastructure changes.
- Use of commercial cloud infrastructure supporting operational flexibility.

---

## Social Engineering Assessment

The recruiter employed reassurance throughout each migration event.

Observed techniques include:

- Minimizing user concerns.
- Presenting replacement domains as routine.
- Maintaining conversational continuity.
- Encouraging immediate continuation of onboarding.
- Avoiding discussion regarding browser security warnings.

These behaviors reduced the likelihood of campaign abandonment despite repeated security alerts.

---

## Related Evidence

| Evidence ID | Description |
|-------------|-------------|
| [COMM-001](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Recruiter_Communications/COMM-001_Initial_Contact.md) | Initial Contact      |
| [COMM-002](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Recruiter_Communications/COMM-002_Onboarding.md) | Onboarding           |
| [COMM-004](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Recruiter_Communications/COMM-004_Operational_Training.md) | Operational Training |
| [COMM-005](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Evidence/Recruiter_Communications/COMM-005_Financial_Escalation.md) | Financial Escalation |

---

## Related Analysis

- [`OSINT/Infrastructure_Analysis.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Infrastructure_Analysis.md)
- [`OSINT/Domain_Relationships.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Domain_Relationships.md)
- [`OSINT/Certificate_Analysis.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Certificate_Analysis.md)
- [`OSINT/Reputation_Analysis.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/OSINT/Reputation_Analysis.md)
- [`Analysis/Social_Engineering_Analysis.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Social_Engineering_Analysis.md)
- [`Analysis/Indicators_of_Compromise.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Indicators_of_Compromise.md)
- [`Analysis/Detection_Opportunities.md`](https://github.com/Hugh-Kumbi/Operation-Phantom-Store/blob/main/Analysis/Detection_Opportunities.md)

---

# Intelligence Assessment

## Campaign Evolution

This phase represents the first strong technical indicator that the campaign relied upon flexible infrastructure capable of being replaced without disrupting recruiter-led operations.

Repeated domain migration significantly increased analytical confidence that infrastructure management formed an intentional component of the campaign.

---

## Confidence Level

**High**

Multiple independent observations documented repeated domain migration directly from first-hand recruiter communications and browser interactions.

---

## Intelligence Value

**Very High**

This evidence establishes one of the investigation's most significant findings: repeated infrastructure replacement associated with recruiter-directed onboarding. The observed migration pattern became a defining behavioral characteristic of the campaign and directly informed the infrastructure analysis, IOC development, and detection opportunities documented elsewhere in the investigation.

---

# Supporting Technical Evidence

The infrastructure transitions documented within this communication are further supported by:

- Browser security warning screenshots.
- Passive DNS analysis.
- WHOIS records.
- Certificate Transparency logs.
- SSL certificate analysis.
- Technology fingerprinting.
- Domain relationship analysis.

These supporting artifacts provide independent technical validation of the behavioral observations documented within this evidence.

---

# Evidence Integrity Statement

This document is an evidence artifact produced during a structured Cyber Threat Intelligence (CTI) investigation.

The transcript has been converted into Markdown format solely to improve readability and repository organization.

No conversational content has been modified, removed, or reordered.

---

## Document Information

**Last Updated:**      August 2026  
**Analyst:**           Hugh Chanetsa  
**Assessment Type:**   OSINT Investigation       
**GitHub:**            https://github.com/Hugh-Kumbi/Operation-Phantom-Store