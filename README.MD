# NIST Cybersecurity Framework Gap Assessment

## Meridian Financial Group

**Assessment Date:** April 2026
**Assessor:** Josh Gouvisis
**Framework Version:** NIST CSF 2.0
**Classification:** Internal Use Only

---

## Executive Summary

Meridian Financial Group engaged this assessment to evaluate its current cybersecurity posture against the NIST Cybersecurity Framework (CSF) 2.0. Meridian is a mid-size financial services firm with approximately 300 employees, operating across three office locations and serving retail and institutional clients through a mix of proprietary and third-party platforms.

This assessment evaluated Meridian's capabilities across all six NIST CSF functions: Govern, Identify, Protect, Detect, Respond, and Recover. Each function was scored on a maturity scale of 1 to 5, with 1 representing ad hoc or nonexistent practices and 5 representing optimized and continuously improving practices.

**Overall Maturity Score: 2.4 out of 5 (Developing)**

Meridian has foundational security controls in place but lacks the formalization, documentation, and consistency required for a mature cybersecurity program. The most critical gaps are in governance and risk management (no formal cybersecurity risk register), detection capabilities (limited SIEM coverage and no defined alert triage process), and incident response (no documented IR plan or tested playbooks). The strongest area is basic access control and endpoint protection, though even these lack centralized policy enforcement.

**Top 5 Priority Recommendations:**

1. Establish a formal cybersecurity risk register and risk assessment process
2. Deploy and configure a SIEM solution with 24/7 log ingestion from critical systems
3. Develop, document, and test an incident response plan with defined roles and escalation procedures
4. Implement a vendor risk management program for all third-party service providers
5. Launch a security awareness training program with phishing simulation exercises

---

## Company Profile

| Attribute | Detail |
|-----------|--------|
| Company Name | Meridian Financial Group |
| Industry | Financial Services (wealth management, retail brokerage, institutional advisory) |
| Employees | ~300 |
| Locations | 3 offices (Phoenix AZ headquarters, Denver CO, Austin TX) |
| IT Environment | Hybrid (on-premises Active Directory, Microsoft 365, Azure cloud workloads, third-party trading platforms) |
| Regulatory Obligations | SEC, FINRA, SOX, state financial regulations, client data privacy requirements |
| IT Staff | 8 person IT team, no dedicated cybersecurity staff |
| Current Security Tools | Microsoft Defender for Endpoint, Cisco Meraki firewalls, Duo MFA (partial deployment), Veeam backup |
| Recent Incidents | Phishing email compromised one employee account in Q1 2026. Contained within 48 hours but no formal post-incident review was conducted. |

---

## Assessment Methodology

This assessment was conducted using the NIST Cybersecurity Framework 2.0 as the primary reference. Each of the six core functions was evaluated through a combination of documentation review, stakeholder interviews, and technical control validation.

**Maturity Scoring Scale:**

| Score | Level | Description |
|-------|-------|-------------|
| 1 | Initial | Practices are ad hoc, undocumented, or nonexistent. Security depends on individual effort. |
| 2 | Developing | Some practices exist but are inconsistent, partially documented, or not enforced across the organization. |
| 3 | Defined | Practices are documented, standardized, and communicated. Policies exist and are generally followed. |
| 4 | Managed | Practices are measured, monitored, and reviewed regularly. Metrics are used to drive improvement. |
| 5 | Optimized | Practices are continuously improved based on lessons learned, threat intelligence, and business changes. |

---

## Function 1: Govern (GV)

**Maturity Score: 1.8 / 5 (Initial to Developing)**

The Govern function establishes the organization's cybersecurity risk management strategy, expectations, and policy. It is the foundation that everything else is built on. Without governance, security efforts are reactive and disconnected from business objectives.

### Current State

Meridian does not have a formal cybersecurity governance structure. The IT Director reports to the CFO and handles security decisions informally. There is no cybersecurity policy document, no risk management strategy, and no defined roles and responsibilities for security. The board receives no regular cybersecurity briefings.

A general acceptable use policy exists but has not been updated since 2021. There is no formal risk appetite statement and no process for evaluating cybersecurity risk as part of business decisions.

### Findings

