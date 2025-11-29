---
created: 2025-11-13
title: Як підключитись до серверу mysql?
tags:
  - 🦮how-to
  - mysql
aliases:
  - How to connect to mysql server?
---
## З'єднання за замовчуванням

```bash
mysql -u root -p
```

## З'єднання по хосту

```bash
mysql -u root -h 127.0.0.1 -p
```

## З'єднання по сокету:

```bash
mysql -u root -S /var/lib/mysql/mysql.sock -p
```

## З'єднання по мережі:

```bash
mysql -u root -h 127.0.0.1 -P 3306 -p
```