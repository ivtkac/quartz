---
created: 2025-11-13
title: WHERE
tags:
  - sql
aliases:
description: Фільтрація за критерієм
---
> [!tldr]
> **WHERE** — це команда, яка дозволяє фільтрувати рядки таблиці за певним критерієм (або критеріями).

> [!warning] **WHERE** не працює з агрегатними функціями.

```sql
SELECT columns
FROM table_name
WHERE condition;
```