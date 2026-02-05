---
created: 2025-11-13
title: Як мігрувати існуючі дані до репліки у MySQL
tags:
  - 🦮how-to
  - replication
  - mysql
aliases:
  - How to migrate existed data to replica in MySQL?
links:
  - "[[MySQL]]"
---
1. Підключитись до source ("мастера")
2. Експортувати базу даних: `sudo mysqldump -u root db > db.sql`
3. Скопіювати дамп до репліки-серверу
4. Створити базу даних та імпортувати дані: `sudo mysql db < db.sql

> [!note] Якщо немає данних для міграції:
> 1. Розблокувати таблиці:
>  ```sql
> UNLOCK TABLES;
>  ```
> 2. Створити таблицю:
> ```sql
> CREATE DATABASE db;
> ```
> 3. Вийти з MySQL: `exit`