---
created: 2025-11-14
title: Шаблони рядкових збігів у awk
tags:
  - scripting
  - awk
aliases:
---
- `/regexpr/` (те саме, що `$0 ~`) — перевіряє збіг у рядках, які містять підрядок `regexpr`
- `expression ~ /regexpr/` — збіг, якщо рядок `expression` містить підрядок `regexpr`
- `expression !~ /regexpr/` — збіг, якщо рядок `expression` не містить підрядок `regexpr`

> [!note] Будь-який вираз, може використовуватися на місці `/regexpr/` у контексті `~`  та `!~`.