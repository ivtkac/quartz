---
created: 2025-11-13
title: Як вказати яку БД реплікувати у mysql
tags:
  - 🦮how-to
  - mysql
  - replication
aliases:
  - How to setup MySQL to replicate specific database?
---
> [!note]- Змінні
> - **replicate-do-db**: перелік БД, які потрібно реплікувати (якщо цієї змінни не існує, то реплікує усі бази дани)
> - **replicate-ignore-db**: перелік, які ігнорується для реплікації
> - **replicate-wild-do-table**: дозволяє динамічно визначати

> [!example] Конфігурація у `/etc/my.cnf`
> ```ini
> replicate-do-db=sales
> replicate-ignore-db=categories
> replicate-wild-do-table=user%.%
> ```