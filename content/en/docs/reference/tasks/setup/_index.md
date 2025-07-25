---
title: Setup
description: Manage installation
---

## Synopsis

```text
Usage:
  setup mini
  setup devcluster [--uninstall|--status|--skip-check-ports] 
  setup cluster [<context>] [--uninstall|--status]
  setup server <server> [<user>] [--uninstall|--status]
  setup status
  setup uninstall
  setup prereq
```

## Commands

```
  setup mini          deploy mini Apache OpenServerless, slim local installation available as http://devel.miniops.me 
  setup cluster       deploy Apache OpenServerless in the Kubernetes cluster using the <context>, default the current
  setup devcluster    deploy Apache OpenServerless in a devcluster created locally
                      you need Docker Desktop available with at least 6G of memory assigned
  setup server        create a Kubernetes in server <server> and deploy Apache OpenServerless
                      the server must be accessible with ssh using the <user> with sudo power, default root
  setup status        show the status of the last installation
  setup uninstall     uninstall the last installation
  setup prereq        validate current configuration
```

## Options

```
  --uninstall         execute an uninstall instead of an installation 
  --status            show the status instead of an installation 
  --skip-check-ports  ignore the check of already used ports
```

## Subtasks

- `kubernetes`: prepare kubernetes
- `nuvolaris`: install nuvolaris
- `docker`: prepare docker
