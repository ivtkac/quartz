---
created: 2025-11-13
title: Як переглянути користувача у MySQL?
tags:
  - 🦮how-to
  - mysql
  - pam
aliases:
---

```sql
SELECT User, Host FROM mysql.user;
```

> [!info] Або конкретний: `SELECT * FROM mysql.user WHERE Host='localhost' AND User='root'\G`
