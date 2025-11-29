---
created: 2025-11-13
title: Конфігураційні файли systemd
description: /etc/systemd/system або ~/.config/systemd
tags:
  - systemd
  - config-file
aliases:
  - Конфігураційні файли systemd
---
[[systemd]] має такі файли для конфігурацій:

```
FILES
	/etc/systemd/system
		Root systemd units (high priority)
	
	~/.config/systemd/
		User systemd units (high priority)
		
	/usr/lib/systemd/system
		Installed by packages
		
	/run/systemd/system/
		Temporary units
```