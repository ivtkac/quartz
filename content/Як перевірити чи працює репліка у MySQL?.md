---
created: 2025-11-13
title: Як перевірити чи працює репліка у MySQL?
tags:
  - 🦮how-to
  - troubleshooting
  - mysql
aliases:
  - How to check mysql replica status?
links:
  - "[[Реплікація]]"
  - "[[MySQL]]"
---
На репліці сервері:

```sql
SHOW SLAVE STATUS\G
-- або
SHOW REPLICA STATUS\G
```

> [!todo] Далі перевірити
> - `Replica_IO_Running`: "Yes"
> - `Replica_SQL_Running`: "Yes"
> - `Seconds_Behind_Master`: показує лаг-час (lag time)

> [!warning] Важливо
> Регулярний моніторинг роботи репліки дозволяє уникнути потенційних проблем у майбутньому.