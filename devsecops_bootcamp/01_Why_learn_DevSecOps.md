# 01 – Why Learn DevSecOps

## Why DevSecOps Matters
- Security breaches cost trillions; DevOps pipelines rarely embed security, so DevSecOps engineers are scarce and in high demand.
- DevSecOps integrates automated security checks across the SDLC, making practitioners stand out even among seasoned DevOps/cloud engineers.

## Prerequisites
- Solid DevOps stack: CI/CD tooling (Jenkins, GitLab CI, GitHub Actions), Docker, Terraform, Kubernetes, Linux, AWS, Python automation.
- Helpful extras: GitLab CI course, DevOps bootcamp background, basic software development lifecycle knowledge (IT beginners course).

## Chapter 1 – Security Essentials
- Covers core security concepts, OWASP Top 10, common attack types (SQLi, XSS, SSRF, etc.).
- Goal: understand *what* tooling protects before learning *how* to automate it.

## Chapter 2 – DevSecOps Concepts
- Why DevSecOps emerged, scanning types (secret scanning, SAST, SCA, DAST) and tooling categories.
- Clarifies role boundaries and responsibilities between DevSecOps and other engineering teams.

## Application Security Automation
- Start with an intentionally insecure CI pipeline, then layer: secret scanning, SAST, SCA (with CVE awareness), report generation, DefectDojo ingestion, false-positive management.
- Automate report uploads (Python) and fix sample issues (SQL injection, vulnerable libraries) to understand remediation.
- Extend into CD: secure deployments, container image scanning (incl. AWS ECR), remediate image-level findings.

## Infrastructure & Cloud Security
- Focus on AWS while teaching cloud-agnostic concepts: IAM least privilege, short-lived access (no SSH keys), secure networking.
- DAST against running workloads; secure infra with Terraform + GitOps pipeline that includes security scans.
- Logging/monitoring via CloudTrail, CloudWatch, AWS Budgets for anomaly + cost alerts.

## Kubernetes Platform Security (Part 2 Preview)
- EKS security: IAM + Kubernetes RBAC integration, secure image pulls, pod hardening, network policies, service mesh.
- Secrets management with Vault; scan manifests for misconfigurations; policy-as-code enforcement inside CI/CD.

## Compliance as Code
- Automate compliance checks (e.g., CIS benchmarks) across application, infrastructure, and Kubernetes layers.

## Adoption & Culture
- DevSecOps is also organizational change: strategies for incremental adoption, demonstrating wins, and gaining buy-in.

## Learning Experience
- Full repos, handouts, dedicated DevSecOps support team across time zones, verifiable certificate/digital badge.
- Emphasis on “concepts before tools,” enabling easy transfer of skills to any CI/CD platform or tech stack.
