---
created: 2025-11-13
title: Як змінити пароль користувачу у MySQL?
tags:
  - 🦮how-to
  - mysql
aliases:
---
```sql
ALTER USER 'username'@'host' IDENTIFIED BY 'password';
-- або
SET PASSWORD FOR 'username'@'host' = 'password';
```