# GridSync Energy — Asset-Threat-Vulnerability Risk Assessment

Maintain a single consolidated register here. Component owners should propose
their rows, agree risk ratings and treatment with the team, then replace the
example below. Link each row to the relevant component mapping and evidence.

| Asset | Owner | Threat | Vulnerability | Risk Rating (L/M/H) | Treatment Strategy (Mitigate/Avoid/Transfer/Accept) | Proposed Mitigation | ISO/IEC 27001 Annex A | ISO/IEC 27017 |
|---|---|---|---|---|---|---|---|---|
| [EXAMPLE - REPLACE] GridSync web portal | Web tier owner | Unauthorised interception of portal traffic | Baseline serves the portal over HTTP without transport encryption | H | Mitigate | Terminate TLS at a controlled load balancer, redirect HTTP to HTTPS, and validate the deployed configuration | A.8.24 Use of cryptography; A.8.20 Network security | 12.4.1 (Cloud service monitoring); 13.1.1 (Network controls) |

Include both technical and organizational risks. For example, assess unauthorized
access alongside weak access approval/review processes, and assess human error
alongside awareness and training gaps. The linked [Statement of Applicability](statement-of-applicability.md)
records control applicability and implementation; it does not replace this risk
register.
