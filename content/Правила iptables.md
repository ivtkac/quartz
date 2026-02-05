---
created: 2025-11-14
title: Правила iptables
tags:
  - network
  - firewall
  - iptables
aliases:
links:
  - "[[iptables]]"
---
> [!tldr]
> **Правила** поєднують умови і дії для обробки пакетів.

```bash
iptables -A INPUT -s 192.168.1.0/24 -p tcp --dport 22 -j ACCEPT
#        ^ ланцюжок ^ умови               ^ протокол      ^ дія
```

> [!example] Targets
> - **ACCEPT** дозволити пакет
> - **DROP** відкинути пакет (не надсилає відповідь)
> - **REJECT** відкинути пакет з повідомленням (про помилку)
> - **LOG**  записати в журнал

> [!example] Порядок додавання
> - `-A` (append) - в кінець
> - `-I` (insert) - вставити на певну позицію
> - `-D` (delete) - видалити прави 