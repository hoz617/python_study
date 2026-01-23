# 260123_python_study

```python
class Human:
    def __init__(self, name):
        self.name = name

areum = Human("아름")
print(areum.name)

hangyeol = Human("한결")
print(hangyeol.name)
```


```python
class Human:
    def __init__(self, name, age, sex):
        self.name = name
        self.age = age
        self.sex = sex
    def __del__(self):
        print("나의 죽음을 알리지마라")
    

    def who(self):
        print("이름: {} 나이: {} 성별: {}".format(self.name, self.age,self.sex))  #format 매서드 중괄호 안에 값을 넣어줌.

    def setInfo(self, name, age, sex):
        self.name = name
        self.age = age
        self.sex= sex


class Human1:
    def __init__(self):
        pass

    def setName(self, name):
        self.name = name  # 이 방법을 더 많이 씀.
    def setAge(self, age):
        self.age = age #설정해주는 것

    def getName(self):
        print(self.name)  # 가져오는 것. set 함수 없으면 못씀.
       
    def who(self):
        print("이름: {} ".format(self.name))



areum = Human("아름", 25, "여자")
areum.who()

han = Human1()
han.setName("김한결")
han.getName()
```


```python
class Stock:
    def __init__(self, name, code,per,pbr, 배당수익률):
        self.name = name
        self.code = code
        self.per = per
        self.pbr = pbr
        self.배당수익률 = 배당수익률

    def set_name(self, name):
        self.name = name  #새터 개터 라고 불리는 걸로 새터는 정보를 설정해주는것

    def set_code(self, code):
        self.code = code

    def get_name(self):
        return self.name

    def get_code(self):
        return self.code

    def set_per(self, per):
        self.per = per

    def set_pbr(self, pbr):
        self.pbr = pbr

    def set_dividend(self, dividend):
        self.dividend =dividend

삼성 = Stock("삼성전자", "005930", 15.79,1.33,2.83)
삼성.set_per(12.75)
print(삼성.per)


종목 = [] #종목을 리스트로 저장하고

삼성 = Stock("삼성전자", "005930", 15.79, 1.33, 2.83)
현대차 = Stock("현대차", "005380", 8.70, 0.35, 4.27)
LG전자 = Stock("LG전자", "066570", 317.34, 0.69, 1.37)

종목.append(삼성) #종목 리스트에 객체를 집어넣는다
종목.append(현대차)
종목.append(LG전자)

for i in 종목:
    print(i.code, i.per) #반복문으로 코드, 퍼센트를 각각 다 출력하기
```

```python
class 차:
    def __init__(self, 바퀴, 가격):
        self.바퀴 = 바퀴
        self.가격 = 가격

    def 정보(self):
        print("바퀴수 ", self.바퀴)  # 정보를 바꿀 수 있는 함수 설정
        print("가격 ", self.가격)

class 자동차(차):
    def __init__(self, 바퀴, 가격):
        super().__init__(바퀴, 가격) #부모 클래스 불러오기

class 자전차(차):
    def __init__(self, 바퀴, 가격, 구동계):
        super().__init__(바퀴, 가격) #부모클래스 불러오기
        self.구동계 = 구동계 #부모인 차에 구동계 없으니까 구동계 정보 설정해주는 것 추가

    def 정보(self):
        super().정보()
        print("구동계 ", self.구동계)

bicycle = 자전차(2, 100, "시마노")
bicycle.정보()
```


# 260121_python_study

return= 반환해주는 함수.

```python
def print_reverse(str_val):
    return str_val[::-1]

print(print_reverse("python"))
```

```python
def print_score(list_val):
    return sum(list_val)/len(list_val)

a= [1,2,3]


print(print_score(a)) #프린트할때 한번 더 받아줘야한다. 지금 이코드에서는 printscore(a)가 결과값을 가지고 있는것.
```

```python
def printa(a):
    if a%2 == 0:
        return True
    else:
        return False

a= int(input())

print(printa(a))
```

```python
def print_sum(list_1):
    hab = 0
    for i in range(len(list_1)):
        hab += list_1[i]
    return hab
    
print(print_sum([1,2,3,4,5]))
```

