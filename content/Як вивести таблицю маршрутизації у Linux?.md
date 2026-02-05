---
created: 2025-11-16
title: Як вивести таблицю маршрутизації у Linux?
tags:
  - 🦮how-to
  - OS/Linux
  - network
aliases:
links:
  - "[[ip command]]"
---
```bash
ip -c r # або ip route list
```

or

```bash
route -n
```

or

```bash
netstat -r -n
```