---
title: "Responsible disclosure policy"
description: ""
summary: ""
date: 2025-04-02T17:19:07+02:00
lastmod: 2025-04-03T10:56:07+02:00
draft: false
type: "legal"
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

**To the ethical hackers and researchers who help uncover the unknown** — Your investigative work is greatly appreciated. [Responsible disclosure](https://en.wikipedia.org/wiki/Coordinated_vulnerability_disclosure "Wikipedia: Coordinated Vulnerability Disclosure") doesn’t just fix code; it protects people and their privacy. Your efforts make systems safer, faster, and more resilient. Together, we defend what matters.


{{< callout context="tip" title="Why private disclosure is preferred" icon="outline/rocket" >}}
Disclosing privately gives time to fix and retest any disclosures, protects people from active threats, and ensures you get accurate credit when the vulnerability is made public.
{{< /callout >}}


## Disclosure scope

- `*.securehive.co.uk`
- `*.docs.securehive.co.uk`

## How to report a vulnerability

All disclosure submissions **must go through** [openbugbounty.org](https://www.openbugbounty.org "Submit a vulnerability via OpenBugBounty"), unless the disclosure involves intrusive testing (which violates the [Open Bug Bounty project's terms of service](https://www.openbugbounty.org/terms-and-privacy/).

For secure, real-time communication, join our: [Secure Hive security disclosure Signal group]([https://signal.group/#C123FakeLinkReplaceMe](https://signal.group/#CjQKIKJmK8FOpqOa5IvHXvy33EMsDXfz9qZMW6y1DKLThiFdEhAzg6FvJqdnR_vI3J2UVgD8))

{{< callout context="note" title="Why use Signal to communicate?" icon="outline/info-circle" >}}
Using Signal means:

- No email/PII sharing  
- Real-time read receipts  
- Minimal metadata collection  
- Perfect forward secrecy  
- Verified, secure communication
{{< /callout >}}

## Reporting requirements

Clear, complete reports are essential to validation and resolution. Submissions must include:

- **Proof of Concept (PoC)**  
  - Step-by-step instructions  
  - Screenshots or videos (optional but helpful)  
  - Safe scripts or payloads with required parameters  


- **CVSS Score & Impact**  
  - Severity using a public [CVSS calculator](https://www.first.org/cvss/calculator/4-0")  
  - Description of the impact (e.g., privilege escalation, data exposure)  
  - Affected components and likelihood of exploitation


- **Remediation Guidance (Optional)**  
  - Suggested mitigations or code improvements  
  - References to best practices (e.g., [OWASP](https://owasp.org "OWASP Foundation"))  
  - Long-term security considerations


- **Third-Party Involvement**  
  - List of any impacted vendors, versions, and relevance

## Researcher responsibilities

- Only test systems listed in scope  
- Avoid disruption or harm to people, systems, data, or privacy  
- Immediately report any access to personally identifiable information (PII) or other sensitive data  
- Do not retain, reuse, or share data encountered during testing  
- Request clarification if scope or boundaries are unclear

## Prohibited testing

- Malware, spam, phishing, or social engineering  
- Denial-of-service (DoS) or resource exhaustion  
- Testing systems not owned by Secure Hive Ltd  
- Submissions involving:
  - Clickjacking on non-sensitive pages  
  - CSRF on non-sensitive forms  
  - MITM or physical access  
  - Known vulnerable libraries without a working PoC  
  - CSV injection without an exploit path  
  - Content spoofing with no meaningful impact  
  - Vulnerabilities that require unrealistic user interaction  
  - Automated scan outputs without manual validation  
  - Stack traces, version banners, or benign error messages  
  - Vulnerabilities affecting unsupported browser versions (2+ versions behind)

## Allowed testing

- Public-facing systems or subdomains under Secure Hive’s control  
- Rate limiting and brute-force testing (non-disruptive only)  
- Controlled use of tools with manual review  
- Testing that avoids user data access or service degradation

## Coordinated disclosure process

Upon receiving a report:

- Your submission will be reviewed and validated  
- A response will be sent within **5 business days** (confirmation or follow-up questions)  
- A disclosure timeline will be coordinated with the researcher  
- The vulnerability will either be resolved or the risk accepted within that timeframe  
- Once the vulnerability is resolved, public disclosure is welcome. Linking to an advisory is encouraged for recognition and community awareness. 
- Valid reports may be acknowledged publicly (if permission is granted)

Disclosures are prioritized, and any affected parties will be informed openly and without delay unless required by law.

## Recognition

Eligible researchers may receive:

- Credit on our [acknowledgments page](https://www.securehive.co.uk/acknowledgments "Secure Hive Acknowledgments Page") and official social media (social handles may be shared for attribution)
- Company branded merchandise (based on severity and at our discretion)  
- Charitable donations are available on request, with proof of donation (Selected from a list of charities)


## Terms

- Stop testing immediately if asked. Failure to comply may result in permanent removal from the program.
- Credit is given to the first reporter of a vulnerability (unless otherwise requested)
- Recognition and rewards must be claimed within **12 months**  
- You're responsible for applicable taxes on non-charitable rewards
- Rewards and acknowledgments are not available to individuals in countries under international sanctions

## Safe Harbour and legal protections

- No legal action will be pursued against you when acting in good faith under this policy
- In the event of third-party legal claims, written assurance will be issued affirming that the research was permitted under this policy and carried out responsibly.
- You are required to comply with all local laws in your country of residence and the laws of the United Kingdom, where Secure Hive operates.
