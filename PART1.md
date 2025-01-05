## 사칙연산(10869)

-  [x] 제출코드
```python
a,b = map(int, input().split())
print(a+b, a-b, a*b, a//b, a%b, sep='\n')
```

-  [x] 📝
```python
문자열.split()  #띄어쓰기를 기준으로 문자열 나누기 
문자열.split('구분자')  #구분자를 기준으로 문자열 나누기
```

```python
map(function, iterable)  #iterable(반복가능객체)에 function(함수)을 수행
map(function, iterable1, iterable2)  #function의 입력값이 두 개인 경우
```
- 반복문 대신 한줄의 코드로 처리 가능 ▶ 가독성 증가
- 내부적으로 C로 구현되어 있어 Python 반복문보다 빠른 속도
- 지연평가(lazy evaluation) 방식 ▶ 효율적인 메모리 사용과 성능 최적화

> **지연평가(lazy evaluation)** <br/>
> iterator는 값을 차례대로 꺼낼 수 있는 객체로, 데이터를 미리 만들어두지 않고 필요한 시점이 되었을 때 데이터를 생성(=지연평가) ▶ 불필요한 계산 방지


-  [x] **+ lambda 표현식**
```python
iter = range(1,5)
print(list(map(lambda x : x**2, iter)))  #결과: [1, 4, 9, 16]
```


## 곱셈(2588)

-  [x] 제출코드
```python
a = int(input())
b = input()

for i in range(len(b), 0, -1) :
    print(a*int(b[i-1]))
print(a*int(b))
```


## 윤년(2753)

-  [x] 제출코드
```python
year = int(input())
if ((year%4 == 0)and(year%100 != 0)) or (year%400 == 0):
    print('1')
else:
    print('0')
```


## X보다 작은 수(10871)

-  [x] 제출코드
```python
N, X = map(int, input().split())
A = list(map(int, input().split()))

for i in range(N):
    if A[i] < X:
        print(A[i],end=" ") 
```


## OX퀴즈(8958)

-  [x] 제출코드
```python
N = int(input())

for i in range(N):
    a = input()
    score = 0
    result = 0
    for j in a:
        if j == 'O':
            score += 1
        else:
            score = 0
        result += score
    print(result)
```


## 평균은 넘겠지(4344)

-  [x] 제출코드
```python
N = int(input())

for i in range(N):
    num = list(map(int, input().split()))
    avg = sum(num[1:])/num[0]
    cnt = 0
    for score in num[1:]:
        if score > avg:
            cnt += 1
    print('%.3f' % (cnt / num[0] * 100) + '%')
```
*round 사용 시 틀리는 이유 : 반올림해서 0으로 딱 떨어질 때 round는 해당 값 출력 X


## 아스키 코드(11654)

-  [x] 제출코드
```python
a = input()
print(ord(a))
```
*chr(숫자), ord(문자)


## 단어의 개수(1152)

-  [x] 제출코드
```python
print(len(input().split()))
```


## 달팽이는 올라가고싶다(2869)

-  [x] 제출코드
```python
import math

A, B, V = map(int, input().split())
print(1+math.ceil((V-A)/(A-B)))
```


## 소수 찾기(1978)

-  [x] 제출코드
```python
import math

def prime(a):
    if a == 1:
        return 0
    for i in range(2, int(math.sqrt(a))+1):
        if a % i == 0:
            return 0
    return 1

N = input()
num = list(map(int, input().split()))

cnt = 0
for i in num:
    cnt += prime(i)
print(cnt)
```
*에라토스테네스의 체


## 팩토리얼(10872)

-  [x] 제출코드
```python
import math

N = int(input())
print(math.factorial(N))
```
```python
N = int(input())
result = 1

for i in range(1, N+1):
    result *= i

print(result)
```
```python
def factorial(n):
    if n>1:
        return n*factorial(n-1)
    else:
        return 1
    
N = int(input())
print(factorial(N))
```


## 하노이 탑(1914)

-  [x] 제출코드
```python
   
```

