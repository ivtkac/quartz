---
created: 2025-11-14
title: Як увімкнути SELinux?
tags:
  - 🦮how-to
  - selinux
aliases:
links:
  - "[[SELinux]]"
---
```bash
$ vi /etc/sysconfig/selinux
…
SELINUX=permissive # або enforcing
…
$ reboot
```