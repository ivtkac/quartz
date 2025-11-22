---
created: 2025-11-21
title: Ansible roles
tags:
  - ansible
aliases:
---
> [!tldr]
> **Ролі (roles)** — це спосіб організації [[ansible tasks|завдань]] у повторно використовувані компоненти.

> [!note] Кожна роль має власну структуру директорій для завдань, змінних, обробників.

```yaml
- hosts: workstations
  tasks:
    - name: Include Powershell roll
      include_role:
          name: powershell
```