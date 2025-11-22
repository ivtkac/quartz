---
created: 2025-11-14
title: systemd.timer
tags:
  - systemd
  - scheduling
aliases:
---
> [!note] Альтернатива [[cron]].


| Параметр            | Опис                             |
| ------------------- | -------------------------------- |
| `OnCalendar`        | Дата (календарна)                |
| `OnBootSec`         | Через N секунд після завнтаження |
| `OnUnitActiveSec`   | Через N секунд після активації   |
| `OnUnitInactiveSec` | Через N секунд після деактивації |

> [!example] Наприклад
> ```ini
> [Unit]
> Description=Run backup daily
> 
> [Timer]
> OnCalendar=daily
> Persistent=true
> 
> [Install]
> WantedBy=timers.target
> ```
