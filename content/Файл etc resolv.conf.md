---
created: 2025-11-14
title: Файл etc resolv.conf
tags:
  - config-file
  - OS/Linux
  - network
aliases:
  - /etc/resolv.conf
---
> [!info] Перелік DNS-серверів для вирішення імен

> [!example] Формат
> ```
> nameserver 8.8.8.8
> nameserver 8.8.4.4
> search google.com gearxxed.com
> ```

> [!note] Дозволяє підстановку піддоменів: `ping docs` → `ping docs.gearxxed.com`