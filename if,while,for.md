# 제어문(Control Statment)

## 1.조건문(True / False)

### __if elif else__

- if <expression==True>:

```python
stress = int(input("오늘의 stress수치를 입력해주세요.(0~100)"))
if stress >= 80 :
    print('매우나쁨')
elif stress >= 60 :
    print('나쁨')
elif stress >= 40 :
    print('보통')
else : print('좋음')
```

- if문에서 80초과가 아닐경우 첫번째 elif로 내려가므로  elif 조건에 `60 <= stress < 80`를 안적어도 60이상 80미만에서만 나쁨이 출력됨
- else = if, elif 둘다 충족을 못시킬때



#### 조건 표현식

- <true 값> if <expression> else <false 값>

```python
#abs() 해석
number = int(input("숫자를 입력해 주세요"))
absolute = number if number >-0 else -number
print(absolute)

#위와 같이 나타내는것
```



## 2.반복문

### __while `____` :__

- 종료조건에 해당하는 코드를 통해 반복문을 종료

- 예시

```python
n = 0
while n<3:
    print(n)
    n=n+1
```

```python
number = [11,22,33,44,55]
n=0
while n<3:
    print(number[n])
    n=n+1
```

- 결과

```
0
1
2
```

```
11
22
33
```

- 조건이 true인 동안 반복적으로 실행 되기에 종료조건이 반드시 필요

  

### __for__

- 반복 가능한 객체(string,tuple,list,range,dict)를 모두 순회하면 종료

#### 기본형

```python
#number = list
number=[1,22,333]
for i in number:
    print(i)
```

```
1
22
333
```

- 정해진 범위를 반복하기에 종료 조건이 필요 없음

```
for <변수명> in <iterable>:
	~~~~
else :
	~~~~
```



#### str순회

- str순환시 한 글자씩 순회



#### dict 순회

- dict 순환시 기본적으로 key를 순회

```python
fordict = {'lee':10, 'jae':20, 'min':30}
print(fordict.keys())
print(fordict.values())
print(fordict.items())
```

```
dict_keys(['lee', 'jae', 'min'])
dict_values([10, 20, 30])
dict_items([('lee', 10), ('jae', 20), ('min', 30)])
```

- items()의 경우 (Key, value)의 튜플로 구성됨



#### enumerate 순회

- 인덱스와 객체를 담은 열거형 객체 반환

  - (index, value)형태의 tuple로 구성

  ```python
  hard = ['이거', '조금', '어렵네']
  for num, say in enumerate(hard):
      print(num, say)
  ```

  ```
  0 이거
  1 조금
  2 어렵네
  ```

  ```python
  hard = ['이거', '조금', '어렵네']
  for num, say in enumerate(hard):
      pass
  
  print(enumerate(hard))
  print(list(enumerate(hard, start=1)))
  ```

  ```
  <enumerate object at 0x00000160C19437C0>
  [(1, '이거'), (2, '조금'), (3, '어렵네')]
  ```

  

#### 표현식

```python
square**2 for num in range(1,7)
```

```
[1,4,9,16,25,36]
```

```python
{square : square**2 for square in range(1,7)}
```

```
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36}
```



### 반복 제어

- break
  - 반복문을 종료

- continue
  - continue 이후의 코드 블록은 수행하지 않고, 다음 반복을 수행

- for-else
  - 끝까지 반복문을 실행한 이후에 else문 실행
  - break를 통해 중간에 종료되면 else도 실행되지 않음

- pass
  - 아무것도 하지 않음
  - 반복문 아니여도 사용 가능

- else

  - 끝까지 반복문을 실행한 이후에 else문 실행

    
