# Container

## tuple

```python
number=(1,2,3,4,5,6,7) or number = 1,2,3,4,5,6,7
print(number[0])

#8
```

- 불변 자료형,순서가 있음
- `tuple()`를 통해 변환 가능
- 단일 항목일 경우 `a=1,`과 같이 마지막 쉼표 필요

## list

```python
number = [1,3,6,8,10,32]
print(number[3])

#8
```

- 가변 자료형,순서가 있음
- `list()`를 통해 변환 가능
- `.append(newdata)`를 통해 list에 데이터 추가 

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



## set

```python
a={1, 2, 3, 1, 2}
print(a)

#{1, 2, 3}
```

- 가변 자료형,순서가 없음
- `set()`를 통해 변환 가능
- 중복값 제거

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

- 



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