| Category | Finding | Gap |
|----------|---------|-----|
| GV.OC (Organizational Context) | No documented understanding of how cybersecurity risk affects business objectives | No cybersecurity risk appetite statement exists |
| GV.RM (Risk Management Strategy) | No formal cybersecurity risk management strategy or risk register | Risk decisions are made ad hoc by the IT Director |
| GV.RR (Roles, Responsibilities, Authorities) | No defined cybersecurity roles or RACI matrix | Security responsibilities are assumed, not assigned |
| GV.PO (Policy) | Acceptable use policy exists but is outdated (2021). No cybersecurity-specific policies | No incident response policy, no data classification policy, no access control policy |
| GV.OV (Oversight) | Board receives no cybersecurity reporting | No metrics, no risk dashboards, no regular briefings |
| GV.SC (Supply Chain Risk Management) | No vendor risk management program | Third-party providers are not evaluated for security posture |

### Recommendations

- Develop a cybersecurity risk management strategy aligned with business objectives and regulatory requirements (SEC, FINRA, SOX)
- Create and maintain a cybersecurity risk register with risk owners, likelihood, impact, and mitigation status
- Define cybersecurity roles and responsibilities using a RACI matrix (Responsible, Accountable, Consulted, Informed)
- Draft and approve a cybersecurity policy suite: acceptable use, access control, incident response, data classification, vendor risk management
- Establish quarterly cybersecurity briefings for the board with defined metrics and risk reporting
- Implement a vendor risk management program that evaluates third-party security posture before onboarding and at regular intervals

---

## Function 2: Identify (ID)

**Maturity Score: 2.2 / 5 (Developing)**

The Identify function focuses on understanding the organization's assets, business environment, and risk. You cannot protect what you do not know you have. This function answers: what do we have, what is it worth, and what are the threats to it.

### Current State

Meridian maintains a partial asset inventory through its IT ticketing system but it is not comprehensive and does not include all cloud resources, SaaS subscriptions, or data repositories. There is no formal data classification scheme. The IT team has a general understanding of the network topology but no documented architecture diagram that includes cloud workloads.

A basic vulnerability scan runs monthly through Microsoft Defender but findings are reviewed inconsistently and there is no formal vulnerability management process with SLAs for remediation.

### Findings

| Category | Finding | Gap |
|----------|---------|-----|
| ID.AM (Asset Management) | Partial hardware/software inventory exists via ticketing system | No comprehensive asset inventory including cloud, SaaS, data repositories. No asset owners assigned. |
| ID.RA (Risk Assessment) | No formal risk assessment process | Vulnerability scans run but findings are not prioritized or tracked to remediation |
| ID.IM (Improvement) | No process for incorporating lessons learned | The Q1 2026 phishing incident had no formal post-incident review |

### Recommendations

- Build and maintain a comprehensive asset inventory covering hardware, software, cloud resources, SaaS applications, and data repositories. Assign an owner to each asset.
- Implement a formal data classification scheme (Public, Internal, Confidential, Restricted) and apply it to all data repositories
- Establish a formal vulnerability management process: scan, prioritize by CVSS score and asset criticality, assign remediation owners, track to closure with SLAs
- Conduct an annual formal risk assessment that identifies threats, vulnerabilities, likelihood, and business impact for critical assets
- Institute a formal lessons learned process triggered by every significant incident or near-miss

---

## Function 3: Protect (PR)

**Maturity Score: 3.0 / 5 (Defined)**

The Protect function covers the safeguards used to limit the impact of cybersecurity events. This is often where organizations invest most heavily, and Meridian is relatively stronger here compared to the other functions.

### Current State

Meridian has Microsoft Defender for Endpoint deployed across all managed devices. Duo MFA is enabled for Microsoft 365 and VPN but is not enforced on all third-party platforms used by advisors. The Cisco Meraki firewall provides perimeter protection and basic network segmentation at each office.

No formal security awareness training program exists. The IT team manages access provisioning manually with no formal access review process. There is no privileged access management (PAM) solution, and several service accounts have excessive permissions that have accumulated over time.

### Findings

| Category | Finding | Gap |
|----------|---------|-----|
| PR.AA (Identity Management and Access Control) | MFA deployed for M365 and VPN, not for all third-party platforms | Incomplete MFA coverage. No PAM solution. No formal access review process. |
| PR.AT (Awareness and Training) | No formal security awareness training program | Employees have not received structured security training. No phishing simulation program. |
| PR.DS (Data Security) | No data classification or data handling standards | No DLP controls. No encryption policy for data at rest or in transit beyond platform defaults. |
| PR.PS (Platform Security) | Defender deployed. Patch management handled by IT but not formalized. | No documented patch SLAs. No configuration baseline or hardening standards. |
| PR.IR (Technology Infrastructure Resilience) | Meraki provides basic segmentation | No micro-segmentation. No formal network architecture review. |

