---
title: How to install phppgadmin in Ubuntu?
created: 2025-12-05
tags:
  - 🦮how-to
  - ubuntu
  - phppgadmin
aliases:
lang:
---
```bash
apt install php8.3-pgsql
```

```bash
cd /tmp

wget https://github.com/phppgadmin/phppgadmin/releases/download/REL_7-13-0/phpPgAdmin-7.13.0.tar.gz 
```

```bash
tar -xzvf phpPgAdmin-7.13.0.tar.gz 
```

```bash
mv phpPgAdmin-7.13.0 /usr/share/phppgadmin
ln -s /usr/share/phppgadmin/ /var/www/html
```