# Представленные задания для подготовки к экзамену ⏰
Тип 2 (все номера):
28677
15124
26974
15618
15970
18614
55589
48423
15787
85678
18578
81786
17320
48450
40718
73828
45236
33504
64932
64887
72587

Тип 8 (все номера):
3697
78064
55625
7667
17328
27539
18491
37143
59745
10473
60250
64938
9796
27009
15822
28546
15795
3700
3237
13486
59741

Для понимания выполнения заданий типа 2 нужно просто перевести форму из алгебра-логики на язык Python
для понимани как это делать возьмём за пример вырожение `((x → y) ∨ (y ≡ w)) ∧ ((x ∨ z) ≡ w)` из номера 28677.
<img width="884" height="408" alt="image" src="https://github.com/user-attachments/assets/5f73aea7-bdfe-4d08-a013-798c6c461443" />
в итоге мы получим: `(( x <= y ) or (y == w)) and ((x or z) == w)`
### Решения задач: (Тип 2)
28677
<img width="319" height="120" alt="image" src="https://github.com/user-attachments/assets/a00602e4-732d-4361-86d5-0f23b2843408" />
((x → y) ∨ (y ≡ w)) ∧ ((x ∨ z) ≡ w)
```
print('x y z w')
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            for w in range(0, 2):
                if (( x <= y ) or (y == w)) and ((x or z) == w):
                    print(x, y, z, w)
```
```
x y z w
0 0 0 0
0 0 1 1
0 1 0 0
0 1 1 1
1 1 0 1
1 1 1 1
```
Ответ:zyxw

15124
<img width="403" height="108" alt="image" src="https://github.com/user-attachments/assets/48361c36-bce4-40bf-adc6-4d80b9e78f46" />
(x ≡ y ) ∨ ((y ∨ z) → x).
```
print("x y z")
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            if not((x == y) or ((y or z) <= x)):
                print(x, y, z)
```
```
x y z
0 1 0
0 1 1
```

Ответ:xzy

26974

(x ∨ y) ∧ ¬(y ≡ z) ∧ ¬w
```
print ('x y z w')
for x in range(0,2):
     for y in range(0,2):
        for z in range(0,2):
            for w in range(0,2):
                if (x or y) and not(y==z) and not w:
                    print (x, y, z, w)
```
```
x y z w
0 1 0 0
1 0 1 0
1 1 0 0
```
Ответ:xyzw

15618

(x ∧ ¬y) ∨ (y ≡ z) ∨ ¬w
```
print('x y z w')
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            for w in range(0, 2):
                if not ((x and not (y)) or (y==z) or not (w)):
                    print(x,y,z,w)
```
```
x y z w
0 0 1 1
0 1 0 1
1 1 0 1
```
Ответ:wzyx

15970

(x ∧ ¬y) ∨ (y ≡ z ) ∨ w
```
print('x y z w')
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            for w in range(0, 2):
                if not ((x and not (y)) or (y==z) or w):
                    print(x,y,z,w)
```
```
x y z w
0 0 1 0
0 1 0 0
1 1 0 0
```
Ответ:yxwz


18614

((w → ¬x) ≡ (z → y)) ∧ (y ∨ w)

```
print("x y z w")
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            for w in range(0, 2):
                if ((w <= (not x)) == (z <= y)) and (y or w):
                    print(x, y, z, w)
```
```
x y z w
0 0 0 1
0 1 0 0
0 1 0 1
0 1 1 0
0 1 1 1
1 0 1 1
1 1 0 0
1 1 1 0
```
Ответ:xwyz

55589

F1  =  (x → y)≡(w ∨ ¬ z),
F2  =  (x → y)∧(¬w≡z).

```
print("x y z w f1 f2")
for x in range(2):
    for y in range(2):
        for z in range(2):
            for w in range(2):
                f1 = ((x <= y) == (w or not z))
                f2 = ((x <= y) and (not w == z))
                print(x, y, z, w, " ", int(f1), " ", int(f2))
```
```
x y z w   f1 f2
0 0 0 0   1   0
0 0 0 1   1   1
0 0 1 0   0   1
0 0 1 1   1   0
0 1 0 0   1   0
0 1 0 1   1   1
0 1 1 0   0   1
0 1 1 1   1   0
1 0 0 0   0   0
1 0 0 1   0   0
1 0 1 0   1   0
1 0 1 1   0   0
1 1 0 0   1   0
1 1 0 1   1   1
1 1 1 0   0   1
1 1 1 1   1   0
```

Ответ:xzyw


### Решения задач: (Тип 8)

3697
Все 5-⁠буквенные слова, составленные из букв В, И, Н, Т, записаны в алфавитном порядке и пронумерованы. Вот начало списка:
1.  ВВВВВ
2.  ВВВВИ
3.  ВВВВН
4.  ВВВВТ
5.  ВВВИВ
...
Запишите слово, которое стоит под номером 1019.
```
k = 0
for b1 in "ВИНТ":
    for b2 in "ВИНТ":
        for b3 in "ВИНТ":
            for b4 in "ВИНТ":
                for b5 in "ВИНТ":
                    k += 1
                    if k == 1019:
                        print(b1, b2, b3, b4, b5)
```
Ответ: T T T H H


