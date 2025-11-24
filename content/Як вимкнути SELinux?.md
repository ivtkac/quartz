---
created: 2025-11-14
title: Як вимкнути SELinux?
tags:
  - 🦮how-to
  - selinux
aliases:
---
```bash
$ vi /etc/sysconfig/selinux
…
SELINUX=disabled
…
$ reboot
```