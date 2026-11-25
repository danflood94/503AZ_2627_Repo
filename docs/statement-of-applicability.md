# GridSync Energy — Statement of Applicability

## Purpose and Use

Use this working, group-wide SoA to record which ISO/IEC 27001:2022 Annex A controls
apply to GridSync, why they apply or do not apply, implementation status, owner, and
evidence. The team maintains one SoA and one shared set of policies; component owners
contribute tier-specific implementation/evidence references rather than making
duplicate policies. This is a student project record, not a certification or claim
of compliance. Review the full Annex A control set against the agreed scope; the
starter rows are prompts, not a complete control set or predetermined applicability
decisions. Only two example rows are included below. They are illustrative, not a
recommended complete control set.

Every decision must be completed by the team. Do not mark a control implemented
solely because a policy or AWS configuration file exists: record how it is
implemented and what evidence demonstrates it. Include organizational controls
such as access-control governance and personnel awareness/training, not only
technical AWS/IAM controls. Review the full Annex A catalogue and add, remove, or
justify controls for the agreed scope; do not treat these examples as a checklist
of all applicable controls.

## SoA Register

| ISO/IEC 27001:2022 Annex A control | Applicable? (Yes/No/To assess) | Justification / scope | Implementation status | Owner | Policy/configuration reference | Evidence reference |
|---|---|---|---|---|---|---|
| A.5.15 Access control [EXAMPLE - ADAPT] | To assess | Example: determine whether access to in-scope resources needs formal authorization; write the scope-specific rationale | To assess | Group policy lead / relevant component owner | `policies/examples/access-control-policy.md`; applicable IAM/resource policy | Access review or supported policy-test evidence |
| A.6.3 Information security awareness, education and training [EXAMPLE - ADAPT] | To assess | Example: determine who needs security awareness and how the requirement applies to the project | To assess | Group policy lead | `policies/examples/security-awareness-training-policy.md` | Sanitized or synthetic completion evidence |

## Required Organizational Policy Artifacts

The team must collaboratively author, review, and approve one group-wide policy
for each of the four minimum topics in the [policy authoring guide](policies/README.md):
Information Security, Access Control, Employee Security Awareness and Training,
and Monitoring and Maintenance. The linked policy files provide prompts only;
complete them for the project scope and prepare the final policies and evidence for
the presentation.

These are governance/process controls and are distinct from AWS IAM policies.
Reference each policy from relevant component mappings and the SoA. Where a policy
is not applicable, state why and record the team's decision rather than leaving it
blank.

## AWS IAM Policy Simulator Evidence

For each IAM policy that can be assessed in the Learner Lab, capture at least one
intended-allow case and one intended-deny case where meaningful. Record the
simulated principal, action, resource, relevant conditions, expected result,
simulator result, date, and policy version or sanitized policy reference. Store
evidence in the owning component's `evidence/` folder and link it from the component
mapping and SoA.

Use only simulator features and lab identities available to the team. Do not try to
create blocked IAM users, roles, or instance profiles. The simulator evaluates
policy logic within its supported scope; it does not prove that a deployed AWS
service is configured correctly or replace a live, authorized validation.
