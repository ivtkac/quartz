---
title: Passing variables in terraform
created: 2025-12-03
tags:
  - terraform
aliases:
lang: eng
---
## Define variables

``

## Passing variables

- [[змінні оточення|Environment variables]]: `TF_VAR_name_variable`
- or `-var=<VAR_NAME>=<VALUE>`, or `-var-file` options on the CLI (has the most priority)
- variable definition files (should be `.tfvars` or `.auto.tfvars`)