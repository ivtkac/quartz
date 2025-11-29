---
created: 2025-11-14
title: Як створити systemd unit
tags:
  - 🦮how-to
  - systemd
aliases:
---
1. Створити файл юніта

```bash
sudo nano /etc/systemd/system/myservice.serivce
```

2.  Базовий шаблон `.service` файлу

```ini
[Unit]
Description=My Custom Service
After=network.target

[Service]
Type=simple
User=myuser
Group=mygroup
WorkingDirectory=/path/to/working/directory
ExecStart=/path/to/executable
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target
```

3. Оновити systemd конфігурацію

```bash
sudo systemctl daemon-reload
```

4. Увімкнути та запустити

```bash
sudo systemctl enable --now myservice
```

> [!tip] Перевірка юніта
> - **Перевірити синтаксис**
> ```bash
> systemd-analyze verify /etc/systemd/system/myservice.service
> ```
> - **Переглянути статус**
> ```bash
> systemctl status myservice
> ```
> - **Переглянути логи**
> ```bash
> journalctl -u myservice -f
> ```