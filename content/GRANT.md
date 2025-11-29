---
created: 2025-11-13
title: GRANT
tags:
  - sql
  - mysql
aliases:
description: Надати права
---
> [!info] [MySQL] **GRANT** дозволяє призначити привілеї.

```sql
GRANT тип_привілею [(перелік стовчиків)] [, тип_привілею [(перелік стовпчиків)]...] ON {ім'я_таблиці} |*|*.*|ім'я_бази_даних.* TO ім'я_користувача [IDENTIFIED BY 'password'] [, ім'я_користувача [IDENTIFIED BY 'password']...] [WITH GRANT OPTION]
```