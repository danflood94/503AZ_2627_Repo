# RDS Tier

## Component Overview and Owner

- **Student name:** To be assigned
- **Baseline vulnerabilities to assess:** Single-AZ availability, limited backup
  recovery, managed-service network placement, and database access/configuration.
- **Scope:** RDS service parameters, network access, database authentication,
  logging, backup/recovery, and the AWS Shared Responsibility boundary.

## 4-Layer Security Controls and ISO Mapping

| Layer (Network/Instance/Server/Data) | Risk / Baseline Flaw | Control Implemented | Config File Reference (configs/...) | Evidence (evidence/...) | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|---|
| Network | DB subnet group uses public subnets; review connectivity boundary | Document private placement and narrow application-only access | `configs/` | `evidence/` | A.8.20 Network security | 13.1.1 Network controls |
| Instance | Single-AZ service can be unavailable after an AZ incident | Assess Multi-AZ and service-level monitoring options | `configs/` | `evidence/` | A.8.14 Redundancy of information processing facilities | 12.1.3 Capacity management |
| Server | Underlying managed host/OS is AWS-operated | Document the Shared Responsibility boundary and customer database configuration | `configs/` | `evidence/` | A.5.23 Information security for use of cloud services | 12.1.5 Administrator's operational security |
| Data | Recovery, encryption, and credentials require explicit review | Document encryption, backup/PITR alternatives where supported, retention, and secret handling | `configs/` | `evidence/` | A.8.13 Information backup; A.8.24 Use of cryptography | 12.3.1 Information backup |

## Configuration Maintenance and Checkpoint Log

| Date | Checkpoint | Config File Updated | Summary of Change |
|---|---|---|---|
| To be recorded | Week 3 | `configs/` | Initial assessment and ownership recorded |
| To be recorded | Week 5 | `configs/` | Network and instance/service controls committed |
| To be recorded | Week 6 | `configs/` | Server responsibility and data controls finalized |

## Tier-Specific Prompts

- Prefer private subnet placement and restrict database ingress to the required application security group.
- Assess Multi-AZ based on availability requirements and Learner Lab limits.
- Enable encryption and suitable backup retention; never store a reusable password in the template or repository.
- Explain that AWS manages the host OS; document customer-controlled service parameters, logging, access policy, and patch-window choices.
