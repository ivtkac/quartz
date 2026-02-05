---
created: 2025-11-13
title: Як зробити бекап з умовою у MySQL?
tags:
  - 🦮how-to
  - mysql
  - backups
aliases:
links:
  - "[[mysqldump]]"
  - "[[MySQL]]"
---
```bash
mysqldump -p -u root --databases VoipCompany --tables Customers --where="name='John'" > backup.sql
```