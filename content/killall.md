---
created: 2025-11-14
title: killall
tags:
aliases:
description: Завершити процес за назво
---
> [!info] Завершити процес за назвою

```bash
killall [-wdivrg] [-u user] [-t term] [-SIG] [-s SIG] [name ...]
```

> [!example] Опції
> - `-i` - інтерактивно
> - `-r` - name як [[Регулярні вирази|regexp]]
> - `-u user` - тільки процеси заданого користувача
> - `-w` - чекати завершення
> - `-s SIG` - відправити сигнал