---
created: 2025-11-14
title: Файл etc nsswitch.conf
tags:
  - config-file
  - network
  - OS/Linux
aliases:
  - /etc/nsswitch.conf
---
> [!info] Загальні налаштування вибору систем для резолву імен

- вибирає систему для резолву
- визначає порядок систем
- можна налаштувати для різних типів даних

> [!example] Системи резолву
> - `files` — брати з `/etc/hosts`
>- `dns` — використовувати dns-службу