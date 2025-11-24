---
created: 2025-11-13
title: Як вивести тільки каталоги у Linux?
tags:
  - 🦮how-to
  - filesystem
  - OS/Linux
aliases:
---
```bash
$ ls -ld */
```

Результат:

```bash
drwxr-xr-x. 2 gxx_admin gxx_admin 6 Jul  3 22:54 test/
```

Або за допомогою команди `find`:

```bash
$ find -type d
```

Результат: 

```
.
./.cache
./.cache/starship
./.cache/helix
./.config
./.config/fish
./.config/fish/completions
./.config/fish/conf.d
./.config/fish/functions
./.config/helix
./.local
./.local/share
./.local/share/fish
./.local/share/fish/generated_completions
./.local/share/zoxide
./.local/bin
./.ssh
./test
```