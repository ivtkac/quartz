---
created: 2025-11-13
title: Як запобігти OOM-killer?
tags:
  - 🦮how-to
  - troubleshooting
  - process
aliases:
---
- встановити ліміти по ресурсам для сервісів
- у [[MySQL]]: `innodb-buffer-pool-size`
- У [[Apache HTTP Server|Apache]]: `ServerLimit`, `ThreadLimit`, `MaxConnectionsPerChild`