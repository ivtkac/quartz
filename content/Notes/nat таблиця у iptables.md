---
created: 2025-11-14
title: nat таблиця у iptables
tags:
  - iptables
aliases:
---
- Реалізує [[NAT]]
- Змінює адреси джерела/призначення та порти
- Впливає на маршрутизацію і зворотній трафік


> [!example] Ланцюжки
> - **PREROUTING** - DNAT (зміна адреси призначення)
> - **POSTROUTING** - SNAT (зміна адреси джерела)
> - **OUTPUT** - для локально генерованого трафіку

> [!example] Типи NAT
> - **SNAT** - Source NAT (зміна адреси відправника)
> - **DNAT** - Destination NAT (зміна адреси призначення)
> - **MASQUERADE** - динамічний SNAT для змінних IP
