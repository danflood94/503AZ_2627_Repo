# Student Policy Authoring Guide

These are policy topics and drafting prompts, not approved GridSync policies. The
team must produce **one group-wide set** of final policies; do not make separate
copies for each component. Students contribute to and review the shared documents,
with an assigned policy lead coordinating each one. Record group approval,
version/review date, and links from the [Statement of Applicability](../statement-of-applicability.md)
and relevant component mappings. An IAM policy is a technical permission document;
it does not replace an organizational policy.

## Minimum Policy Set

The examples below are starting points only. Adapt one or two example elements,
then complete each policy using the prompts in its linked guide.

| Policy to author | Example elements (adapt, do not copy as a complete policy) | Group completion guidance | Annex A prompts |
|---|---|---|---|
| [Information Security Policy](examples/information-security-policy.md) | Commitment to protect in-scope information; assigned security responsibilities | Define scope, objectives, roles, decision-making, exceptions, approval, and review | A.5.1; consider A.5.2 |
| [Access Control Policy](examples/access-control-policy.md) | Approval before access; review or removal when access is no longer needed | Define access scope, approvers, least-privilege process, review frequency, exceptions, and evidence | A.5.15, A.5.18; consider A.8.2 |
| [Employee Security Awareness and Training Policy](examples/security-awareness-training-policy.md) | Guidance before access; record whether required training is complete | Define audience, learning goals, timing, refresh triggers, follow-up, and privacy-safe evidence | A.6.3 |
| [Monitoring and Maintenance Policy](examples/monitoring-and-maintenance-policy.md) | Review selected security events; record maintenance changes | Select relevant events/assets, owners, review/escalation process, maintenance approach, and evidence | A.8.15, A.8.16; consider A.8.8 |

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
