---
created: 2025-11-13
title: LIKE
tags:
  - sql
aliases:
description: Значення за шаблоном
---
> [!info] **LIKE** дозволяє шукати текстові значення за шаблоном використовуючи спеціальні символи (wildcards).


```sql
SELECT columns FROM table_name
WHERE column LIKE 'pattern';
```

> [!example] **Спеціальні символи**
> - `%` — нуль або більше символів
> - `_` — рівно один символ