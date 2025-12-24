---
title: "Apache doesn't load php"
created: "2025-12-24"
tags:
aliases:
lang:
---
```bash
$ sudo a2dismod mpm_event 
Module mpm_event disabled.
To activate the new configuration, you need to run:
  systemctl restart apache2
$ sudo a2enmod php8.3 
Considering dependency mpm_prefork for php8.3:
Considering conflict mpm_event for mpm_prefork:
Considering conflict mpm_worker for mpm_prefork:
Enabling module mpm_prefork.
Considering conflict php5 for php8.3:
Enabling module php8.3.
To activate the new configuration, you need to run:
$  sudo systemctl restart apache2
```
