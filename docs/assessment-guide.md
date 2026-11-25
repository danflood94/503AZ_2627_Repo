# Cloud Security Assessment Alignment Guide

This reusable guide summarizes the assessment phases, evidence expectations, and
mark-band progression. It supplements the official assessment brief and does not
replace module instructions or guarantee a grade.

## Assessment Overview

| Phase | Assessment | Weight | Main evidence |
|---|---|---:|---|
| 1 | Group Cloud Security Framework and Implementation | 50% | Technical repository, Asset-Threat-Vulnerability (ATV) assessment, cloud-lab implementation, and ISO mapping |
| 2 | Group Presentation | 30% | Integrated live demonstration, communication and defence of decisions, and APA 7th edition citations |
| 3 | Individual Reflective Report | 20% | Critical evaluation of implemented controls against the CIA Triad, supported by research and APA 7th edition references |

## Phase 1 — Group Cloud Security Framework and Implementation (50%)

This phase assesses the technical repository, ATV Risk Assessment, cloud-lab
implementation, and ISO mapping.

### Evidence and Quality Checklist

- **ATV:** Identify assets and owners, credible threats, specific vulnerabilities,
  risk ratings, treatments, and proposed mitigations. Look beyond obvious
  misconfigurations to consider dependencies, trust boundaries, subtle attack or
  failure scenarios, and organizational risks. Explain ratings and treatment
  choices.
- **Four security layers:** Address Network, Instance, Server, and Data controls.
  Show how controls reinforce one another in a defence-in-depth strategy.
- **Implementation:** Commit actual configurations and policies, explain decisions,
  and capture suitable validation evidence. State lab limitations and distinguish
  simulated results from deployed behavior.
- **Shared responsibility:** Identify which controls are managed by the cloud
  provider and which remain the customer's responsibility, especially for managed
  services. Do not claim control over provider-managed layers.
- **ISO mapping:** Verify control identifiers and titles against the applicable
  ISO/IEC 27001 and ISO/IEC 27017 materials. Justify applicability and show how
  controls address risks; link configuration and evidence. Do not include
  unexplained control numbers or imply certification.
- **Governance:** Include organizational and people controls, documented policies,
  ownership, approval, status, and evidence alongside technical IAM/resource
  policies.

| Mark band | General standard |
|---|---|
| **80–100% Exceptional / Outstanding** | Masterful, well-documented implementation; ATV identifies complex and subtle risks; controls across all four layers demonstrate proactive defence in depth; ISO mapping is highly accurate and comprehensively justified. |
| **70–79% Excellent** | Comprehensive and effective solution; thorough, accurate ATV; controls work and are well documented; ISO mapping is logical and well justified. |
| **60–69% Very Good** | Strong solution that secures the environment; significant risks identified; controls function across the layers; mapping is structured and clearly connected to controls. |
| **50–59% Good** | Core requirements met; main risks identified but with limited detail; all layers addressed with minor errors or inefficiencies; some mapping rationale is inconsistent. |
| **40–49% Sufficient (Pass)** | Basic attempt; ATV is incomplete or misses risks; implementation is basic and may have significant layer errors; ISO mapping is incomplete or poorly structured. |
| **0–39% Fail** | ATV or mapping is absent or fundamentally flawed; controls are missing or ineffective, leaving significant risks unaddressed. |

For stronger evidence, make controls testable: state the intended outcome, validation
method, result, and remaining gap. Keep contributions and configuration changes
traceable.

## Phase 2 — Group Presentation (30%)

This phase assesses the live demonstration, framework integration, communication
of findings, defence of technical decisions, and APA 7th edition referencing on
presentation materials.

### Evidence and Quality Checklist

- Demonstrate that the components and controls integrate and function together.
- Explain important findings, control choices, trade-offs, limitations, and residual
  risks; be prepared to defend decisions during questions or a viva.
- Support claims with relevant standards, regulatory material, technical guidance,
  or academic research. Use accurate APA 7th edition in-text citations on slides
  and a complete reference list.
- Rehearse the demonstration and confirm the required lab environment is available
  for the presentation.

| Mark band | General standard |
|---|---|
| **80–100% Exceptional / Outstanding** | Comprehensive live demonstration; robust viva defence with explicit, relevant research or standards; flawless APA 7th edition citations and references. |
| **70–79% Excellent** | Demonstration proves integration and security; decisions are substantiated with appropriate sources; viva answers justify configurations; APA 7th edition has negligible errors. |
| **60–69% Very Good** | Functional demonstration and logical integration explanation; accurate answers, though limited synthesis of research; minor citation inconsistencies. |
| **50–59% Good** | Core functions demonstrated, but explanation is mostly descriptive; weak connection to external sources in the viva; noticeable APA errors or omissions. |
| **40–49% Sufficient (Pass)** | Partially successful demonstration; minimal theoretical understanding and limited standards references; significant citation errors or missing references. |
| **0–39% Fail** | Integration is not demonstrated or presentation is disorganized; little understanding of controls or relevant sources; references are absent or academic-integrity requirements are breached. |

Keep a source record while preparing:

| Claim / decision supported | Source and locator | Slide citation | APA 7th edition reference checked |
|---|---|---|---|
| To be completed by the group | To be completed | To be completed | To be completed |

## Phase 3 — Individual Reflective Report (20%)

This phase assesses critical analysis of implemented controls against the CIA
Triad, use of relevant standards, regulatory, technical, or academic research, and
APA 7th edition referencing.

### Evidence and Quality Checklist

Each student should critically evaluate their assigned work and contribution rather
than only describe implementation steps. Use evidence to assess:

- **Confidentiality:** Did the controls limit unauthorized access and protect
  information? What evidence supports the conclusion, and what exposure remains?
- **Integrity:** Did the controls prevent or detect unauthorized or accidental
  changes? How was effectiveness validated?
- **Availability:** Did resilience, monitoring, and recovery controls meet the
  stated needs? What limitations remain?

Discuss control effectiveness, trade-offs, assumptions, residual risks, and
realistic improvements. Support assertions with relevant research and use APA 7th
edition in-text citations and a reference list.

| Mark band | General standard |
|---|---|
| **80–100% Exceptional / Outstanding** | Deep, objective critical analysis; effectively synthesizes relevant research to support assertions; flawless APA 7th edition citations and references. |
| **70–79% Excellent** | Thorough critical evaluation; arguments consistently supported by research; clear evaluation against the CIA Triad; negligible referencing errors. |
| **60–69% Very Good** | Sound CIA Triad analysis and good use of research; mostly correct APA 7th edition with minor inconsistencies. |
| **50–59% Good** | Reflection is mainly descriptive; limited research; superficial CIA Triad evaluation; noticeable APA errors. |
| **40–49% Sufficient (Pass)** | Little critical evaluation or external research; minimal CIA Triad application; significant citation errors or omissions. |
| **0–39% Fail** | Reflection is absent or shows little understanding; no meaningful research or CIA Triad analysis; widespread referencing or academic-integrity failures. |

## Final Readiness Check

- ATV, control mappings, implementation, and evidence tell a consistent story.
- All four security layers are addressed, with justified and validated controls.
- ISO mappings are accurate, applicable, and explained.
- The group presentation demonstrates integration and cites sources in APA 7th
  edition format.
- Each individual reflection critically evaluates confidentiality, integrity, and
  availability using evidence and relevant research.
