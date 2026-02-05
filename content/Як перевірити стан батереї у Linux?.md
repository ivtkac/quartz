---
created: 2025-11-13
title: Як перевірити стан батереї у Linux?
tags:
  - 🦮how-to
  - OS/Linux
aliases:
  - How to check battery status in Linux?
links:
  - "[[upower]]"
---

```bash
upower -i "$(upower -e | grep 'BAT')"
```