---
created: 2025-11-13
title: Директиви Apache
tags:
  - apache
aliases:
  - Apache Directives
doc: https://httpd.apache.org/docs/current/mod/quickreference.html
description: Інструкції для вебсервера
---
> [!tldr]
> **Директива Apache** — це інструкція в конфігураційних файлах [[Apache HTTP Server|вебсервера Apache]], яка вказує серверу, як саме поводитись.

## Основні директиви

- `ServerRoot "/etc/httpd"` — базовий шлях для відносних шляхів
- `Listen 80` — порт для прослуховування, також можна вказати IP: `Listen 1.2.3.4:80`
- `User apache`/`Group apache` — власник процесів обробки запитів
- `ServerAdmin bird@flock.org` — email для повідомлень про помилки
- `ServerName bird.paradise.com` — домене ім'я сервера
- `DocumentRoot "/var/www/html"` — директорія з веб-контентом
- `ErrorLog "logs/error_log"` — розташування журналу помилок
- `LogLevel "warn"` — рівень деталізації журналу ("error", "notice", "debug")
- `LogFormat` — формат для журнулювання

## LogFormat

**Apache** дозволяє вести журнал доступу до ресурсів сайту та помилок. У конфігураційному файлі `/etc/httpd/conf/httpd.conf` можна налаштувати, які дані про клієнта або ресурси потрібно заносити до журналу.

 > [!info] **Директива** `LogFormat "%v %h %t %T %b (%r - %>s)" myfmt`

- `%v` — сервер
- `%h` — адреса клієнта
- `%t` — коли завітав
- `%T` — витрачений час
- `%b` — розмір відповіді
- `%r` — [[Методи запитів HTTP|запит]]
- `%>s` — [[Коди статусів HTTP|фінальний статус]]
- `myfmt` — назва формату