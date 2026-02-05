---
created: 2025-11-13
title: Як встановити пароль для аутентифікації у Apache?
tags:
  - 🦮how-to
  - apache
aliases:
  - How to set up password authentication in Apache?
links:
  - "[[htpasswd]]"
---
```bash
htpassswd -cb /etc/httpd/.htpasswd "$HTTPD_USER" "$HTTPD_PASSS"
```

у httpd.conf:

```yaml
AuthType Basic
AuthName "Resitrcted Content"
AuthUserFile "/etc/httpd/.htpasswd"
Require valid-user
```