---
created: 2025-11-14
title: розгалуження у bash
tags:
  - scripting
  - bash
aliases:
  - if statements in bash
  - conditions in bash
---
- базовий if

```bash
if [ condition ]; then
  # код якщо умова істинна
fi
```

- if-else

```bash
if [ condition ]; then
  # якщо умова істина
else
  # якщо умова хибна
fi
```

- if-elif-else

```bash
if [ condition1 ]; then
  # якщо істина умова condition1
elif [ condition2 ]; then
  # якщо попердня умова хибна, а condition2 істина
else
  # якщо усі умови хибні
fi
```

- case-statemnt

```bash
case $variable in
	pattern1)
	   # відповідає умові pattern1
	   ;;
	pattern2|pattern3)
	  # відопвідає умові pattern2 або pattern3
	  ;;
	*)
	  # код за замовчуванням
	  ;;
esac
```
