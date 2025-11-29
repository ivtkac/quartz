---
created: 2025-11-13
title: Як переглянути привілеї у MySQL?
tags:
  - 🦮how-to
  - mysql
  - pam
aliases:
---
```sql
SHOW GRANTS FOR 'username'@'host';
```

```sql
+-----------------------------------------+
| Grants for username@host                |
+-----------------------------------------+
| GRANT USAGE ON *.* TO `username`@`host` |
+-----------------------------------------+
```