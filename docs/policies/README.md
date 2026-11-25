# Student Policy Authoring Guide

These are policy topics and drafting prompts, not approved GridSync policies. The
team must produce **one group-wide set** of final policies; do not make separate
copies for each component. Students contribute to and review the shared documents,
with an assigned policy lead coordinating each one. Record group approval,
version/review date, and links from the [Statement of Applicability](../statement-of-applicability.md)
and relevant component mappings. An IAM policy is a technical permission document;
it does not replace an organizational policy.

## Minimum Policy Set

| Policy to author | Minimum topics to address | ISO/IEC 27001:2022 Annex A prompts | Suggested evidence |
|---|---|---|---|
| [Information Security Policy](information-security-policy.md) | Purpose, scope, security objectives, roles, responsibilities, risk/compliance expectations, exceptions, approval and review | A.5.1 Policies for information security; consider A.5.2 Roles and responsibilities | Approved student-authored policy, review record, assigned responsibilities |
| [Access Control Policy](access-control-policy.md) | Access request/approval, least privilege, access review/removal, privileged access, credentials, exceptions | A.5.15 Access control; A.5.18 Access rights; consider A.8.2 Privileged access rights | Access review record; sanitized IAM Policy Simulator allow/deny cases where supported |
| [Employee Security Awareness and Training Policy](security-awareness-training-policy.md) | Induction, role-specific training, refreshers, completion tracking, missed-training follow-up | A.6.3 Information security awareness, education and training | Training outline/checklist and sanitized or synthetic completion evidence |
| [Monitoring and Maintenance Policy](monitoring-and-maintenance-policy.md) | What is monitored, ownership, review frequency, log protection, patch/vulnerability review, maintenance windows, escalation, evidence retention | A.8.15 Logging; A.8.16 Monitoring activities; consider A.8.8 Management of technical vulnerabilities | Sanitized log/monitoring review, maintenance record, vulnerability/patch review |

Use the Annex A references as prompts, not automatic applicability decisions. The
team must review the applicable control, justify its decision in the SoA, and
identify evidence. Never commit credentials, private keys, or personal training
records.

## Group Ownership and Presentation Readiness

Before the presentation, the team should:

1. Assign a policy lead and reviewers for each of the four group-wide policies.
2. Replace prompts with concise, project-specific policy statements; record group
   approval, version, date, and review owner.
3. Agree the relevant SoA applicability, rationale, implementation status, and
   evidence for each policy.
4. Ask each component owner to explain how the shared policy applies to their tier,
   with linked configuration or process evidence rather than duplicate policy text.
5. Prepare a short presentation summary: policy purpose, key responsibilities,
   evidence shown, Learner Lab limitations, and any remaining gaps/treatment.
   Support claims on presentation slides with APA 7th edition citations and include
   cited sources in the final reference list.

Keep shared policy approval/review records and sanitized group training evidence
under `docs/policies/evidence/`. Keep technical implementation evidence and
component-specific IAM Policy Simulator results in the owning component's
`evidence/` directory. Do not include personal or confidential records.

## Additional Policies to Consider

Choose and justify additional policies based on the risk assessment and project
scope. Possible topics include:

- Incident reporting and response.
- Data classification, handling, retention, and secure deletion.
- Backup, recovery, and continuity.
- Change and configuration management.
- Acceptable use and secure development.
- Cloud service use, supplier responsibilities, and AWS Shared Responsibility.
- Cryptography and key management.
- Vulnerability management and security testing.

## AWS IAM Policy Simulator

Use the AWS IAM Policy Simulator for supported policy scenarios that are available
in the Learner Lab. Record the principal, action, resource, relevant conditions,
expected and simulated decisions, policy version/reference, date, and limitations.
Capture both allowed and denied outcomes where meaningful. Store sanitized evidence
in the owning component's `evidence/` folder and link it from the mapping and SoA.
The simulator does not replace organizational access approval/review, prove deployed
service behavior, or override Learner Lab restrictions. Do not attempt to create
blocked IAM users, roles, or instance profiles.
