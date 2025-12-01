---
title: Об'єднання таблиць у SQL
created: 2025-12-01
tags:
  - sql
  - rules
aliases:
---
**JOIN** операція дозволяє об'єднувати дані з двох або більше [[Таблиця|таблиць]] на основі зв'язків між ними.

```sql
SELEECT a.cols, B.cols FROM A
JOIN B ON A.col = B.col;
```