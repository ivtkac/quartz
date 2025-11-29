---
created: 2025-11-14
title: Основні налаштування Apache
tags:
  - config-file
  - apache
aliases:
  - /etc/httpd/conf/httpd.conf
---

```apache
# Where Apache lives
ServerRoot "/etc/httpd"

# What port to listen on
Listen 80

# Who runs Apache
User apache
Group apache

# Where your websites are
DocumentRoot "/var/www/html"

# Admin email (shows in error pages)
ServerAdmin you@example.com
```

> [!warning] After changing config: `sudo systemctl reload httpd`