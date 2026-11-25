# Assessment Alignment Guide

Use this guide to organize evidence for the three assessment phases. It supplements
the marking criteria; it does not guarantee a grade or replace module instructions.
Keep the distinction clear between group deliverables (Phase 1 and Phase 2) and
each student's own reflective analysis (Phase 3).

## Phase 1 — Group Cloud Security Framework and Implementation (50%)

The repository should show a coherent risk-to-control chain:

1. **ATV:** Identify assets, owners, credible threats, specific vulnerabilities,
   risk ratings, treatments, and proposed mitigations. Go beyond obvious settings:
   assess trust boundaries, dependencies, accidental and malicious scenarios,
   logging/monitoring gaps, availability, and organizational/people risks. Explain
   ratings and treatment choices, including residual risk.
2. **Four security layers:** Address Network, Instance/Service, Server/OS, and Data.
   Show how controls reinforce one another (defence in depth), not just a list of
   settings. Respect AWS Shared Responsibility for RDS and DynamoDB; do not claim
   customer OS controls over managed services.
3. **Working implementation:** Commit actual configurations and policies, explain
   relevant decisions, and capture sanitized validation evidence. State Learner
   Lab limitations and distinguish simulator results from deployed behavior.
4. **ISO mapping:** For each relevant control, verify the control ID and title
   against the applicable ISO/IEC 27001:2022 and ISO/IEC 27017 material available
   to the team. Explain applicability and how the implementation addresses the
   risk; identify an artifact and evidence. Do not copy control numbers without
   justification, and do not imply certification.
5. **Governance:** Complete the group-wide policy set and SoA alongside technical
   IAM/resource policies. Show approval, ownership, implementation status, and
   evidence for organizational and people controls.

For a stronger submission, make each control testable: state the intended outcome,
the validation performed, its result, and any remaining gap. Keep commit history
regular and attributable to individual contributions.

## Phase 2 — Group Presentation (30%)

Prepare an integrated, time-bounded live demonstration in the Integration Lead's
Learner Lab. Show the architecture, selected before/after risks, controls across
the four layers, validation evidence, and how the shared policies and component
configurations fit together. Each component owner should be ready to defend key
decisions and explain constraints, trade-offs, and remaining risks.

Support technical and standards-based claims with relevant sources (for example,
the applicable standards, AWS documentation, NIST guidance, or peer-reviewed
research). Add APA 7th edition in-text citations to slides and a correctly formatted
reference list at the end. Use the university's APA 7 guidance for exact formatting;
do not include uncited sources or present a source as support for a claim it does
not make. Keep a source record while researching:

| Claim / decision supported | Source and locator | Slide citation | APA 7 reference checked |
|---|---|---|---|
| To be completed by the group | To be completed | To be completed | To be completed |

Rehearse the integration and presentation. Start the Learner Lab at least 30 minutes
before the demo and account for its four-hour auto-stop.

## Phase 3 — Individual Reflective Report (20%)

Each student should critically evaluate their assigned component and their own
contribution, not simply describe configuration steps. Use implementation and test
evidence to assess:

- **Confidentiality:** Did the controls limit access and protect data/secrets?
  What evidence supports that conclusion, and what exposure remains?
- **Integrity:** Did the controls prevent or detect unauthorized or accidental
  changes? How was this validated?
- **Availability:** Did resilience, monitoring, and recovery controls meet the
  project's needs? What limitations remain?

Discuss control effectiveness, trade-offs, false assumptions, Learner Lab limits,
residual risks, and realistic improvements. Connect the analysis to relevant
standards, technical documentation, or academic research; support assertions with
APA 7th edition in-text citations and a reference list. Use the student's own
analysis and the module's academic-integrity requirements.

## Final Readiness Check

- ATV rows, SoA decisions, mappings, and evidence references are consistent.
- Every implemented control has a clear owner, configuration/policy reference, and
  suitable validation evidence.
- ISO/IEC 27001 and 27017 mappings are checked, justified, and scoped accurately.
- Shared group policies are approved and presentation-ready; component differences
  are captured in mappings rather than duplicate policies.
- The presentation demonstrates integration and includes APA 7 citations and
  references.
- Each student's reflection evaluates confidentiality, integrity, and availability
  using evidence and relevant sources.
