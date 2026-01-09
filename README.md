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

리스트 = [3, -20, -3, 44]

for i in 리스트:
    if  i<0:
        print(i)
리스트 = [3, 100, 23, 44]
for i in 리스트:
    if i%3 == 0:
        print(i)
리스트 = ['intra.h', 'intra.c', 'define.h', 'run.py']
for 변수 in 리스트:
  split = 변수.split(".")
  if (split[1] == "h") or (split[1] == "c"):
    print(변수)
