---
created: 2025-11-13
title: Як налаштувати Linux як роутер з NAT?
tags:
  - 🦮how-to
  - OS/Linux
  - network
  - nat
aliases:
  - How to setup Linux as Router with NAT?
---
1.  Дозволити переадрасацію IP:

```bash
sysctl -w net.ipv4.ip_forward
```

2. Налаштувати NAT:

```bash
iptables -t nat -A POSTROUTING -o <eth1> -j MASQUERADE
```

3. Дозволити трафік з eth1 до eth0:

```bash
iptables -A FORWARD -i <eth0> -o <eth1> -j ACCEPT 
```

4. Дозволити встановлені з'єднання з зовні

```bash
iptables -A FORWARD -i <eth1> -o <eth0> --ctstate RELATED,ESTABLISHED -j ACCEPT
```

5. Дропнути увесь інший трафік

```bash
iptables -A FORWARD -j DROP
```