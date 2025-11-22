---
created: "2025-11-13"
title: "LIMIT"
tags:
aliases:
---
> [!info] **LIMIT** обмежує кількість рядків, які повертає запит.


```sql
SELECT columns FROM table_name LIMIT number;
SELECT columns FROM table_name LIMIT offset, number; -- MySQL
SELECT columns FROM table_name LIMIT number OFFSET offset; -- PostgreSQL
```

> [!question]- Коли використовувати?
> - Велика таблиця і не потрібні усі результати
> - [[Pagination|Пагінація]] для веб-додатків
> - Швидкий перегляд даних
> - Топ-N запити