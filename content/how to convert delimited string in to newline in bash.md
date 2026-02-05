---
created: 2025-11-14
title: how to convert delimited string in to newline in bash
tags:
  - 🦮how-to
  - bash
aliases:
links:
  - "[[Bash]]"
---
> [!example] Конвертувати CSV в окремі рядки
> ```bash
> echo "$csv_string" | tr "," "\n"
> ```