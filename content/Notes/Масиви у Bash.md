---
created: 2025-11-15
title: Масиви у Bash
tags:
  - scripting
  - bash
aliases:
---
**Масиви** у [[Bash]] дозволяють зберігати кілька значень в одній змінній.

## Типи масивів

- індексні масиви (з числовими індексами)

```bash
numbers=(1 2 3 4 5)
```

- асоціативні масиви ("ключ-значення")

```bash
declare -A data
data["username"] = "gearxxed"
data["age"] = "23"
data["city"] = "Chernivtsi"
```

## Доступ до елементів

- по індексу/ключу:

```bash
echo ${numbers[0]}
echo ${data["username"]}
```

- усі елементи

```bash
echo ${numbers[@]}
echo ${numbers[*]}
```

- вивести тільки індекси (для асоціативних виведе ключі)

```bash
echo ${!numbers[@]}
echo ${!data[@]}
```

- вивести к-сть елементів

```bash
echo ${#numbers[@]}
```

## Операції з масивами

- додати елемент

```bash
numbers+=(10)
```

- видалити елемент

```bash
unset numbers[1]
# видалити увесь масив
unset numbers
```

- отримати зріз масиву

```bash
# починаючи з 1, 2 елементи
echo ${numbers[@]:1:2}
```

- замінити у масиві

```bash
echo ${numbers[@]/2/8}
```

## Ітерація по масивах

- По значеннях

```bash
for fruit in "${fruits[@]}"; do
	echo $fruit
done
```

- По індексах

```bash
for i in "${!fruits[@]}"; do
	echo "$i — ${fruits[i]}"
done
```

- По ключам (асоціативний масив)

```bash
for key in "${!person[@]}"; do
	echo "$key: ${person["key"]}"
done
```
