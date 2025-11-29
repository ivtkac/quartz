---
created: 2025-11-13
title: HTTP
description: Передає гіпертекст
tags:
  - network
  - protocol
  - layer/application
aliases:
  - HyperText Transfer Protocol
default port: 80
---
> [!tldr]
> **HyperText Transfer Protocol (HTTP)** — це протокол передачі [[гіпертекст|гіпертексту]], який використовує механізм [[Методи запитів HTTP|запитів]] та [[Коди статусів HTTP|відповідей]] у [[клієнт-серверна архітектура|клієнт-серверній архітектурі]].

> [!warning] HTTP не передбачає захист та шифрування даних, тмоу чутливу інформацію (напр. паролі) через нього передавати не можна. (Див. [[HTTPS]], [[SSL]])

## Будова HTTP-повідомлень

```
start-line CRLF
*( field-line CRLF )
CRLF
[ message-body ]
```

HTTP запити:

```HTTP
<method> <request-target> <protocol>
```

HTTP відповіді:

```HTTP
<protocol> <status-code> <reason-phrase>
```