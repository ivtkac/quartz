---
created: 2025-11-14
title: Row-based реплікація
tags:
  - database
  - replication
aliases:
links:
  - "[[Формати реплікацій]]"
---
- зберігає лише **точні змінни рядків**
- здатна опрацьовувати складні запити та тригери
- може займати великий розмір на диску


> [!example] Наприклад
> `Change row #534's value from 10 to 20`