### Recommendations

- Enforce MFA on all applications accessed by employees, including third-party trading and advisory platforms
- Implement a privileged access management solution to control, monitor, and audit all privileged account activity
- Conduct quarterly access reviews to verify that user permissions are appropriate and revoke access for departed employees or role changes
- Launch a security awareness training program with at minimum annual training and monthly phishing simulation exercises
- Implement a data loss prevention solution and define encryption requirements for data at rest and in transit
- Establish patch management SLAs: critical patches within 48 hours, high within 7 days, medium within 30 days
- Define and implement configuration baselines and hardening standards for all endpoints, servers, and network devices

---

## Function 4: Detect (DE)

**Maturity Score: 2.0 / 5 (Developing)**

The Detect function covers capabilities for identifying cybersecurity events in a timely manner. Detection is the difference between catching an incident early and discovering a breach months after the fact.

### Current State

Meridian has no SIEM solution. Microsoft Defender generates endpoint alerts and Microsoft 365 produces audit logs, but these are not centrally aggregated or reviewed on any consistent schedule. The IT team reviews Defender alerts reactively when something is flagged as urgent.

Network monitoring is limited to Meraki dashboard alerts for connectivity issues. There is no network-level threat detection (IDS/IPS) beyond what Meraki provides by default.

### Findings

| Category | Finding | Gap |
|----------|---------|-----|
| DE.CM (Continuous Monitoring) | No SIEM. Defender alerts and M365 logs exist but are not centrally collected or reviewed. | No centralized logging, no correlation, no 24/7 monitoring capability |
| DE.AE (Adverse Event Analysis) | No alert triage process. Alerts are reviewed reactively. | No severity classification, no escalation criteria, no analyst workflow |

### Recommendations

- Deploy a SIEM solution (Microsoft Sentinel, Splunk, or equivalent) with log ingestion from endpoints, firewalls, Active Directory, Microsoft 365, VPN, and third-party platforms
- Define an alert triage process with severity levels, escalation criteria, and analyst response workflows
- Implement network-level threat detection (IDS/IPS) at all three office locations
- Establish baseline monitoring for user behavior to detect anomalous activity (unusual login times, geographic anomalies, impossible travel)
- Consider a managed detection and response (MDR) service if 24/7 internal monitoring is not feasible with current staffing

---

## Function 5: Respond (RS)

**Maturity Score: 2.0 / 5 (Developing)**

The Respond function covers the actions taken once a cybersecurity incident is detected. A strong response capability limits damage, preserves evidence, and ensures regulatory obligations are met. Without a documented plan, incident response is chaotic and inconsistent.

### Current State

Meridian has no documented incident response plan. When the Q1 2026 phishing incident occurred, the IT Director coordinated the response informally. The compromised account was disabled, the password was reset, and affected systems were reviewed. However, there was no formal communication to leadership, no evidence preservation, no notification to regulatory bodies (despite SEC and FINRA notification requirements for certain incidents), and no post-incident review.

There are no defined incident response roles, no escalation procedures, no communication templates, and no tested playbooks for common incident types (phishing, ransomware, insider threat, data breach).

### Findings

| Category | Finding | Gap |
|----------|---------|-----|
| RS.MA (Incident Management) | No documented IR plan. Q1 incident handled informally. | No defined roles, escalation procedures, or communication templates |
| RS.AN (Incident Analysis) | No evidence preservation or forensic capability | Compromised account was reset before evidence could be fully collected |
| RS.CO (Incident Reporting and Communication) | No stakeholder communication during Q1 incident | No templates, no regulatory notification process, no leadership briefing protocol |
| RS.MI (Incident Mitigation) | Basic containment was performed (account disabled) | No playbooks for common incident types. Mitigation was ad hoc. |

### Recommendations

- Develop a documented incident response plan that defines roles (IR lead, communications, legal, technical), escalation thresholds, and communication chains
- Create playbooks for the top 5 incident types: phishing/credential compromise, ransomware, data breach, insider threat, third-party compromise
- Establish evidence preservation procedures that ensure forensic integrity before containment actions (e.g., capture logs and mailbox state before resetting passwords)
- Define regulatory notification procedures for SEC, FINRA, and state regulators with timelines and templates
- Conduct tabletop exercises at minimum twice per year to test the IR plan with realistic scenarios
- Designate an incident response team with members from IT, legal, compliance, communications, and executive leadership

