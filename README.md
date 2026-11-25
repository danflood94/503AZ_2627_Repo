# Module 503AZ — Securing Cloud Systems

## Project Overview

GridSync Energy is building a Smart Grid Analytics Platform to collect and analyse
meter telemetry. This repository supports a four-tier security project: a web tier,
a relational database (RDS) tier, a bastion-host management tier, and a DynamoDB
telemetry tier. Teams assess the supplied architecture, propose controls, maintain
configuration artifacts, and integrate their work for a live demonstration.

The CloudFormation file in `baseline/` is a Learner Lab-compatible teaching
baseline. Its web portal is intentionally reachable from the internet over
unencrypted HTTP so teams can assess and harden its network, instance, server, and
data layers. It also leaves review topics such as single-AZ RDS, disabled DynamoDB
point-in-time recovery, and a missing DynamoDB gateway endpoint. Both VPC subnets
are public. RDS has a public endpoint, but direct MySQL access is restricted to the
configured assessment CIDR plus the web security group; set `DBAccessCidr` to an
authorized tester's current public IP in `/32` notation, never `0.0.0.0/0`. SSH
remains limited to its configured trusted CIDR. Storage is encrypted, and the
database password is supplied at deployment rather than embedded in the template.
Use only a disposable Learner Lab stack, keep real or sensitive data out of it, and
remove the stack when assessment is complete.

## Team and Component Allocation

| Component | Assigned Student | GitHub Username | Folder Path |
|---|---|---|---|
| Web tier | To be assigned | To be assigned | `components/web-tier/` |
| RDS tier | To be assigned | To be assigned | `components/rds-tier/` |
| Bastion host | To be assigned | To be assigned | `components/bastion-host/` |
| DynamoDB tier | To be assigned | To be assigned | `components/dynamodb-tier/` |

## Architecture Diagram

Replace this placeholder with the team's hardened architecture diagram. Save the
diagram as `docs/architecture.png` and update the link if using another path.

![GridSync hardened architecture diagram](docs/architecture.png)

## Risk Assessment and Statement of Applicability

Maintain the team's consolidated [ATV Risk Assessment](docs/atv-risk-assessment.md)
and [Statement of Applicability (SoA)](docs/statement-of-applicability.md) as
separate project records. Replace examples, make applicability decisions, and
merge each component owner's final risks and control evidence before submission.

## Individual Ownership and Configuration Rules

- Each student owns an assigned component and maintains its component-level
  ISO/IEC 27001 and ISO/IEC 27017 mapping in that component's `README.md`.
- The mapping must include organizational and people controls as well as technical
  controls. Complete the shared [Access Control Policy](docs/policies/access-control-policy.md)
  and [Security Awareness and Training Policy](docs/policies/security-awareness-training-policy.md),
  record their applicability and status in the SoA, and reference relevant policies
  and evidence from each component mapping. These policies are separate from AWS
  IAM identity, permissions, and resource policies.
- For IAM policies, use the AWS IAM Policy Simulator for supported allow/deny cases
  that can be assessed in Learner Lab. Save sanitized inputs and results in the
  component's `evidence/` folder, including principal, action, resource, expected
  and simulated decision, date, and any simulator limitations. Do not create IAM
  users, roles, or instance profiles that the lab blocks. A simulator result is
  not proof of deployed service behavior.
- Store and iteratively update real configuration artifacts in
  `components/<component>/configs/`, not just screenshots. Examples include AWS CLI
  scripts, hardened CloudFormation snippets, IAM/resource policies, `nginx.conf`,
  and `sshd_config`. Do not commit credentials, private keys, or other secrets.
- Store supporting screenshots, command output, and other verification evidence in
  `components/<component>/evidence/`. Redact account identifiers and sensitive data.
- Before submission, merge each owner's finalized ATV rows into the standalone
  register and complete the SoA decisions and evidence references.

## 4-Layer Security Guide (including Shared Responsibility)

Document controls and evidence against all four layers; identify the owner and
configuration artifact for each relevant control.

1. **Network:** VPC/subnet placement, routing, security groups, ingress/egress
   boundaries, load balancers, and service endpoints.
2. **Instance/Service:** EC2 instance profile and metadata settings, instance
   exposure, RDS/DynamoDB service parameters, service access policies, logging, and
   operational configuration.
3. **Server/OS:** For systems the team administers, document patching, services,
   host firewall, SSH, and web-server hardening. Do not claim OS-level control where
   AWS operates the underlying host or managed service.
4. **Data:** Data classification, encryption in transit and at rest, key choices,
   backup/recovery, retention, access, and audit evidence.

Access-control policy, staff/student awareness training, and other organizational
controls are cross-cutting: map and evidence them alongside the four technical
layers, rather than omitting them because they are not an AWS configuration.

For **RDS**, AWS manages the underlying host and managed database service
infrastructure; students should document this Shared Responsibility boundary rather
than claim access to the managed server OS. At the Instance/Service layer, assess
service parameters such as public accessibility, encryption, backups, and Multi-AZ,
along with database/network access, logging, and credential handling. At the
Server/OS layer, record AWS's managed-service responsibility and the customer's
responsibility for database configuration, patch-window choices, and secure use of
the service.

For **DynamoDB**, AWS manages the service infrastructure and server OS. Students
should record that boundary at the Instance and Server layers, then assess customer
responsibilities including table/service parameters, encryption and recovery,
IAM/resource policies, logging (including appropriate CloudTrail data events), and
private connectivity via a VPC Gateway Endpoint where suitable. A VPC endpoint
does not replace least-privilege policies.

## Formative Checkpoints and Deadlines

- **End of Week 3:** Initial ATV risk assessment matrix and component allocation.
- **Start of Week 5:** Network and Instance layer configuration artifacts committed.
- **Early Week 6:** Server and Data layer configuration artifacts committed; ready
  to present.
- **Phase 1 Repo Submission:** Monday of Week 6 at 18:00.

## AWS Learner Lab Group Workflow

Learner Labs are single-user sandboxes. Students develop and test individually in
their own labs; designate one **Integration Lead** to apply everyone's reviewed
`configs/` artifacts in a single lab for the Week 6 live demo. Start that lab at
least **30 minutes before** the demo and plan around the four-hour automatic stop.
Confirm changes are appropriate for the lab and avoid deploying unsafe public
exposures or real data.

## Git Commit History and AI Usage (Amber)

Make regular individual commits so the repository history provides authorship
evidence. Under the module's **Amber** AI usage rules, AI must not generate
functional code. If AI is used to help debug, record the prompt, the original error,
and an explanation of the fix in your own words, following the module's submission
guidance. Do not commit AI-generated functional code as your own work.
