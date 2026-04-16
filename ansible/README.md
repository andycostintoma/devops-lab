# Ansible Lab

Ansible Lab is the configuration-management track here. It starts with the basic mechanics of connecting to hosts and collecting facts, then grows into practical machine setup, service provisioning, templating, inventory design, and more advanced playbook patterns.

## What the area covers

The material is split into three layers:

- `playbooks/` for core operational tasks such as pinging hosts, printing facts, waiting for SSH, bootstrapping Python, managing known hosts, and deploying public keys
- `examples/` for more realistic service and system work including web servers, MariaDB, task control, Jinja templating, time sync, SELinux, repositories, users, cron, storage, and networking
- `advanced-examples/` for more dynamic automation patterns such as inventory work, rolling updates, lookups, filters, loops, and broader orchestration techniques

The area also includes `ansible.cfg`, inventory files, and templates so the examples are not just isolated YAML snippets but part of a runnable automation workflow.

## Why it matters

Ansible becomes valuable when automation stops being a single command and starts becoming repeatable system state. That is the role of this area. It moves from connectivity and bootstrapping into the kind of changes that platform work actually cares about: users, packages, services, security settings, scheduled jobs, and host-level configuration.

## Local workflow

Most of the work here is playbook-driven. Typical commands follow the normal Ansible loop:

```bash
ansible all -i inventory/inventory -m ping
ansible-playbook -i inventory/inventory playbooks/00-ping.yml
ansible-playbook -i inventory/inventory examples/01-webserver.yml
```

Exact host targeting and credentials depend on the machines defined in the inventory. The important part is not one single deployable project, but the progression from simple remote execution into richer configuration management patterns.
