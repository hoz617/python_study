# 260114_python_study
+=, -=,*= 누적계산

```python
a = ["I", "study", "python", "language", "!"]
for i in range(2,len(a)):
    print(a[i])
```

```python
hab = 0
for i in range(1,11):
    hab += i
print("합 :",hab)
```

```python
price_list = [32100, 32150, 32000, 32500]
for i in range(len(price_list)):
    print((len(price_list)-1)-i,price_list[i])
```

```python
my_list = ["가", "나", "다", "라"]
for i in range(len(my_list)-1):
    print(my_list[i],my_list[i+1])
```

```python
my_list = [100, 200, 400, 800]
for i in range(len(my_list)-1):
    print(my_list[i+1] - my_list[i])
```

```python
my_list = [100, 200, 400, 800, 1000, 1300]
for i in range(len(my_list)-2):
    print((my_list[i] + my_list[i+1] +my_list[i+2])/3)
```

이차원 리스트, 리스트안의 리스트로
```python
apart = [ [101, 102], [201, 202], [301, 302] ]

for i in apart: #여기서는 결과가 [101, 102], [201, 202], [301, 302] 로 나옴.
    for j in i: #리스트 안의 리스트를 프린트하는걸로 결과는 각각의 변수로 나옴.
        print(j)
```


# 260109_python_study
> 대문자ㅡ> 소문자로, 소문자-> 대문자로.
>   > isupper()= 대문자인지?, islower()= 소문자인지?

```python
a= input()
if a.isupper():
    print(a.lower())
else:
    print(a)
```

```python
리스트 = ["가", "나", "다", "라"]
for i in range(1, len(리스트)):
    print(리스트[i])
```

```python
리스트 = ["가", "나", "다", "라"]
for i in range(len(리스트)-1,-1,-1):
    print(리스트[i])
```

```python
리스트 = [3, -20, -3, 44]

for i in 리스트:
    if  i<0:
        print(i)
```

```python
리스트 = [3, 100, 23, 44]
for i in 리스트:
    if i%3 == 0:
        print(i)
```

```python
리스트 = ['intra.h', 'intra.c', 'define.h', 'run.py']
for 변수 in 리스트:
  split = 변수.split(".")
  if (split[1] == "h") or (split[1] == "c"):
    print(변수)
```
