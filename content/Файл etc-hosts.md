---
created: 2025-11-14
title: Файл etc-hosts
tags:
  - config-file
  - OS/Linux
  - network
aliases:
  - /etc/hosts
---

> [!info] /etc/hosts
> Локальні налаштування доменних імен, локальний DNS

> [!example] Формат
> `192.168.5.5 domain1.com domain2.ua`

> [!question] Як працює?
> При зверненні до domain1.com або domain2.ua, трафік направляється на IP 192.168.5.5.

> [!tip] Можна встановити приорітет над [[DNS]] (у [[Файл etc nsswitch.conf|/etc/nsswitch.conf]])