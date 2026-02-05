---
created: 2025-11-22
title: Infrastructure as Code
tags:
  - iac
  - devops
aliases:
  - Infrastructure as Code
links:
  - "[[Що таке IAC?]]"
---
> [!question]- FAQ
> - [[Why do you need IaC?]]

> [!tldr]
> **IaC** is the way of defining computing and network infrastructure through source code.


> [!warning] AVOID MANUAL CONFIGURATION ALWAYS

- should be **Repeatable**, **Reliable**, **Consistent**
- ad hoc scripts ([[Bash]], [[Python]])
- configuration management tools ([[Ansible]], [[Chef]], [[Puppet]])
- server templating tools ([[Terraform]])
- orchestration tools ([[Kubernetes]])
- provisioning tools

- declarative: what you want? I want EC2, S3 bucket, load balancer
- imperative: what you want happen? Run scripts, cron schedulig, what state
