# Web Tier

## Component Overview and Owner

- **Student name:** To be assigned
- **Baseline vulnerabilities to assess:** HTTP without TLS, public-subnet placement,
  exposed application surface, and instance metadata / host-hardening configuration.
- **Scope:** Web entry point, network path to the application, EC2 configuration,
  web-server/OS controls, and protection of data handled by the portal.

## 4-Layer Security Controls and ISO Mapping

| Layer (Network/Instance/Server/Data) | Risk / Baseline Flaw | Control Implemented | Config File Reference (configs/...) | Evidence (evidence/...) | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|---|
| Network | Public subnet and unencrypted HTTP | Record the allowed client path and proposed HTTPS termination | `configs/` | `evidence/` | A.8.20 Network security; A.8.24 Use of cryptography | 13.1.1 Network controls |
| Instance | Publicly addressed EC2 instance | Document exposure, least-privilege profile use, and metadata controls | `configs/` | `evidence/` | A.8.9 Configuration management | 12.1.5 Administrator's operational security |
| Server | Web server may be unpatched or over-permissive | Document secure Nginx configuration, patching, and service hardening | `configs/` | `evidence/` | A.8.8 Management of technical vulnerabilities | 12.6.1 Management of technical vulnerabilities |
| Data | Portal traffic may be observed or altered | Document TLS and data-minimisation controls | `configs/` | `evidence/` | A.8.24 Use of cryptography | 13.1.1 Network controls |

## Cross-Cutting Policy Controls

These are references to the group's shared policies, not separate web-tier policy
copies. Map the shared controls here and record web-tier-specific implementation
and evidence.

| Control | Web-tier application | Policy / configuration reference | Evidence reference | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|
| Access control and access rights | Apply the group access policy to web configuration and workload permissions | `docs/policies/access-control-policy.md`; relevant `configs/` IAM/resource policies | Shared approval/review in `docs/policies/evidence/`; tier IAM simulations in `evidence/` | A.5.15 Access control; A.5.18 Access rights | Team to map applicable cloud guidance |
| Security awareness and training | Apply group training expectations to public HTTP exposure, change handling, and secret protection | `docs/policies/security-awareness-training-policy.md` | Shared sanitized training record in `docs/policies/evidence/` | A.6.3 Information security awareness, education and training | Team to map applicable cloud guidance |
| Information security policy | Apply shared security roles and expectations to web-tier work | `docs/policies/information-security-policy.md` | Shared policy approval/review in `docs/policies/evidence/` | A.5.1 Policies for information security | Team to map applicable cloud guidance |
| Monitoring and maintenance | Apply group monitoring/maintenance process to web logs, configuration, and patch follow-up | `docs/policies/monitoring-and-maintenance-policy.md`; relevant `configs/` | Shared policy plus web-tier monitoring evidence in `evidence/` | A.8.15 Logging; A.8.16 Monitoring activities; A.8.8 Management of technical vulnerabilities | Team to map applicable cloud guidance |

## Configuration Maintenance and Checkpoint Log

| Date | Checkpoint | Config File Updated | Summary of Change |
|---|---|---|---|
| To be recorded | Week 3 | `configs/` | Initial assessment and ownership recorded |
| To be recorded | Week 5 | `configs/` | Network and instance controls committed |
| To be recorded | Week 6 | `configs/` | Server and data controls finalized |

## Tier-Specific Prompts

- Replace direct public HTTP access with HTTPS through a suitably configured load balancer.
- Assess IMDSv2, instance-profile permissions, and security-group scope.
- Harden Nginx, remove unused services, and document patching and log handling.
- Keep secrets out of user data and source control; document how the application obtains them.

## Individual Reflection (Phase 3)

Use your evidence to evaluate web-tier confidentiality (traffic and secrets),
integrity (content/configuration changes), and availability (failure and recovery).
Critically discuss effectiveness, limitations, and residual risk, supporting
technical claims with research and APA 7th edition citations. See the
[assessment alignment guide](../../docs/assessment-guide.md).
