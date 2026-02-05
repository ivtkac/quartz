---
created: 2025-11-14
title: how to make port forwarding in iptables?
tags:
  - 🦮how-to
  - iptables
aliases:
links:
  - "[[iptables]]"
---
```bash
iptables -t nat -A PREROUTING -p tcp --dport 80 -j DNAT --to-destination 192.168.1.10:8080
```