---
created: 2025-11-14
title: how to split string by delimiter in bash
tags:
  - 🦮how-to
  - bash
aliases:
---

```bash
for item in ${string//,/}; do
	echo "$item"
done
```

Або

```bash
IFS=',' read -ra ARRAY <<< "$string"
for item in "${ARRAY[@]}"; do
	echo "$item"
done
```