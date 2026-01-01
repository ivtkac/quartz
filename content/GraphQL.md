---
title: GraphQL
created: 2026-01-01
tags:
  - api
aliases:
lang:
---
- query language
	- clients request exactly what they need
- single endpoint
	- one endpoint for all operations
- operations
	- query (read)
	- mutation (write)
	- subscription (real-time)
- minimal round trips
- used in complex UIs

> [!example]
> ```
> query {
> 	user(id: "123") {
>		name
>		posts { title, content } 	
>		followers { name }
> 	}
> }
> ```