# Bastion Host

## Component Overview and Owner

- **Student name:** To be assigned
- **Baseline vulnerabilities to assess:** Public management entry point, SSH
  exposure, instance permissions, and host-level hardening.
- **Scope:** Administrative access path, network restrictions, EC2 configuration,
  operating-system controls, and evidence of authorized access.

## 4-Layer Security Controls and ISO Mapping

| Layer (Network/Instance/Server/Data) | Risk / Baseline Flaw | Control Implemented | Config File Reference (configs/...) | Evidence (evidence/...) | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|---|
| Network | Publicly addressed administrative host | Restrict source CIDRs or assess private access alternatives | `configs/` | `evidence/` | A.8.20 Network security | 13.1.1 Network controls |
| Instance | Unnecessary permissions or metadata exposure | Review instance profile scope, IMDSv2, and patch configuration | `configs/` | `evidence/` | A.8.9 Configuration management | 12.1.5 Administrator's operational security |
| Server | SSH and OS defaults may be insufficiently hardened | Document SSH configuration, updates, host firewall, and logging | `configs/` | `evidence/` | A.8.8 Management of technical vulnerabilities | 12.6.1 Management of technical vulnerabilities |
| Data | Private keys or session data may be mishandled | Protect credentials and record secure session/log handling | `configs/` | `evidence/` | A.5.17 Authentication information | 9.5.1 Access control |

## Cross-Cutting Policy Controls

These are references to the group's shared policies, not separate bastion policy
copies. Map the shared controls here and record bastion-specific implementation
and evidence.

| Control | Bastion-tier application | Policy / configuration reference | Evidence reference | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|
| Access control and access rights | Apply group approval, least privilege, review, and removal expectations to administrative access | `docs/policies/examples/access-control-policy.md`; relevant `configs/` IAM/resource policies | Shared approval/review in `docs/policies/evidence/`; tier IAM simulations in `evidence/` | A.5.15 Access control; A.5.18 Access rights | Team to map applicable cloud guidance |
| Security awareness and training | Apply group training expectations to key handling, SSH/session risks, and lab restrictions | `docs/policies/examples/security-awareness-training-policy.md` | Shared sanitized training record in `docs/policies/evidence/` | A.6.3 Information security awareness, education and training | Team to map applicable cloud guidance |
| Information security policy | Apply shared security roles and secure-use expectations to bastion administration | `docs/policies/examples/information-security-policy.md` | Shared policy approval/review in `docs/policies/evidence/` | A.5.1 Policies for information security | Team to map applicable cloud guidance |
| Monitoring and maintenance | Apply group process to SSH/authentication review, OS updates, and vulnerability follow-up | `docs/policies/examples/monitoring-and-maintenance-policy.md`; relevant `configs/` | Shared policy plus bastion monitoring evidence in `evidence/` | A.8.15 Logging; A.8.16 Monitoring activities; A.8.8 Management of technical vulnerabilities | Team to map applicable cloud guidance |

## Configuration Maintenance and Checkpoint Log

| Date | Checkpoint | Config File Updated | Summary of Change |
|---|---|---|---|
| To be recorded | Week 3 | `configs/` | Initial assessment and ownership recorded |
| To be recorded | Week 5 | `configs/` | Network and instance controls committed |
| To be recorded | Week 6 | `configs/` | Server and data controls finalized |

## Tier-Specific Prompts

- Limit SSH ingress to a current trusted CIDR; do not leave administrative access open to all sources.
- Assess AWS Systems Manager Session Manager as an alternative to inbound SSH, subject to lab permissions.
- Disable password-based SSH, enforce key-based access, and document `sshd_config` hardening.
- Review IMDSv2, patching, audit logs, session recording options, and key handling.

## Individual Reflection (Phase 3)

Use your evidence to evaluate bastion confidentiality (sessions and keys), integrity
(administrative actions and auditability), and availability (authorized management
access and recovery). Critically discuss effectiveness, limitations, and residual
risk, supporting claims with research and APA 7th edition citations. See the
[assessment alignment guide](../../docs/assessment-guide.md).
