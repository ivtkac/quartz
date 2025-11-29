---
created: 2025-11-13
title: mysqld
tags:
  - demon
  - mysql
aliases:
---

```bash
systemctl start mysqld.service # or stop
```

## Опції

- `-?, --help` - довідка
- `-b, --basedir=[path]` - шлях до MySQL
- `-h, --datadir [homedir]` - шлях до БД
- `-P, --port=[port]` - порт з'єднання
- `--skip-grant-tables` - ігнорувати привілеї (по рукам можна получити за таке!)