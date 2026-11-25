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
