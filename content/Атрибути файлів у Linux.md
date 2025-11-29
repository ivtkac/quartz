---
created: 2025-11-14
title: Атрибути файлів у Linux
tags:
  - OS/Linux
  - pam
aliases:
---
- **a** (append only) - тільки додвати 
- **i** (immutable) — незмінний (навіть для рута О_О)
- **A** (no atime) — не змінювати час доступу

> [!tip] Встановити атрибут: `chattr +a`, зняти: `chattr -i`, переглянути: `lsattr`