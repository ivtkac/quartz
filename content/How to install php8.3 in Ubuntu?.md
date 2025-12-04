---
title: How to install php8.3 in Ubuntu?
created: 2025-12-04
tags:
  - ubuntu
  - php
  - 🦮how-to
aliases:
lang:
---
- Remove existed apache (if available)
```bash
  apt purge php8.5* -y >/dev/null
  apt autoremove -y >/dev/null
```

- Installed necessary packages:

```bash
  apt install software-properties-common ca-certificates lsb-release apt-transport-https -y
```

- Add repository:

```bash
add-apt-repository ppa:ondrej/php -y
```

- Install php

```
  apt install php8.3 php8.3-fpm libapache2-mod-php8.3 php8.3-cli php8.3-mysql php8.3-curl php8.3-gd php8.3-mbstring php8.3-xml php8.3-bz2 php8.3-zip php8.3-intl php8.3-soap php8.3-bcmath php8.3-imagick php8.3-ldap php8.3-imap php8.3-common php8.3-gmp php8.3-redis php-net-ldap2 php-net-ldap3 -y
```

- Restart php service

```bash
systemctl restart php8.3-fpm
```
