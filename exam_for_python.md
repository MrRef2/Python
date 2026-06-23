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
<img width="304" height="135" alt="image" src="https://github.com/user-attachments/assets/8e5f6b8f-5632-4c91-b3c0-9f5a5a23d342" />
<img width="291" height="86" alt="image" src="https://github.com/user-attachments/assets/df191838-3fb3-4381-a452-988c73ce93f8" />

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
<img width="281" height="130" alt="image" src="https://github.com/user-attachments/assets/abf0919d-3ee0-4e7d-b077-5b3b9b9f0402" />
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
<img width="499" height="130" alt="image" src="https://github.com/user-attachments/assets/cadd0b5e-faa2-418e-be19-3010713f0168" />
<img width="289" height="83" alt="image" src="https://github.com/user-attachments/assets/bb981b38-a2bd-4b32-bee4-5fd9ee76e227" />
неповторяющиеся
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
<img width="500" height="133" alt="image" src="https://github.com/user-attachments/assets/6ede2105-968e-4465-a804-9f30c19d9909" />
<img width="290" height="83" alt="image" src="https://github.com/user-attachments/assets/e35c257e-31d2-4ff3-bea3-9a6a5d175157" />
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
<img width="180" height="105" alt="image" src="https://github.com/user-attachments/assets/cee0a054-6f43-48f1-980f-f2a1ac643fa2" />
<img width="288" height="79" alt="image" src="https://github.com/user-attachments/assets/b5e55b79-d073-401c-bbcf-7e872398fdfb" />

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


