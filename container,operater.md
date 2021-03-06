# Container

## tuple

```python
number=(1,2,3,4,5,6,7) or number = 1,2,3,4,5,6,7
print(number[0])

#8
```

- 불변 자료형,순서가 있음
  - 값에 영향을 미치지 않는 메소드만 지원(type, 연산자*,T/F)

- `tuple()`를 통해 변환 가능
- 단일 항목일 경우 `a=1,`과 같이 마지막 쉼표 필요

## **list**

```python
number = [1,3,6,8,10,32]
print(number[3])

#8
```

- 가변 자료형,순서가 있음

- `list()`를 통해 변환 가능

  

### list 메소드

- `.append(x)`list 마지막에 x 추가

- `.insert(i,x)` list 인덱스 i에 x 삽입 (i가 list 길이보다 크면 맨뒤에 생성)

  ```python
  coffee = ['arabica','robustas']
  coffee.insert(1,'luwak')
  print(coffee)
  # ['arabica','luwak','robustas']
  ```

- `.remove(x)`list 가장 왼쪽에 있는 항목 x를 제거, 없을경우 error

  ```python
  coffee = ['arabica','robustas','luwak']
  coffee.remove('luwak')
  print(coffee)
  #['arabica','robustas']
  ```

- `.pop(i)`리스트 인덱스 i에 있는 항목을 반환 후 제거 , i를 입력 안하면 마지막 인덱스

  ```python
  coffee = ['arabica','robustas','luwak']
  coffee.pop()
  print(coffee)
  #['arabica','robustas']
  ```

  ```python
  num = [1,2,3,4,5,6,7]
  print(numbers.pop(0))
  print(numbers)
  # 1
  # [2,3,4,5,6,7]
  ```

  

- `.extend(m)`순회형 m의 모든 항목들의 리스트 끝에 추가(+=)

  ```python
  coffee = ['arabica','robustas']
  cafe.extend(['luwak'])
  print(coffee)
  #['arabica','robustas','luwak']
  ```

  ```python
  coffee = ['arabica','robustas']
  cafe.extend('luwak')
  print(coffee)
  #['arabica','robustas','l','u','w','a','k']
  ```

  ```python
  #.append와 a.extend
  app =[]
  app.append('apple')
  #app = ['apple']
  
  ext = []
  ext.extend('apple')
  #ext = ['a','p','p','l','e']
  ```

  

- `.index(x, start, end)`리스트에 있는 항목 중 가장 왼쪽에 있는 항목 x 인덱스를 반환

  ```python
  coffee = ['arabica','robustas','luwak']
  print(coffee.index('luwak'))
  # 2
  ```

  

- `.reverse()`리스트 순서를 반대로 뒤집음

  - `.revese()`는 원본을 바꿈
  - 내장함수`reversed()`는 원본을 안바꿈

- `.sort()`리스트를 정렬

  ```python
  num=[5,2,4,3,1]
  #num1은 원본 변경이라 할당이 안됨
  num1 = num.sort()
  print(num,num1)
  #[1,2,3,4,5] None
  ```

  ```python
  num = [5,2,4,3,1]
  num2 = sorted(num)
  print(num,num2)
  # [5, 2, 4, 3, 1] [1, 2, 3, 4, 5]
  ```

  ```python
  mix_num_alpha1 = [(4,'e'),(1,'b'),(1,'a'),(2,'c'),(3,'d')]
  mix_num_alpha1.sort(key = lambda num:num[0] )
  print(mix_num_alpha1)
  # [(1, 'b'), (1, 'a'), (2, 'c'), (3, 'd'), (4, 'e')]
  
  mix_num_alpha2 = [(4,'e'),(1,'b'),(1,'a'),(2,'c'),(3,'d')]
  mix_num_alpha2.sort(key = lambda alpha:alpha[1])
  mix_num_alpha2.sort(key = lambda num:num[0] )
  print(mix_num_alpha2)
  # [(1, 'a'), (1, 'b'), (2, 'c'), (3, 'd'), (4, 'e')]
  ```

  

- `.count(x)`리스트에서 항목 x가 몇개 존재하는지 갯수 반환

  ```python
  num = [1,2,3,4,1,2,3,4,1,2,3]
  num.count(4)
  #2
  ```

  

- `.clear()`모든 항목을 삭제

## range

- range(a,b,c)
  - a부터 b-1까지 s증감


```python
for i in range(0,5,1):
    print(i)
    
#0
#1
#2
#3
#4
```

## 패킹/언패킹

- ```python
  #튜플 패킹
  ljm = (123,75)
  #튜플 언패킹
  num1, num2 = ljm
  print(num1, num2)
  
  # 123 75
  ```

- ```python
  x, *y = 1, 2, 3, 4
  print(x,y)
  
  # 1 [2,3,4]
  ```


- ```python
  x = [1,2,3]
  print(x)
  print(*x)
  
  #[1,2,3]
  #1 2 3
  ```

`def dict_list(*args)` 와 같이 쓰일때는 args가 ()가 씌워져서 tuple로 들어옴



## set

```python
a={1, 2, 3, 1, 2}
print(a)

#{1, 2, 3}
```

