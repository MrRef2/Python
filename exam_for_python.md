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
print('x y z w F')
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            for w in range(0, 2):
                F = (( x <= y ) or (y == w)) and ((x or z) == w)
                if F == 1:
                    print(x, y, z, w, F)
```
```
x y z w F
0 0 0 0 True
0 0 1 1 True
0 1 0 0 True
0 1 1 1 True
1 1 0 1 True
1 1 1 1 True
```
Ответ:zyxw

15124
<img width="403" height="108" alt="image" src="https://github.com/user-attachments/assets/48361c36-bce4-40bf-adc6-4d80b9e78f46" />
(x ≡ y ) ∨ ((y ∨ z) → x).
```
print ('x y z F')
for x in range (0, 2):
    for y in range (0, 2):
        for z in range (0, 2):
            F = (x==y)or((y or z) <= x)
            if not F == 1:
                print (x, y, z, F)
```
```
x y z F
0 1 0 False
0 1 1 False
```

Ответ:xzy

26974

(x ∨ y) ∧ ¬(y ≡ z) ∧ ¬w
