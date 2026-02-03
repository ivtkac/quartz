---
title: Як зробити nginx на 80 порту віддає статику та проксує запити до Apache.
created: 2025-12-04
tags:
  - 🦮how-to
  - nginx
  - apache
  - proxy-server
aliases:
---
```bash
apt update apache2 nginx
```

- For nginx

```
server {
  listen 80;
  server_name example.com;

  location / {
    proxy_pass http://127.0.0.1:8080;
    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
  }

  location ~* \.(js|css|png|jpg|jpeg|gif|ico|svg)$ {
    root /var/www/html;
    expires max;
    access_log off;
  }
}
```

- For /etc/apache2/ports.conf change port to `8080`:

```bash
Listen 8080

<IfModule ssl_module>
	Listen 443
</IfModule>

<IfModule mod_gnutls.c>
	Listen 443
</IfModule>
```

- For /etc/apache2/sites-enabled/000-default.conf

```
<VirtualHost *:8080>
	ServerAdmin example.com 
	ServerAlias www.example.com
	DocumentRoot /var/www/html

	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

- enable site:  
```bash
a2ensite 000-default.conf
```

- restart services

```bash
systemctl reload apache2 nginx
```