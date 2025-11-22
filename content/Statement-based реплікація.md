---
created: 2025-11-14
title: Statement-based реплікація
tags:
  - database
  - replication
aliases:
---
- записує як **SQL запити**
- малі розміри логів, менше використання мережі
- певні обмеження у не-детермічних запитах

> [!example] Приклад зберігання
> ```sql
> UPDATE users SET status = 'active';
> ```