- 가변 자료형,순서가 없음
- `set()`를 통해 변환 가능
- 중복값 제거
- 메소드
  - s.copy() : 복사본 반환
  - s.add(x): x 추가
  - s.pop() : 랜덤하게 항목을 반환하고 제거, set이 비어 있을 경우 KeyError
  - s.remove(x) : 항목 x를 삭제, 존재하지 않을경우 KeyError 
  - s.discard(x) : 항목 x가 있을 경우 x삭제
  - s.update(t): set t에 있는 모든 항목중 셋s에 없는 항목을 추가
  - s.clear() : 모든 항목 제거
  - s.isdisjoint(t): set s와 set t가 같은 항목이 하나도 없으면 True
  - s.issubset(t) :set s가 set t의 하위 set일 경우 True
  - s.issuperset(t): set s가 set t의 상위 set일 경우 True

## dictionary(key-value)

```python
number = {'파':1,'이':2,'썬':3,}
print(number['썬'])

#dictionary 변경
number['썬'] = 4
print(number['썬'])

for pp in number.keys():
    print(pp)
for pp in number.values():
    print(pp)
for pp in number.items():
    print(pp)
#3 4
#파 이 썬
#1 2 4
#('파',1)('이',2)('썬',4)
```

- 가변 자료형,순서가 없음
  - key에는 불변 자료형만 가능
  - value에는 모든 자료형 가능
- `dict()`를 통해 변환 가능
- dict.get()

```python
my_home = {
    'location': 'gj',
    'code': '82+',
}

# 딕셔너리 원소 접근
print(my_home['location'])
#print(my_home['name']) 오류발생
print(my_home.get('location'))
#print(my_home.get('name')) None으로 나옴
```

```python
classbook = {}
a=int(input('인원수'))
for i in range(a):
    classbook[input('이름')] = int(input('나이'))

print(classbook)
```

- dict.setdefault()

  - key가 dictionary에 있으면 value를 돌려준다

  - key가 없을 경우 default값을 갖는 key를 삽입한후 default를 반환

    ```python
    setdef = {'성': 'l', '이름':'jm'}
    print(setdef.setdefault('성'))
    setdef.setdefault('호','흑우')
    
    print(setdef)
    #ㅣ
    #{'성': 'l', '이름': 'jm', '호': '흑우'}
    ```

    

- 메소드

  - d.clear() 

  - d.copy() : 복사본 반환

  - d.keys() : 모든 키를 반환

  - d.values() : 모든 값을 반환

  - d.items() : 키-값 쌍을 반환

  - d.get(k) : 키 k의 값을 반환하는데 없을경우 None

  - d.get(k, v): 키 k의 값을 반환하는데 없을경우 v반환

  - d.pop(k) : 키 k인 값을 반환하고 삭제, 없을경우 KeyError

  - d.update(NewDict): 딕셔너리 d값을 매핑하여 업데이트,덮어쓰기

    ```python
    my_dict = {'apple': '사과', 'banana': '바나나', 'melon': '멜론'}
    my_dict.update({'apple':'사과아'})
    ```

- dict.fromkeys(ls,a):

  - ls 리스트 값 : a 인 dict 생성

  - ```python
    a = ['l','j','m']
    b = [1,2,3]
    c = dict.fromkeys(a,b)
    print(c)
    # {'l': [1, 2, 3], 'j': [1, 2, 3], 'm': [1, 2, 3]}
    ```



### defaultdict

- `from collections import defaultdict`

```python
from collections import defaultdict
test = defaultdict(int)
test['l']
print(test)
# defaultdict(<class 'int'>, {'l': 0})

test2 = defaultdict(list)
test2['l']
print(test2)
// defaultdict(<class 'list'>, {'l': []})
```

- key만 주고 value값을 주지 않을 경우 자동으로 기본값을 value로 제공
  - int 기본값:  0
  - list 기본값: []
  - dict 기본값: {}




#  연산자(operator)

### 논리연산자

- A and B : A와 B 모두 True시 True
- A ro B : A와 B 모두 False시 False
- Not : True를 False로, False를 True로

### 멤버십 연산자

- in<->not in : 시퀀스 포함 여부

### 슬라이싱[시작:끝:간격]

```python
[1,3,5,7][1:4] ->[3,5,7]
(1,2,3)[:2] -> (1,2)
range(10)[5:8] -> range(5,8)
'asdf'[2:4] ->'df'
```

`a[::-1]`의 경우 a를 거꾸로 



### set 연산자

- |: 합집합
- & : 교집합
- -: 여집합
- ^:대칭차



## 할당

```python
num1 = [1, 2, 3]
num2 = num1

num2[0] = 5
print(num1)
#[5,2,3]
```



## 얕은 복사(Shallow copy)

- slice 연산자

  ```python
  b=a[:]
  b[0] = 5
  print(a,b)
  #[1, 2, 3] [5, 2, 3]
  ```

- list() 활용

  ```python
  b = list(a)
  b[0] = 5
  print(a,b)
  #[1, 2, 3] [5, 2, 3]
  ```

  

- **얕은 복사의 문제**

  ```python
  a = [1, 2, [1, 2]]
  
  b = a[:]
  b[2][0] = 5
  
  print(id(a))
  print(id(b))
  #id가 다르게 나옴
  print(id(a[2]))
  print(id(b[2]))
  print(a)
  # id가 같게 나옴
  #[1, 2, [5, 2]]
  ```

  

## 깊은 복사 (Deep copy)

```python
import copy

a=[1,2,[1,2]]
b=copy.deepcopy(a)

b[2][0] = 5
print(a)
#[1, 2, [1, 2]]
```

