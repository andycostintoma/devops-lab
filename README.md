# DevOps Lab

DevOps Lab collects hands-on work across automation, containers, CI/CD, Kubernetes, cloud scripting, Terraform, and the security mindset that starts to turn raw DevOps practice into DevSecOps.

## Areas

- [`ansible`](ansible/README.md) for host automation, playbook structure, inventory management, and progressively richer configuration management examples
- [`devsecops_bootcamp`](devsecops_bootcamp/README.md) for security-oriented notes covering why DevSecOps matters, attack classes, OWASP, posture, monitoring, and compliance foundations
- [`docker`](docker/README.md) for container basics, Dockerfiles, Compose, persistence, networking, and Podman-oriented deployment work
- [`jenkins`](jenkins/README.md) for the CI/CD track from freestyle jobs to pipelines, shared libraries, AWS deployment, Terraform provisioning, and Python automation
- [`kubernetes`](kubernetes/README.md) for manifest basics, jobs, configmaps, secrets, ingress, volumes, and a larger microservices deployment example
- [`python_aws_automation`](python_aws_automation/README.md) for lightweight operational scripts against AWS, Linode, and application uptime checks
- [`terraform`](terraform/README.md) for infrastructure-as-code work spanning AWS basics, EKS provisioning, and IBM Cloud examples

## How to use this lab

The top-level README is the map. The area READMEs are the actual entry points.

- If the goal is configuration management and fleet automation, start with `ansible/`.
- If the goal is containers and local platform building blocks, start with `docker/`.
- If the goal is CI/CD and delivery workflows, start with `jenkins/`.
- If the goal is cluster orchestration, move into `kubernetes/`.
- If the goal is cloud provisioning, use `terraform/` alongside the AWS automation scripts.
- If the goal is adding security thinking to delivery pipelines, use `devsecops_bootcamp/` as the conceptual layer across the rest.

## Tooling mix

The lab deliberately spans multiple operational styles rather than one stack:

- YAML-heavy infrastructure and orchestration work in Ansible and Kubernetes
- Dockerfiles and Compose-based local environments
- Jenkinsfiles and CI/CD pipeline material
- Terraform modules and environment-specific variables
- Python scripts for day-to-day automation and health checks
- Markdown notes where the main value is architecture, security concepts, and operational reasoning

That mix makes the lab useful as both a command reference and a record of how platform work connects across automation, deployment, observability, and security.
