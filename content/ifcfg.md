---
created: 2025-11-14
title: ifcfg
tags:
  - config
  - OS/Linux
  - network
  - deprecated
aliases:
---
Конфігураційні файли знаходяться у каталозі `/etc/sysconfig/network-scripts` 

> [!example] Параметри
> 
> - `TYPE` - тип мережевого з'єднання
> - `DEVICE` - назва мережевого пристрою
> - `IPADDR` - IP-адреса
> - `PREFIX` - розмір мережі (або NETMASK)
> - `GATEWAY` - шлюз за замовчуванням
> - `DNS1` - перший DNS-сервер
> - `ONBOOT` - вмикати при старті системи
> - `DEFROUTE` - використовувати шлюз цього пристрою
> - `PEERDNS` - записувати DNS в /etc/resolv.conf