```python
def print_sum(list_1):
    hab = 0
    for i in list_1:
        hab += i
    return hab
    
print(print_sum([1,2,3,4,5]))
```

```python
def print_sum(a,b):

    if a>b:
        hap=0
        for i in range(b,a+1):
            hap += i
        print(hap)
    
    
    else:
        hap=0
        for i in range(a,b+1):
            hap += i
        print(hap)
        
    
print_sum(6,1)
```

```python
def print_sum(a,b):
    c=0
    for i in a:
        if i == b:
            c += 1
    return c
    
    
print(print_sum("abcdb","b"))
```

# 260119_python_study
```pyton
user= int(input())
def print_upper_price(user) :
    print(user * 1.3)

print_upper_price(user)
```

별표현식 별에서부터 끝까지.
```pyton
scores = [8.8, 8.9, 8.7, 9.2, 9.3, 9.7, 9.9, 9.5, 7.8, 9.4]
*valid_score,a,b = scores


a,b,*valid_score = scores

a,*valid_score,b = scores
```

key, value 로 정해져 있는 딕셔너리.
중괄호{}로 나타낸다.
딕셔너리 값을 추가할려면 ice["죠스바"] = 1200 이런식으로~

```pyton
ice = {"메로나": 1000, "폴라포": 1200, "빵빠레": 1800}
ice["죠스바"] = 1200
ice["월드콘"] = 1500
print(ice)
```


keys() 메서드. 키값만 출력된다.

```pyton
inventory = {"메로나" : [300,20], "비비빅" : [400,3], "죠스바": [250,100]}
inventory["월드콘"]= [500,7]
print(list(inventory.keys()))
```

values 메서드. 밸류 값만 출력된다.

딕셔너리 update 메서드

```pyton
icecream = {'탱크보이': 1200, '폴라포': 1200, '빵빠레': 1800, '월드콘': 1500, '메로나': 1000}
new_product = {'팥빙수':2700, '아맛나':1000}
icecream.update(new_product)
print (icecream)
```



```pyton
def print_value_by_key(my_dict, key):
    print(my_dict[key])



my_dict = {"10/26" : [100, 130, 100, 100],
           "10/27" : [10, 12, 10, 11]}



print_value_by_key  (my_dict, "10/26")
```

```pyton
print_5xn(line):
    chunk_num = int(len(line) / 5)
    for x in range(chunk_num + 1) :
        print(line[x * 5: x * 5 + 5])
```

# 260116_python_study


()는 튜플, []은 리스트
endswith, startswith 끝나는 것,시작하는 것을 판별하는 함수.
이 함수에 여러개의 값을 넣을 때는 리스트가 아닌 튜플로 넣어야한다.

```pyton
words = ["apple", "banana", "avocado", "berry"]
for i in words:
    if i.startswith(("a","b")):
        print(i)
```

```python
log = "ERROR_2024_01.txt"
print(log.startswith(("ERROR","WARNING")) and log.endswith((".txt",".log"))
)
```

```python
names = ["Kim", "Lee", "Park", "Choi"]
result = []
for i in names:
    if i.startswith(("M","K")):
        result.append(i)
print(result)
```

def는 함수를 지정하고
지정한 함수 이름을 입력하면 호출이 된것이다.
지정하기전에 입력하면 에러가 난다~

```python
def print_coin():
    print("비트코인")


def print_coins():
    for i in range(100):
        print("비트코인")
```



# 260114_python_study
> +=, -=,*= 누적계산
>    > range는 for i 의 i에 숫자의 값을 가지게 함.
>    >range() 괄호 안 기본값은 stop(끝나는 위치)
>    >stop은 0- 2자리까지 나타내고 싶으면 +1해서 3으로 지정해야함(인덱스로 나타내는 것이기 때문)
>    >문자열 인덱싱 할때랑 마찬가지로.
>    >len() 은 리스트의 길이로 처음부터 끝까지를 나타내야할때 쓴다
>    >range가 없는 그냥 for문은 리스트안의 값을 그대로 가진다. (숫자가 아니라)

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
