# Oscorp Cybersecurity Program Review
### NIST CSF Assessment & 3-Year Risk Reduction Roadmap

> **Disclaimer:** This is a fictional cybersecurity consulting case study developed as a capstone project for the GRC Mastery course. Oscorp and all associated details are fictional.

---

## What This Project Is

This project simulates a full cybersecurity consulting engagement. I was placed in the role of an incoming Cybersecurity Consultant at Oscorp — a fictional research-driven pharmaceutical company with high-value intellectual property (a proprietary drug formula) and a largely reactive, IT-managed security posture.

The engagement covered everything a real GRC consulting project would require:

- Conducting a structured current-state assessment mapped to the NIST Cybersecurity Framework (CSF)
- Identifying and scoring control gaps across all five CSF functions
- Translating control gaps into quantified financial risk using the ALE model
- Designing a sequenced, prioritized 3-year cybersecurity roadmap
- Presenting findings in an executive-ready format with ROI justification

---

## The Problem

Oscorp had no formal cybersecurity strategy. Cyber responsibility was informally assigned to the IT team with no defined ownership, governance structure, or executive visibility. Key control failures included:

- No multi-factor authentication across any systems
- Shared administrative credentials among senior IT staff
- No data classification, labeling, or DLP controls
- No centralized logging or SIEM capability
- Vulnerability scanning (Qualys) used on an ad-hoc basis only — high and critical findings left unresolved
- No third-party risk management despite a critical SaaS dependency (Horizon Labs)
- No formal incident response plan

Oscorp's only meaningful strengths were in physical security and business continuity/disaster recovery.

---

## My Approach

### 1. NIST CSF Assessment
I conducted a control-by-control assessment across all five CSF functions (Identify, Protect, Detect, Respond, Recover) using structured interview questions per sub-category. Each control was scored Pass/Fail with written commentary explaining the gap and its business implication.

**Summary findings:**

| Function | Maturity | Key Gap |
|----------|----------|---------|
| Govern | Low | No strategy, no executive ownership |
| Identify | Low | No risk process, weak asset management |
| Protect | Low–Medium | No MFA, no DLP, shared admin credentials |
| Detect | Low | No SIEM, no log review, reactive only |
| Respond | Low | No incident response plan or process |
| Recover | Medium | Strong BCP/DR — the one clear strength |

### 2. Risk Quantification
I used the **Annualized Loss Expectancy (ALE)** model as the primary risk quantification method, with FAIR (Factor Analysis of Information Risk) used to structure and pressure-test the likelihood and impact assumptions.

**Methodology:**
- Baseline breach likelihood sourced from the Verizon DBIR and IBM Cost of a Data Breach Report (industry average: 15–20% annually for similar organizations)
- Oscorp's likelihood adjusted upward to **25–30%** based on three specific control failures: absence of MFA, shared admin credentials, and no centralized monitoring — each with documented impact on breach probability per DBIR data
- Impact modeled in two scenarios:

| Scenario | Rationale | Impact Estimate |
|----------|-----------|----------------|
| Conservative | Standard breach: credential compromise, data exposure, incident response costs, regulatory notification | $8M–$15M |
| High-Impact | IP exfiltration: loss of drug formula competitive advantage, legal exposure, lost market exclusivity | $50M–$100M |

**Note on uncertainty:** These are estimates with meaningful uncertainty bands, not predictions. The conservative scenario is grounded in IBM average breach cost data ($4.88M industry average, adjusted upward for Oscorp's IP sensitivity). The high-impact scenario is directional — it reflects a plausible but not certain worst-case outcome. Real FAIR analysis would require threat frequency data and asset valuation inputs that are beyond the scope of this exercise.

**Current risk exposure (ALE):**
- Conservative: 0.28 × $12M = **~$3.4M/year**
- High-impact: 0.28 × $75M = **~$21M/year**

**Post-implementation (Year 1 controls reduce breach likelihood ~60–65%):**
- Conservative: 0.10 × $12M = **~$1.2M/year**
- High-impact: 0.10 × $75M = **~$7.5M/year**

**Annual risk reduction:** ~$2.2M–$13.5M
**3-year program investment:** $0.75M–$1.5M
**ROI:** ~4x–9x (conservative to high-impact), with payback under 12 months in both scenarios

### 3. 3-Year Roadmap
The roadmap is sequenced by risk priority, not by cost or ease. Year 1 addresses the controls most directly tied to breach likelihood. Years 2 and 3 build operational maturity and long-term resilience.

**Year 1 — Risk Containment**
Enforce MFA across all users. Eliminate shared admin credentials. Implement DLP controls and baseline data classification. Deploy SIEM with initial log sources onboarded. Formalize vulnerability management with defined SLAs and remediation tracking.

**Year 2 — Operational Maturity**
Implement full Privileged Access Management (PAM). Automate identity lifecycle (joiner–mover–leaver). Deploy CMDB with automated asset discovery. Establish Third-Party Risk Management (TPRM) program targeting critical SaaS dependencies. Formalize and test incident response with executive tabletop exercises.

**Year 3 — Optimization**
Deploy behavioral analytics for insider threat detection. Implement continuous control monitoring. Adopt advanced risk quantification methods. Begin Zero Trust architecture alignment (Conditional Access, Entra ID, Defender for Cloud Apps in Oscorp's Microsoft-centric environment).

---

## Deliverables

| Deliverable | Description |
|-------------|-------------|
| 📄 [Executive Report](3-Year%20Cybersecurity%20Program.pdf) | Full consulting deliverable: current state, roadmap, financial model, NIST summary |
| 📊 [NIST CSF Assessment (Excel)](supporting-deliverables/GRC_Mastery_NIST_Cyber_Security_Assessment.xlsx) | Control-by-control scoring with interview questions and gap commentary |
| 📋 [Current State Brief (PDF)](supporting-deliverables/Capstone_Oscorp_CurrentState.pdf) | Source scenario document describing Oscorp's environment |

---

## Skills Demonstrated

- **GRC program design** — end-to-end consulting engagement structure
- **NIST CSF alignment** — structured control assessment across all five functions
- **Risk quantification** — ALE modeling with FAIR-informed assumptions, grounded in industry data sources
- **Executive communication** — business-language translation of technical risk findings
- **Financial justification** — ROI modeling tied directly to control effectiveness data
- **Roadmap prioritization** — risk-based sequencing, not feature listing

---

## What I Would Do Differently

Honest self-assessment matters in GRC. If I were rebuilding this engagement:

1. **Tighter impact ranges.** A $50M–$500M range signals methodology gaps. I've since revised the model to a $8M–$100M range with explicit scenario definitions.
2. **Actual FAIR decomposition.** I cited FAIR but only executed ALE math. A real FAIR analysis requires threat event frequency, contact frequency, and loss magnitude broken into primary and secondary forms. I would build that out.
3. **Regulatory layer.** A pharma company with proprietary research should be assessed for applicable privacy and IP protection obligations. I did not cover this.
4. **Control effectiveness sourcing.** I cited industry studies for control effectiveness (e.g., MFA reduces credential attacks ~50%) but did not link to specific sources inline. That needs to be documented.

---

## About

**Role simulated:** Cybersecurity Compliance
**Frameworks used:** NIST CSF 1.1, ALE risk model, FAIR methodology
**Tools/sources:** Qualys (referenced in scenario), Microsoft Azure/O365 environment, Verizon DBIR, IBM Cost of a Data Breach Report
**Completed:** May 2026 | GRC Mastery Capstone

---

*Kelvin Guzman | [LinkedIn](https://linkedin.com) | Analyst*
