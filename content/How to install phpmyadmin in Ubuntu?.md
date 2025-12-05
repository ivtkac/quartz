---
title: How to install phpmyadmin in Ubuntu?
created: 2025-12-05
tags:
aliases:
lang:
url: https://hostman.com/tutorials/how-to-install-phpmyadmin-on-ubuntu/
---
```
sudo apt install php8.3-fpm php8.3-mysql -y
```

```bash
cd /tmp
wget -c https://files.phpmyadmin.net/phpMyAdmin/5.2.1/phpMyAdmin-5.2.1-english.tar.gz
```

```
tar -xzvf phpMyAdmin-5.2.1-english.tar.gz
```

```
rm phpMyAdmin-5.2.1-english.tar.gz
```

```
sudo mv phpMyAdmin-5.2.1-english /usr/share/phpmyadmin
```

```
ln -s /usr/share/phpmyadmin /var/www/html
```

https://hostman.com/tutorials/how-to-install-phpmyadmin-on-ubuntu/