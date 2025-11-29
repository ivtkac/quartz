---
created: 2025-11-13
title: Як створити користувача у MySQL?
tags:
  - 🦮how-to
  - pam
  - mysql
aliases:
---

```sql
CREATE USER 'name_user'@'host' IDENTIFIED BY 'password';
```

> [!tip]
> За допомогою символа `%` можна гнучко вказувати хости. 
 
> [!example] Наприклад
> - `192.168.0.%` — будь-яка адреса в підмережі
> - `%.mydomain.com` — будь-який піддомен
> - `%` — з будь-якого місця
