# GridSync Energy — Statement of Applicability

## Purpose and Use

Use this working SoA to record which ISO/IEC 27001:2022 Annex A controls apply to
the GridSync project, why they apply or do not apply, their implementation status,
the owner, and evidence. This is a student project record, not a certification or
claim of compliance. Review the full Annex A control set against the agreed scope;
the starter rows below are prompts, not a complete control set or predetermined
applicability decisions.

Every decision must be completed by the team. Do not mark a control implemented
solely because a policy or AWS configuration file exists: record how it is
implemented and what evidence demonstrates it. Include organizational controls
such as access-control governance and personnel awareness/training, not only
technical AWS/IAM controls.

## SoA Register

| ISO/IEC 27001:2022 Annex A control | Applicable? (Yes/No/To assess) | Justification / scope | Implementation status | Owner | Policy/configuration reference | Evidence reference |
|---|---|---|---|---|---|---|
| A.5.15 Access control | To assess | Decide based on GridSync information, users, and services in scope | Not assessed | Team / component owners | `policies/access-control-policy.md`; component IAM/resource policies | `components/<component>/evidence/` |
| A.5.18 Access rights | To assess | Consider granting, reviewing, changing, and removing access | Not assessed | Team / component owners | `policies/access-control-policy.md`; component IAM/resource policies | Access review and Policy Simulator records in component `evidence/` |
| A.6.3 Information security awareness, education and training | To assess | Consider awareness needs for everyone performing GridSync project work | Not assessed | Team lead / all members | `policies/security-awareness-training-policy.md` | Redacted or synthetic completion evidence in component `evidence/` |
| A.5.23 Information security for use of cloud services | To assess | Consider AWS Learner Lab responsibilities, constraints, and service use | Not assessed | Integration Lead / component owners | Component configuration and Shared Responsibility notes | Lab configuration and review evidence |
| A.8.2 Privileged access rights | To assess | Consider administrative access to the lab and tier resources | Not assessed | Component owners | IAM/resource policies and access procedure | Policy Simulator evidence and access review |
| A.8.9 Configuration management | To assess | Consider controlled, reviewed, and traceable configuration changes | Not assessed | Component owners | `components/<component>/configs/` | Git history and configuration review evidence |
| A.8.15 Logging | To assess | Consider recording and protecting relevant security events | Not assessed | Component owners | Service logging configuration and procedures | Sanitized log/configuration evidence |
| A.8.24 Use of cryptography | To assess | Consider protection of data in transit and at rest | Not assessed | Component owners | TLS, encryption, and key configuration | Sanitized configuration and verification evidence |

## Required Organizational Policy Artifacts

Complete and review the two policy starters before submission:

- [Access Control Policy](policies/access-control-policy.md): define who may request,
  approve, receive, review, and revoke access; address least privilege and exceptions.
- [Security Awareness and Training Policy](policies/security-awareness-training-policy.md):
  define project-relevant security learning, when it is completed, and how completion
  is evidenced.

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
