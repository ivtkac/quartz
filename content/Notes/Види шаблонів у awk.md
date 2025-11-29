---
created: 2025-11-14
title: Види шаблонів у awk
tags:
  - scripting
  - awk
aliases:
---
- `BEGIN { statements }` — виконується один раз перед читанням вводу
- `END { statements }` — виконується один раз після прочитання усіх рядків
- `expression { statements }` — виконується для кожного рядку, якщо `expression` є `True` (nonzero або nonnull)
- `/regular expression/ { statements }` — виконується для кожного рядку, що відповідає регялурному виразу
- `compound pattern { statements }` — кобмінація логічних операцій `&&` (AND), `||` (OR), `|` (NOT)  та дужок, виконується коли `True`
- `pattern1, pattern2 { statements }` — діапазон шаблонів, виконується для кожного рядку, який відповідає `pattern1` до наступного збігу з `pattern2` (включно)