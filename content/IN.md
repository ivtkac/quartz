---
created: 2025-11-13
title: IN
tags:
  - sql
aliases:
description: Значення у списку
---
> [!info] **IN** дозволяє перевірити, чи міститься значення в списку можливих значень.

> [!note] Використовується як альтернатива багатьом OR умовам.

```sql
SELECT columns FROM table_name WHERE column IN (value1, value2, ...);
SELECT columns FROM table_name WHERE column IN (SELECT ...);
```