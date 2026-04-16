# Jenkins Lab

Jenkins Lab is the CI/CD backbone of `devops-lab`. It follows a clear progression from getting Jenkins running, to building jobs, to moving delivery logic into versioned pipelines, and then into shared libraries, cloud deployment, infrastructure provisioning, and Python-assisted automation.

## Track outline

The area is organized as an incremental path:

- `00-initial-setup/` for the first Jenkins setup steps
- `01-demo-freestyle-job/` for the classic job model before pipelines take over
- `02-pipeline-job-and-jenkinsfile-basics/` and `03-complete-pipeline-job/` for the move into scripted delivery
- `04-multibranch-pipeline/` for branch-aware CI/CD
- `05-use-shared-library/` for extracting reusable pipeline logic
- `06-increment-version/` for version bumping and release-oriented workflow
- `07-deploy-to-aws-ec2/` and `08-deploy-to-eks-cluster/` for cloud deployment paths
- `09-terraform-provisioning/` for connecting Jenkins to infrastructure provisioning
- `10-jenkins-python/` for Python-driven automation around Jenkins tasks

## Why the area matters

The important thing about this track is that it treats Jenkins as more than a UI for running shell commands. The material gradually turns Jenkins into a delivery control plane:

- jobs become versioned pipeline definitions
- deployment logic moves closer to source control
- shared libraries reduce duplication
- cloud targets make infrastructure and application delivery intersect
- Terraform and Python automation pull Jenkins into broader platform workflows

That makes the area useful both for basic Jenkins practice and for understanding how CI/CD pipelines start to coordinate real infrastructure change.

## Project signals

The area includes a mix of:

- `Jenkinsfile`-based examples
- Dockerfiles and compose setups
- Maven projects used as pipeline targets
- shell scripts for deployment steps
- embedded Terraform under `09-terraform-provisioning/`
- Python automation under `10-jenkins-python/`

## Local workflow

There is no single command for the whole area. Each numbered stage is its own working unit.

- use the earlier stages to get Jenkins and basic jobs running
- use the pipeline stages to iterate on `Jenkinsfile` structure
- use the deployment stages when validating AWS, Kubernetes, and Terraform integration

Taken together, the area captures the shift from basic CI to platform-aware CD.
