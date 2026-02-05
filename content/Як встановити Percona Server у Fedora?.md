---
created: 2025-11-13
title: Як встановити Percona Server у Fedora?
tags:
  - 🦮how-to
  - mysql
  - fedora
aliases:
  - How to install Percona Server in Fedora?
links:
  - "[[Fedora]]"
  - "[[Percona Server]]"
---
1. Встановити Percona repository:

```bash
sudo dnf install https://repo.percona.com/yum/percona-release-latest.noarch.rpm
```

2. Перевірити, чи  пакети є в наявності:

```bash
sudo percona-release setup ps80
sudo dnf list | grep percona | grep server
```

3. Встановити MySQL

```bash
sudo dnf install percona-server-server
```

4. Запустити MySQL

```bash
sudo systemctl start mysqld
```