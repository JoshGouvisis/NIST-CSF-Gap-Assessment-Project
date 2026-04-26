# NIST CSF Gap Assessment — Study Guide for Josh Gouvisis

> This document is for your personal study only. It does NOT go on your GitHub.

---

## What This Project Is

I built you a complete NIST Cybersecurity Framework gap assessment for a fictional financial services company called Meridian Financial Group. This is the kind of document that Security Risk Analysts produce on the job. It evaluates a company's cybersecurity posture against a recognized framework, identifies gaps, and recommends improvements.

When you interview for Security Risk Analyst roles, you need to be able to explain what a gap assessment is, how the NIST CSF works, and walk someone through how you would conduct one. Studying this project teaches you all of that while also giving you a portfolio piece to show.

---

## How to Study This Project

1. Read the full gap assessment first, start to finish. Don't try to memorize anything yet, just understand the flow.
2. Come back and read this study guide section by section alongside the assessment.
3. Try the exercises at the bottom.
4. Practice explaining the project out loud as if you're in an interview.

---

## Understanding the NIST CSF

### What Is It

The NIST Cybersecurity Framework is a set of guidelines published by the National Institute of Standards and Technology. It gives organizations a common language and structured approach for managing cybersecurity risk. It is not a checklist of technical controls. It is a risk management framework that helps organizations understand where they are, decide where they need to be, and prioritize what to do next.

### Why It Matters

NIST CSF is the most widely referenced cybersecurity framework in the United States. It is voluntary (the government does not require private companies to follow it), but it has become the de facto standard that companies use to organize their security programs. If you work in GRC or security risk, you will use NIST CSF or something closely related to it in almost every role.

### The Six Functions

NIST CSF 2.0 has six core functions. Think of them as six questions every organization needs to answer.

**Govern (GV):** How do we manage cybersecurity risk as an organization? Who is responsible? What are our policies? How does the board stay informed? This function was added in CSF 2.0 and sits above the other five because governance drives everything else.

**Identify (ID):** What do we have, and what are the risks to it? This covers asset management (knowing what hardware, software, data, and people you have), risk assessment (understanding what threats and vulnerabilities exist), and business environment (understanding how cybersecurity risk affects your business objectives).

**Protect (PR):** What safeguards do we have in place? This covers access control, security awareness training, data security, platform security, and resilience. These are the preventive controls that limit or contain the impact of an incident.

**Detect (DE):** How do we know when something bad happens? This covers monitoring, logging, alerting, and analysis. Without detection, you are blind. The Q1 phishing incident in the assessment was caught because an employee noticed something odd, not because any system detected it. That is a major gap.

**Respond (RS):** What do we do when an incident occurs? This covers incident management, analysis, communication, and mitigation. A good response limits damage, preserves evidence, meets regulatory requirements, and leads to improvements.

**Recover (RC):** How do we get back to normal? This covers recovery planning, communication during recovery, and lessons learned. Recovery is about resilience, making sure the business can continue operating after a serious incident.

### How They Connect

The functions are not independent. They build on each other:

- You cannot **Protect** what you have not **Identified**
- You cannot **Respond** to what you have not **Detected**
- You cannot **Recover** effectively without a plan built during **Govern**
- **Govern** ties everything together and connects cybersecurity to business objectives

This is why the assessment found that Meridian's weakest area is Governance. Without governance, everything else is ad hoc.

---

## Understanding the Maturity Scoring

The maturity scale (1-5) is a common way to measure how mature an organization's practices are. It tells you not just whether something exists but how well it works.

A company at Level 1 (Initial) might have someone who kind of handles security when a problem comes up. A company at Level 5 (Optimized) has documented processes, metrics, regular reviews, and continuous improvement cycles.

Most small to mid-size companies land between 2 and 3. Getting to Level 3 (Defined) across all functions is a realistic and meaningful goal. Level 5 is where large enterprises and critical infrastructure organizations aim.

The reason this matters for your career: when you do a gap assessment for an employer, you are helping them understand where they are on this scale and what it takes to move up.

---

## Walkthrough: Key Findings

### Why Governance Scored Lowest (1.8)

Meridian has no cybersecurity risk register, no formal policies, no defined roles, and no board reporting. This means every security decision is made informally by the IT Director. There is no documented risk appetite (how much risk is the company willing to accept?), no way to track whether risks are being managed, and no visibility for leadership.

In your insurance background, think of it this way: imagine a brokerage that has no written underwriting guidelines, no compliance documentation, and no reporting to leadership on the state of the book. Everything depends on one person's judgment. That is what Meridian looks like for cybersecurity.

### Why Protect Scored Highest (3.0)

This is typical. Most companies invest in protective controls first because they are tangible and vendor-driven. You can buy a firewall, deploy antivirus, and enable MFA. These are real, visible things. What Meridian lacks is the processes and documentation around those controls: no access reviews, no training program, no patch management process, no DLP rules.

