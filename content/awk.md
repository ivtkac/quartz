---
created: 2025-11-13
title: awk
description: Programming language for text processing
tags:
  - man
  - OS/Linux
  - text-processing
aliases:
doc: https://www.gnu.org/s/gawk/manual/gawk.html
links:
  - "[[man]]"
---
> [!question]- FAQ
> - [[Структура програми awk]]
> - [[Вбудованні змінні у awk]]
> - [[Дії у awk]]
> - [[Шаблони awk]]

> [!info] `awk` — повноцінна [[мова програмування]] та інструмент [[cli|командного рядка]] для обробки та фільтрації структурованого тексту.

```bash
awk 'program' input files # код як рядок
awk -f profile input files # код як файл
some_command | awk 'program' # код як рядок
```

> [!note] 
> Також можна використовувати [[шебанг]] для [[Скрипти|скриптів]]:
> ```awk
> #!/usr/bin/env awk -f
> BEGIN { print "Hello, world!" }
> ```