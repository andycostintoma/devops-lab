# DevSecOps Bootcamp Notes

DevSecOps Bootcamp Notes is the security layer here. It is still in a notes-first stage rather than a tooling-heavy implementation stage, but the material already frames the mindset needed to connect CI/CD, infrastructure, cloud platforms, and security controls into one delivery story.

## Current coverage

The notes currently focus on two core chapters:

- `01_Why_learn_DevSecOps.md` for motivation, role definition, learning path, and the broader shape of secure delivery work
- `02_Security_Essentials.md` for attack classes, OWASP risks, defense in depth, posture, logging, monitoring, and compliance foundations

Those notes already outline the direction for later practical work: secret scanning, SAST, SCA, DAST, secure container delivery, Terraform and cloud security, Kubernetes platform hardening, and compliance as code.

## Why it matters

This area is important because DevOps tooling without security context quickly turns into automation that ships problems faster. The notes here focus on the `why` behind the tooling:

- what kinds of failures security controls are meant to catch
- why least privilege matters for pipelines and platforms
- how OWASP and common attack classes map back to delivery workflows
- why logging, monitoring, and evidence collection are part of engineering work rather than only security work

## How to use it

The best way to read this area is as a conceptual overlay for the rest of the material here.

- Read it alongside `jenkins/` to think about secure CI/CD.
- Read it alongside `terraform/` and `kubernetes/` to connect provisioning and platform decisions with posture and policy.
- Read it alongside `python_aws_automation/` to keep least privilege, monitoring, and remediation in view.

Even in note form, it gives the rest of the material here a clearer security frame.
