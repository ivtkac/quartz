---
title: How to install proFTPD and create user?
created: 2025-12-04
tags:
  - 🦮how-to
  - ubuntu
  - ftp
aliases:
lang:
links:
  - "[[proFTPD]]"
  - "[[Ubuntu]]"
---
```bash
apt install proftpd
```

```bash
systemctl enable proftpd
```

```bash
useradd -m ftpuser -s /sbin/nologin
```

```bash
passwd ftpuser
```

```bash
chown -R ftpuser:ftpuser /home/ftpuser
```

Uncomment in config: `DefaultRoot ~`

```
vim /etc/proftpd/proftpd.conf
```
