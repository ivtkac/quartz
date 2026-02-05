---
created: 2025-11-23
title: how to find out what process used port?
tags:
  - 🦮how-to
  - troubleshooting
  - OS/Linux
  - network
aliases:
links:
  - "[[ss]]"
  - "[[lsof]]"
---
```bash
sudo lsof -i :port
```

```bash
sudo ss -tulpn | grep :80
```