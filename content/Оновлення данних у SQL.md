---
created: 2025-11-14
title: Оновлення данних у SQL
tags:
  - sql
  - rules
aliases:
---
```sql
UPDATE table_name SET column1=value1, column2=value2 
WHERE some_column=some_value;
```

> [!warning] Якщо не вказати WHERE, то оновляться усі записи.
[[WHERE]]