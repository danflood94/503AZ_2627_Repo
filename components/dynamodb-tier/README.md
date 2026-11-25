# DynamoDB Tier

## Component Overview and Owner

- **Student name:** To be assigned
- **Baseline vulnerabilities to assess:** Point-in-time recovery is disabled and
  the VPC has no DynamoDB Gateway Endpoint; review policies, logging, and data access.
- **Scope:** DynamoDB table and data controls, IAM/resource policies, private
  connectivity, audit events, and the AWS Shared Responsibility boundary.

## 4-Layer Security Controls and ISO Mapping

| Layer (Network/Instance/Server/Data) | Risk / Baseline Flaw | Control Implemented | Config File Reference (configs/...) | Evidence (evidence/...) | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|---|
| Network | No VPC Gateway Endpoint in baseline | Assess endpoint routing and endpoint policy for private access | `configs/` | `evidence/` | A.8.20 Network security | 13.1.1 Network controls |
| Instance | Workload identity may be broader than required | Document least-privilege IAM and resource-policy conditions | `configs/` | `evidence/` | A.5.15 Access control | 9.5.1 Access control |
| Server | AWS operates DynamoDB servers and underlying OS | State the AWS Shared Responsibility boundary; do not claim customer OS access | `configs/` | `evidence/` | A.5.23 Information security for use of cloud services | 12.1.5 Administrator's operational security |
| Data | Point-in-time recovery is disabled in baseline | Assess PITR, encryption, retention, and CloudTrail data events | `configs/` | `evidence/` | A.8.13 Information backup; A.8.15 Logging | 12.3.1 Information backup |

## Cross-Cutting Policy Controls

These are references to the group's shared policies, not separate DynamoDB policy
copies. Map the shared controls here and record DynamoDB-specific implementation
and evidence.

| Control | DynamoDB-tier application | Policy / configuration reference | Evidence reference | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|
| Access control and access rights | Apply group approval, least privilege, review, and removal expectations to table/data access | `docs/policies/examples/access-control-policy.md`; relevant `configs/` IAM/resource policies | Shared approval/review in `docs/policies/evidence/`; tier IAM simulations in `evidence/` | A.5.15 Access control; A.5.18 Access rights | Team to map applicable cloud guidance |
| Security awareness and training | Apply group training expectations to telemetry sensitivity, data access, and service boundaries | `docs/policies/examples/security-awareness-training-policy.md` | Shared sanitized training record in `docs/policies/evidence/` | A.6.3 Information security awareness, education and training | Team to map applicable cloud guidance |
| Information security policy | Apply shared security roles and data-protection expectations to DynamoDB | `docs/policies/examples/information-security-policy.md` | Shared policy approval/review in `docs/policies/evidence/` | A.5.1 Policies for information security | Team to map applicable cloud guidance |
| Monitoring and maintenance | Apply group process to table access/audit events, configuration, and service notifications | `docs/policies/examples/monitoring-and-maintenance-policy.md`; relevant `configs/` | Shared policy plus DynamoDB monitoring evidence in `evidence/` | A.8.15 Logging; A.8.16 Monitoring activities; A.8.8 Management of technical vulnerabilities | Team to map applicable cloud guidance |

## Configuration Maintenance and Checkpoint Log

| Date | Checkpoint | Config File Updated | Summary of Change |
|---|---|---|---|
| To be recorded | Week 3 | `configs/` | Initial assessment and ownership recorded |
| To be recorded | Week 5 | `configs/` | Network and instance/service controls committed |
| To be recorded | Week 6 | `configs/` | Server responsibility and data controls finalized |

## Tier-Specific Prompts

- Assess a DynamoDB VPC Gateway Endpoint, route-table association, and restrictive endpoint policy.
- Enable point-in-time recovery and document the recovery objective and retention needs.
- Review encryption settings and least-privilege IAM/resource policies for the table and indexes.
- Consider CloudTrail data events; document AWS's responsibility for the server/OS and the customer's controls.

## Individual Reflection (Phase 3)

Use your evidence to evaluate telemetry confidentiality (table/data access),
integrity (unauthorized or accidental item changes), and availability (recovery and
service access). Critically discuss AWS/customer responsibility boundaries,
effectiveness, limitations, and residual risk, supporting claims with research and
APA 7th edition citations. See the
[assessment alignment guide](../../docs/assessment-guide.md).
