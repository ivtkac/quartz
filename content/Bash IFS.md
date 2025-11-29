---
created: 2025-11-29
title: Bash IFS
tags:
  - scripting
  - bash
aliases:
  - IFS
description: Розділювач полів
---
> [!tldr]
> **IFS (Internal Fields Separator)** — [[Змінні у Bash|змінна]], яка визначає символи для розділення полів.

> [!note] За замовчуванням: `^I$` (пробіл, табуляція, новий рядок)

> [!example] Приклад використання
> ```bash
> while IFS=":" read -r username hash uid gid gecos home shell; do
>   echo "$username: $home, ($shell)"
>  done < /etc/passwd
> ```