---
title: ніколи не використовуй git commit -m,  використовуй git commit -v
created: 2025-12-10
tags:
  - git
  - tips
aliases:
  - never use git commit -m, use git commit -v
links:
  - "[[Git]]"
---
> [!warning] 
> `git commit` відкриває редактор з зі змінними `$EDITOR` або з конфігурації гіта.

За допомогою `git commit -v` можна бачити різницю комітів ([[git diff]]) під час написання повідомлення коміту.

> [!question] Нащо?
> Щоб швидко перервірити правильність коміту та що саме змінено.