---

## Function 6: Recover (RC)

**Maturity Score: 2.5 / 5 (Developing)**

The Recover function supports timely restoration of capabilities after a cybersecurity incident. Recovery planning ensures business continuity and captures lessons learned to improve future resilience.

### Current State

Meridian has nightly Veeam backups of file servers and critical databases. Microsoft 365 data is backed up through a third-party SaaS backup solution. However, backup restoration has never been formally tested. The IT Director is confident the backups work but there is no documented evidence of a successful restoration test.

There is no documented business continuity plan (BCP) or disaster recovery plan (DRP). If the Phoenix headquarters experienced a major incident (ransomware, facility loss, extended outage), there is no documented plan for how the business would continue operating.

No lessons learned process exists. The Q1 2026 phishing incident produced no formal after-action report, and no changes were made to controls or processes as a result.

### Findings

| Category | Finding | Gap |
|----------|---------|-----|
| RC.RP (Recovery Planning) | No documented BCP or DRP | Business continuity depends on informal knowledge held by the IT Director |
| RC.CO (Recovery Communication) | No recovery communication plan | No templates for client, employee, or regulatory communication during a recovery scenario |

### Recommendations

- Develop and document a business continuity plan that identifies critical business functions, recovery time objectives (RTOs), and recovery point objectives (RPOs)
- Develop a disaster recovery plan with specific technical recovery procedures for each critical system
- Test backup restoration quarterly and document results. Verify that RTO and RPO targets can be met.
- Establish a formal lessons learned process: every significant incident produces a written after-action report with findings and corrective actions
- Conduct an annual BCP/DRP tabletop exercise with participation from business leadership, not just IT

---

## Maturity Summary

| Function | Score | Level |
|----------|-------|-------|
| Govern | 1.8 | Initial to Developing |
| Identify | 2.2 | Developing |
| Protect | 3.0 | Defined |
| Detect | 2.0 | Developing |
| Respond | 2.0 | Developing |
| Recover | 2.5 | Developing |
| **Overall** | **2.4** | **Developing** |

---

## Prioritized Remediation Roadmap

| Priority | Action | Function | Effort | Timeline |
|----------|--------|----------|--------|----------|
| 1 | Establish cybersecurity risk register and risk assessment process | Govern | Medium | 30 days |
| 2 | Develop and document incident response plan with playbooks | Respond | Medium | 30 days |
| 3 | Deploy SIEM with centralized log ingestion from critical systems | Detect | High | 60 days |
| 4 | Implement vendor risk management program | Govern | Medium | 45 days |
| 5 | Launch security awareness training with phishing simulations | Protect | Low | 30 days |
| 6 | Enforce MFA on all applications including third-party platforms | Protect | Low | 14 days |
| 7 | Implement quarterly access reviews and PAM solution | Protect | Medium | 45 days |
| 8 | Build comprehensive asset inventory with data classification | Identify | Medium | 45 days |
| 9 | Develop business continuity and disaster recovery plans | Recover | Medium | 60 days |
| 10 | Test backup restoration and document results quarterly | Recover | Low | 7 days |

---

## What I Learned

I went into this project thinking the biggest problems at Meridian would be on the technical side, missing tools, unpatched systems, that kind of thing. What actually surprised me was how much damage the absence of governance caused across everything else. Meridian had real security tools deployed, but without documented policies, defined ownership, or any formal risk process, those tools weren't connected to anything. That's why Govern scored the lowest at 1.8, and it changed how I think about where security programs actually break down.

The Q1 2026 phishing incident was the most eye-opening part of the assessment for me. On the surface it looked like one compromised account that got contained. But when I mapped it against the framework, that single incident exposed gaps in Detect, Respond, and Identify all at once. No centralized logging to catch it faster, no IR plan to follow when it happened, and no post-incident review to learn from it afterward. I hadn't thought about incidents that way before. Now I do.

I also learned that gap analysis is only useful if you're honest. It would have been easy to rate something as "partially implemented" just because a tool exists. But the framework pushes you to ask what evidence you actually have that a control is working, and for a lot of Meridian's controls, that evidence wasn't there. That discipline is something I'll bring into any GRC or risk analyst role I step into.
