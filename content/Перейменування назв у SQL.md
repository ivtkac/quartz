---
created: 2025-11-14
title: Перейменування назв у SQL
tags:
  - sql
  - rules
aliases:
---

- Явне використання AS

```sql
SELECT first_name AS "Ім'я"
FROM users;
```

-  Неявне використання (без AS)

```sql
SELECT first_name "Ім'я"
FROM users;
```

> [!note] Щоб перейменувати колонку на ім'я, що містить пробіли потрібно використовувати лапки (\` \`, ' ', " ")