---
created: 2025-11-14
title: exit status vs return
tags:
  - scripting
  - bash
aliases:
---
Якщо написати `return 1` у [[Функції у Bash|функції]], то функція завершиться з кодом `1`, 
але якщо ввести `exit 1`, то скрипт завершиться з кодом `1`.