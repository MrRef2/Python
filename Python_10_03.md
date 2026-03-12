# Решение задачи с вложенными циклами

## Тип 2 № 28677
Логическая функция F задаётся выражением:
`((x → y) ∨ (y ≡ w)) ∧ ((x ∨ z) ≡ w)`

```python
print("Тип 2 № 28677")
print("x y z w F")
for x in range(2):
    for y in range(2):
        for z in range(2):
            for w in range(2):
                F = ((x <= y) or (y == w)) and ((x or z) == w)
                if x == 1 and y == 0 and z == 0 and w == 1 and F == 1:
                    print(x, y, z, w, F)
                if x == 0 and z == 1 and w == 1:
                    print(x, y, z, w, F)
                if x == 1 and y == 1 and z == 0:
                    print(x, y, z, w, F)
print()
```

## Тип 2 № 18808
Логическая функция F задаётся выражением:
`(x ∧ ¬y) ∨ (y ≡ z) ∨ w`

```python
print("Тип 2 № 18808")
print("x y z w F")
for x in range(2):
    for y in range(2):
        for z in range(2):
            for w in range(2):
                F = (x and not y) or (y == z) or w
                if x == 1 and y == 0 and z == 1 and w == 0 and F == 0:
                    print(x, y, z, w, F)
                if x == 1 and y == 1 and z == 1 and w == 1 and F == 1:
                    print(x, y, z, w, F)
print()
```

## Тип 2 № 16805
Логическая функция F задаётся выражением:
`(¬x ≡ z) → (y ≡ (w ∨ x))`

```python
print("Тип 2 № 16805")
print("x y z w F")
for x in range(2):
    for y in range(2):
        for z in range(2):
            for w in range(2):
                F = ((not x) == z) <= (y == (w or x))
                if x == 0 and y == 0 and z == 0 and w == 0:
                    print(x, y, z, w, F)
print()
```

## Тип 8 № 3697
Все 5-буквенные слова, составленные из букв В, И, Н, Т, записаны в алфавитном порядке.  
Найти слово под номером 1019.

```python
print("Тип 8 № 3697")
letters = ["В", "И", "Н", "Т"]
count = 0
for a in letters:
    for b in letters:
        for c in letters:
            for d in letters:
                for e in letters:
                    count += 1
                    if count == 1019:
                        print(f"Слово под номером 1019: {a}{b}{c}{d}{e}")
print()
```

## Тип 8 № 56536
Определите количество чисел, для записи которых в восьмеричной системе счисления требуется ровно 12 цифр, ровно 3 из которых  — нечётные, и никакие две нечётные цифры не стоят рядом.

```python
from itertools import*
cnt1 = 0
cnt2 = 0
for i in product('НЧ', repeat = 12):
    p = ''.join(i)
    if p[0]=='Н' and p.count('Н')==3 and p.count('НН')==0:
        cnt1 += 1
    elif p[0]=='Ч' and p.count('Н')==3 and p.count('НН')==0:
        cnt2 += 1
print(4**12*cnt1 + 3*4**11*cnt2)
words.sort()

```

## Тип 8 № 25840
Вася составляет 4-буквенные слова из букв Б, Е, Л, К, А,  
причём буква Б используется ровно 1 раз. Сколько таких слов?

```python
print("Тип 8 № 25840")
letters = ["Е", "Л", "К", "А"]
count = 0
for pos_B in range(4):
    for a in letters:
        for b in letters:
            for c in letters:
                word = [a, b, c]
                word.insert(pos_B, "Б")
                count += 1
print(f"Количество слов: {count}")
```
