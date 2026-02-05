---
created: 2025-11-13
title: Як зробити бекап конкретної таблиці у MySQL?
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
mysqldump -p -u root --databases VoipCompany --tables Customers > backup.sql
```