---
created: 2025-11-14
title: Цикли у Bash
tags:
  - scripting
  - bash
aliases:
---
- `for` — ітерація по списку

```bash
for file in *.txt; do
	echo $file
done
```

- `while` — виконання поки умова істина

```bash
while read line; do
	echo $line
done
```

- `until` — виконання поки умова хибна

```bash
counter=0
until [ $counter -qe 5 ]; do
	echo $counter
	((counter++))
done
```

- `select` — меню вибору

```bash
select option in "Hello" "Start" "Quit"; do
	case $option in
		"Hello") echo "Hello Bash" ;;
		"Start") echo "Starting script..." ;;
		"Quit") break ;;
		*) echo "Invalid option" ;;
	esac
done
```
