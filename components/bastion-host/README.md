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
