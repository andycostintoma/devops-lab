# Terraform Lab

Terraform Lab is the infrastructure-as-code branch here. It spans foundational AWS exercises, EKS provisioning, and IBM Cloud examples, which makes it useful both for learning Terraform syntax and for understanding how module-based infrastructure starts to grow across providers.

## Area structure

The work is grouped into three main projects:

- `terraform-basics/` for core AWS provisioning patterns such as VPC, subnet, and modular webserver setup
- `terraform-eks/` for AWS networking plus EKS-oriented infrastructure
- `terraform-ibm-cloud/` for IBM Cloud infrastructure with separate areas for VPC, Kubernetes cluster work, and registry-related provisioning

The subprojects already contain their own more command-oriented READMEs. The role of the area README is to explain how they fit together as one learning track.

## Technical focus

Across the area, the main themes are:

- provider configuration and authentication
- reusable modules
- environment-specific variables via tfvars files
- plan and apply workflow
- state inspection and targeted destroy operations
- cluster-oriented infrastructure rather than only single-resource examples
- cross-provider thinking between AWS and IBM Cloud

The presence of `.terraform.lock.hcl`, module folders, and multiple provider-specific trees makes the area feel more like real Terraform practice than a single one-file tutorial.

## Local workflow

Typical commands in the subprojects follow the standard Terraform loop:

```bash
terraform init
terraform plan
terraform apply -var-file terraform-dev.tfvars
terraform destroy
```

Some projects also use targeted inspection and debugging commands such as `terraform state list`, `terraform state show`, or `TF_LOG=TRACE`.

## Why it matters

Terraform Lab is where infrastructure work becomes versioned, reviewable, and repeatable. It connects especially well with the rest of the material here: Jenkins can orchestrate it, Kubernetes can run on top of it, and the DevSecOps notes give it the security and policy context it needs.
