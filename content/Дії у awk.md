---
created: 2025-11-14
title: Дії у awk
tags:
  - scripting
  - awk
aliases:
---
Діями можуть бути:

- вирази, з константами, зміннами, викликами функціями, тощо
- `print expression-list`
- `printf(format, expression-list)`
- `if (expression) statement`
- `if (expression) statement else statement`
- `while (expression) statement`
- `for (expression; expression; expression) statement`
- `for (variable in arary) statement`
- `do statement while (expression)`
- `break`, `continue`, `next`
- `exit`, `exit expression`
- `{ statements }`

> [!example] Особливості
> - виконується, якщо відповідає шаблону
> - може створювати  змінні, модифікувати їх

> [!note] Дужки у викликах функціях опціональні.