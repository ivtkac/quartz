---
created: 2025-11-14
title: Конфігураційний файл etc-sudoers
tags:
  - config-file
  - OS/Linux
  - pam
aliases:
  - /etc/sudoers
description: Повноваження користувачів
---
> [!info] /etc/sudoers
> Налаштування повноважень користувачів. ([[sudo]])

> [!warning] Редагувати тільки черезе `visudo`
 
```
user ALL=(ALL) ALL # повні права
user ALL=(ALL) /bin/ls, /bin/cat # тільки конкретні команди
%group ALL=(ALL) NOPASSWD: /sbin/mount # не треба пароля
```
