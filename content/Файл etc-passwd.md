---
created: 2025-11-14
title: Конфігураційний файл etc-passwd
tags:
  - config-file
  - OS/Linux
  - pam
aliases:
  - /etc/passwd
description: Облікові записи користувачів
---
> [!info] Формат: `username:x:1000:1000:User Name:/home/username:/bin/bash`

- `username`: ім'я користувача
- `x`: історично зберігався пароль (зараз хеши у `/etc/shadow`)
- `UID`: id користувача
- `GID`: id групи
- `User Name`: опис або повне ім'я користувача
- `/home/username`: [[Домашній каталог користувача]]
- `/bin/bash`: [[Оболонка]]