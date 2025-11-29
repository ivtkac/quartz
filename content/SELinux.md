---
created: 2025-11-13
title: SELinux
tags:
  - OS/Linux
  - selinux
aliases:
---
> [!tldr]
> **SELinux (Security Enhanced Linux)** — це система контролю, яка реалізує [[Mandatory Access Control]] на основі [[Discretionary Access Control]].

SELinux може бути лише у одному з можливих трьох режимів:

- **Enforcing** (Примусовий)
- **Permissive** (Дозвіл)
- **Disabled** (вимкнутий)

> [!note]
> У режимі **Enforcing** SELinux примусово прйиматиме політику і недозволятиме будь-які неавторизований доступ для користувачів і процесів. Ця політика не застосовується до **логування**.