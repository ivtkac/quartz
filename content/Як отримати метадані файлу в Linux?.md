---
created: 2025-11-13
title: Як отримати метадані файлу в Linux?
tags:
  - 🦮how-to
  - filesystem
aliases:
links:
  - "[[stat]]"
---

```bash
$ stat file.txt
```

Результат:

```bash
  File: file.txt
  Size: 0         	Blocks: 0          IO Block: 4096   regular empty file
Device: fc00h/64512d	Inode: 101537091   Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/gxx_admin)   Gid: ( 1000/gxx_admin)
Context: unconfined_u:object_r:user_home_t:s0
Access: 2025-07-03 19:28:30.974991719 +0300
Modify: 2025-07-03 19:28:30.974991719 +0300
Change: 2025-07-03 19:28:30.974991719 +0300
 Birth: 2025-07-03 19:28:30.974991719 +0300
```