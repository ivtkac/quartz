---
created: 2025-11-14
title: Конфігураційний файл etc-group
tags:
  - config-file
  - OS/Linux
  - pam
aliases:
  - /etc/group
description: Групи користувачів
---
> [!info]  /etc/group
> Формат: `groupname:x:1000:user1,user2`

- `groupname`: ім'я групи
- `x`: історично зберігався пароль (тепер у `/etc/gshadow`)
- `1000`: GID групи
- `user1,user2`: учасники групи