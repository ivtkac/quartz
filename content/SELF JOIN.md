---
created: 2025-11-13
title: SELF JOIN
tags:
  - sql
aliases:
description: Об'єднання таблиці з самою себе
---
> [!info] **SELF JOIN** це [[Об'єднання таблиць у SQL|об'єднання таблиці]] самої з собою.

```sql
SELECT columns FROM table_name a
JOIN table_name b
ON condition;
```

> [!note] `a` та `b` — аліаси одніє і тієї ж таблиці `table_name`. ([[Перейменування назв у SQL]])