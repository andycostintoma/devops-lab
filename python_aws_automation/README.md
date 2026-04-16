# Python AWS Automation

Python AWS Automation is a compact operations-scripting area here. Instead of one packaged application, it collects small scripts aimed at day-to-day cloud tasks, status checks, tagging, backups, recovery, and uptime monitoring.

## Script coverage

The current scripts focus on a few practical categories:

- `add-env-tags.py` for tagging EC2 instances across multiple regions
- `cleanup-snapshots.py` and `volume-backups.py` for storage lifecycle and backup work
- `restore-volume.py` for recovery-oriented operations
- `ec2-status-checks.py` and `eks-status-checks.py` for quick infrastructure visibility
- `monitor-website.py` for application uptime monitoring, email notification, Linode instance rebooting, and container restart logic over SSH

## Technical focus

The area uses direct scripting rather than a larger framework, which makes the operational intent easy to see:

- `boto3` for AWS interactions
- `requests` and `schedule` for simple monitoring loops
- `paramiko` for remote SSH actions
- `linode_api4` for provider-side recovery actions outside AWS

That mix is useful because it reflects the kind of glue code that often exists in real environments when a full internal platform is not in place yet.

## Runtime assumptions

Several scripts assume working cloud credentials or environment variables are already present. For example, `monitor-website.py` depends on values such as:

- `EMAIL_ADDRESS`
- `EMAIL_PASSWORD`
- `LINODE_TOKEN`

It also assumes SSH access to a target host and knowledge of the container or service being restarted.

## Why it matters

This area is valuable because operational engineering is often a mix of bigger platform tools and smaller targeted scripts. The Terraform, Kubernetes, and Jenkins folders cover the larger systems. Python AWS Automation covers the fast, practical end of the same work: checks, remediation, tagging, and keeping systems alive when something breaks.
