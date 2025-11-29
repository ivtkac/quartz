---
created: 2025-11-13
title: Як перевірити чи працює mysql на хості?
tags:
  - 🦮how-to
  - troubleshooting
  - mysql
aliases:
  - How to check if mysql is connected?
---
> [!example] Перевірити через сокет з'єднання
> ```bash
> ss -xap | grep mysql
> ```

> [!example] Перевірити з'єднання по мережі
> ```bash
> ss -na | grep 3306
> ```