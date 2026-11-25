# Access Control Policy — Group Drafting Guide

- **Group policy lead:** To be assigned
- **Group approval:** To be recorded in the final policy
- **Version / review date:** Complete in the group-authored policy

This is a drafting guide, not a finished policy. The group should write and approve
the policy for the GridSync project, using the prompts below and the team's agreed
scope.

## Topics to Address

- Which people, project information, AWS resources, and configuration repositories
  are in scope?
- Who may request, approve, implement, review, and revoke access? How are duties
  separated where practical?
- How are least privilege, role changes, periodic access reviews, and access
  removal handled?
- How are credentials and private keys protected, and how are exceptions approved,
  time-limited, and reviewed?
- Which IAM capabilities are available in Learner Lab? Document the existing lab
  identity/profile and limitations; do not create IAM users, roles, or instance
  profiles where the lab blocks them.

## Implementation and Evidence Prompts

Reference the AWS IAM/resource policies separately from this organizational policy.
Use the AWS IAM Policy Simulator for supported allow/deny cases and record the
principal, action, resource, expected and simulated result, policy reference, and
date. Store sanitized access-review and simulator evidence in the owning component's
`evidence/` folder; do not include credentials or personal data. Link the final
policy and evidence in the component mapping and SoA.
