---
created: 2025-11-13
title: Apache architecture
tags:
  - apache
  - principle
aliases:
url: https://httpd.apache.org/docs/current/mod/quickreference.html
---
```
┌─────────────────────────┐
│   Apache Core Server    │  ← Handles basic requests
├─────────────────────────┤
│       Modules           │  ← Add features
│  - mod_ssl (HTTPS)      │
│  - mod_rewrite (URLs)   │
│  - mod_php (PHP code)   │
│  - mod_proxy (Reverse)  │
└─────────────────────────┘
```
