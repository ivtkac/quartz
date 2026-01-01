---
title: API
created: 2026-01-01
tags:
  - architecture
  - design
  - programming
aliases:
lang:
---
> [!tldr]
> **API** (Application Programming Interface) defines how software components should interact.

A contract that defines:

- what requests can be made
- how  tot make them
- what responses to expect

Keys:

- [[Abstraction mechanism]]
- [[Service boundaries]]

## Key Design Principles

- consistency: consistent naming, consistent patterns
- simplicity: focus on core use cases, intuitive design
- security: authentication, authorization, input validation, rate limiting
- performance: caching strategies, pagination, minimize payloads, reduce round trips