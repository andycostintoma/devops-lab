# Kubernetes Lab

Kubernetes Lab is the cluster orchestration track here. It starts with raw YAML and core resource types, then moves through jobs, init containers, configmaps, secrets, ingress, storage, and finally a more realistic multi-service deployment.

## Track outline

The area is split into focused stages:

- `01-yaml-configuration-file-basics/` for first contact with deployments and services
- `02-jobs-and-init-containers/` for one-shot work, cron-style execution, and startup sequencing
- `03-configmap-and-secret-volumes/` for configuration injection and secret handling
- `04-demo-project-1/` for a Django plus PostgreSQL deployment
- `05-demo-project-2/` for a Mongo plus Mongo Express application with ingress
- `06-ingress-examples/` for routing and entry-point behavior
- `07-volumes-examples/` for persistent volumes, claims, and storage classes
- `online-boutique-k8s/` for the larger microservices deployment using manifests, Helm charts, and Helmfile

## Technical focus

This area covers the parts of Kubernetes that matter when moving from tutorials to actual platform reasoning:

- deployments and services
- jobs, cronjobs, and init containers
- configmaps and secrets
- ingress and traffic entry points
- persistent storage primitives
- Helm templating and Helmfile-driven orchestration
- multi-service application deployment

The `online-boutique-k8s/` section is especially useful because it steps beyond isolated examples and starts to resemble a real platform deployment surface.

## Local workflow

Most of the area uses the standard Kubernetes loop:

```bash
kubectl apply -f <manifest>
kubectl get all
kubectl describe <resource>
```

The boutique example adds Helm and Helmfile:

```bash
helm install <release> <chart>
helmfile sync
```

Each subdirectory is best treated as a separate lesson or deployment scenario rather than one monolithic cluster project.

## Why it matters

Kubernetes Lab is where container packaging turns into platform operations. It covers not just how to run an app in the cluster, but how configuration, secrets, scheduling, storage, ingress, and multi-service rollout all shape the behavior of that app after deployment.
