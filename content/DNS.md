---
created: 2025-11-13
title: DNS
description: Перетворює доменне ім'я у IP
tags:
  - network
  - protocol
  - layer/application
aliases:
  - Domain Name System
default port:
---

> [!question]- FAQ
> - [[Навіщо потрібен DNS?]]
> - [[DNS records]]

> [!tldr]
> **DNS** - розподілена система для перетворення доменних імен у [[IP]]-адреси.

DNS є ієрархічним за природою. Якщо локальний DNS не містить потрібних записів, він надсилає запит вище по рівню, поки не отримує позитивну відповідь.

> [!note] Для роботи DNS не потрібно [[FQDN]].

> [!example]
> `www.google.com`
> - `www`: сервіс
> - `google`: локальне доменне ім'я
> - `com`: top level доменне ім'я

![[dns.png|600x400]]

## Типи DNS серверів

- [[Локальний DNS]]
- [[Домен верхнього рівня]]
- [[Кореневий DNS]]
- [[авторитетний DNS]]
- [[Неавторитетний DNS]]