### The Q1 Phishing Incident

This incident runs through the entire assessment and illustrates why every function matters:

- **Govern:** No policy defined what should happen during an incident
- **Identify:** No risk assessment had identified phishing as a top risk (even though it is the number one attack vector)
- **Protect:** No security awareness training or phishing simulations that might have prevented the click
- **Detect:** No automated system detected the compromise. An employee noticed it.
- **Respond:** Response was informal. No evidence preservation, no regulatory notification, no communication to leadership.
- **Recover:** No after-action report. No lessons learned. No changes made.

In an interview, you can use this example to explain how the NIST CSF functions work together by showing what goes wrong when they don't.

---

## How This Connects to Your Insurance Experience

The gap assessment methodology maps directly to what you already know from risk management in insurance:

| Insurance Concept | Cybersecurity Equivalent |
|-------------------|-------------------------|
| Client risk assessment | Cybersecurity risk assessment |
| Identifying coverage gaps | Identifying security control gaps |
| Evaluating carrier compliance | Evaluating regulatory compliance (SEC, FINRA, SOX) |
| Risk mitigation recommendations | Security control recommendations |
| Documenting exposures for audit | Documenting findings for compliance and audit |
| Renewal review cycle | Annual risk reassessment |
| Carrier risk evaluation | Vendor/third-party risk assessment |
| Policy structure (coverage, limits, exclusions) | Security policy structure (scope, requirements, exceptions) |

When an interviewer asks "what makes you different from other entry-level candidates," this table is your answer. You have been doing risk assessment professionally for over a decade. The domain changed from insurance to cybersecurity. The discipline did not.

---

## Interview Q&A Prep

### "Tell me about a project you've worked on."

> "I conducted a NIST Cybersecurity Framework gap assessment for a mid-size financial services company. I evaluated their cybersecurity posture across all six CSF functions: Govern, Identify, Protect, Detect, Respond, and Recover. I scored each function on a maturity scale, identified critical gaps including the absence of a cybersecurity risk register and incident response plan, and developed a prioritized remediation roadmap with timelines and effort estimates. The assessment found an overall maturity of 2.4 out of 5, with governance and detection as the weakest areas."

### "What is the NIST Cybersecurity Framework?"

> "NIST CSF is a risk management framework published by the National Institute of Standards and Technology. It provides a common language for organizations to manage cybersecurity risk through six core functions: Govern, Identify, Protect, Detect, Respond, and Recover. It is not a checklist of specific controls, it is a framework for understanding your risk posture and prioritizing improvements. It is the most widely used cybersecurity framework in the US and is referenced across industries, especially in financial services and government."

### "How would you conduct a gap assessment?"

> "I would start by scoping the assessment, defining which systems, business units, and regulatory requirements are in scope. Then I would evaluate the organization's current practices against each NIST CSF function through documentation review, stakeholder interviews, and technical validation. I would score each function on a maturity scale, document specific gaps with their business impact, and produce a prioritized remediation roadmap. The output is a report that leadership can use to make informed risk decisions about where to invest in security improvements."

### "What is the difference between NIST CSF and ISO 27001?"

> "NIST CSF is a risk management framework. It helps organizations understand and manage cybersecurity risk but does not prescribe specific controls. ISO 27001 is a security management system standard that can be formally certified. ISO 27001 is more prescriptive and audit-focused. Many organizations use NIST CSF as their framework for understanding risk and then map specific ISO 27001 controls to address the gaps they identify. They are complementary, not competing."

### "What was the most critical finding in your assessment?"

> "The most critical finding was the complete absence of cybersecurity governance. The company had no risk register, no cybersecurity policies, no defined roles and responsibilities, and no board-level reporting. This meant that every security decision was informal and undocumented, which created both operational risk and regulatory risk given their SEC and FINRA obligations. Without governance, even the controls they did have in place, such as endpoint protection and MFA, lacked the policy foundation and oversight to be consistently effective."

---

## Exercises

1. **Pick one NIST CSF function and explain it in your own words.** Don't read the study guide. Just explain it as if you were telling a non-technical manager what it covers and why it matters.

2. **Read the Q1 phishing incident findings across all six functions.** Write 2-3 sentences explaining how proper governance could have prevented or reduced the impact of that incident.

3. **Look at the Prioritized Remediation Roadmap.** Why is "Establish cybersecurity risk register" listed as Priority 1 instead of "Deploy SIEM"? Explain why governance comes before detection.

4. **Compare the maturity scores across functions.** Why does Protect score highest while Govern scores lowest? Is this common? Why?

5. **Using the insurance-to-cybersecurity mapping table, write 3 sentences for a cover letter** explaining how your risk management experience translates to a Security Risk Analyst role.

6. **Open the README in your gap assessment repo and fill in the "What I Learned" section.** Write 3-5 sentences about what you learned from studying this assessment, what surprised you, and how you would explain it in an interview.
