---
created: 2025-11-13
title: Конфігураційні файли systemd
description: /etc/systemd/system або ~/.config/systemd
tags:
  - systemd
  - config-file
aliases:
  - Конфігураційні файли systemd
---

| Каталог                                        | Опис                   | Пріоритет   |
| ---------------------------------------------- | ---------------------- | ----------- |
| `/etc/systemd/system` або `~/.config/systemd/` | Користувацькі юніти    | Найвищий    |
| `/usr/lib/systemd/system`                      | Встановлені з пакетами | Стандартний |
| `/run/systemd/system/`                         | Тимчасові юніти        |             |
