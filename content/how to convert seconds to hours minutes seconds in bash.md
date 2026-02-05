---
created: 2025-11-14
title: how to convert seconds to hours minutes seconds in bash
tags:
  - 🦮how-to
  - bash
aliases:
links:
  - "[[date]]"
  - "[[Bash]]"
---
```bash
seconds=1000
date -d@"$seconds" -u +"%-H %-M %S"
```

Результат:

```
0 16 40
```