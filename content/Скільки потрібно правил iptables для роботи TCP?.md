---
created: 2025-11-14
title: Скільки потрібно правил iptables для роботи TCP?
tags:
  - question
  - network
  - iptables
aliases:
links:
  - "[[TCP]]"
---
2 правила, а саме для:

- **NEW** - для SYN-запиту (1 правило)
- **ESTABLISHED** - для пітвердження з'єднання (відповідь SYN-ACK->ACK)