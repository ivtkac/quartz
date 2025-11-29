---
created: 2025-11-13
title: Як перевірити використання пам'яті процесами у Linux?
tags:
  - 🦮how-to
  - troubleshooting
  - OS/Linux
aliases:
  - How to check memory usage in Linux?
---
```bash
ps axo,rss,comm,pid | awk '{print "%0.fMB\t%s\t%s\n", $1/1024, $2, $3}' | sort -nr
```

Або

```bash
ps -eo pid,ppid,cmd,%mem,%cpu --sort=-%mem | head
```