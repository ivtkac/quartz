---
title: Why it's better to store terraform state remotely?
created: 2025-11-30
tags:
  - terraform
  - question
aliases:
---
prev:: [[Чому краще зберігати відалено terraform state?]]

Для початку потрібно **мануально** (або за допомогою terraform :)  створити два ключових ресурси перед збереження віддалено конфігурацію:

1. 🗃️ [[AWS S3]] (для state storage )
	- *керування версіями* має бути ввімкнено (для відновлення стану)
	- *шифрування на стороні сервера* ([[SSE]]) має бути ввімкнено (наприклад, AES-256)
	- *публічний доступ* має бути **заблоковано**
2. 🔒 **Таблиця [[Dynamodb]]** (для state locking)
	- запобігає одночасному запуску `terraform apply` кількома користувачами
	- повинна мати **первинний ключ** з назвою `LockID` (тип String)

next:: [[How to store terraform remotely in AWS S3 bucket?|Як зберігати terraform state у S3?]]