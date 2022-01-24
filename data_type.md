# Data_type

## 불린형(Boolen)

- True / False 값을 가짐
- `0, 0.0, (), [], {}, '', None`는 False로 변환

```python
bool = True
print(type(bool))
```

`<class 'bool'>`

## 수치형

- int (정수) <오버플로우 발생x>

  - 2진수 : 0b
  - 8진수 : 0o
  - 16진수 :0x

- float (부동소수)

  - e-100과 같은 지수 표기법 사용

  - ```python
    1.8 - 0.6 != 1.2
    round(1.8-0.6,1) == 1.2
    ```

    round(값,소수점자리수) : 반올림

- complex (복소수)

  - complex.real + complex.imag 구조
  
  

## 문자열

- str('문자') 

- 특정 부분만 고칠수는 없지만, 순서는 존재

 ```python
 hello = '문자열'
 print(type(hello))
 ```

```
<class 'str'>
```

```
\n = 줄바꿈
\t = 탭
\\= \ 문자 출력
\' = '문자 출력
\" = "문자 출력
\0 = Null
```

### 문자열 조회/탐색 메소드

- `s.find(x)`: x의 첫 번째 위치를 반환, 없으면 -1 반환

  ```python
  'apple'.find('p') #1
  ```

- `s.index(x)`: x의 첫 번째 위치를 반환, 없으면 오류 발생

  ```python
  'apple'.index('p') #1
  'apple'.index('k') # error
  ```

- `s.isalpha()`:알파벳 문자 여부(유니코드 상)

  ```python
  'ㄱㄴㄷ'.isalpha() #true
  ```

- `s.isupper()`:대문자 여부

  ```python
  'Ab'.isupper() #False
  ```

- `s.islower()`:소문자 여부

  ```python
  'ab'.islower() #True
  ```

- `s.istitle()`:타이틀 형식 여부

  ```python
  'Title Title!'.istitle() #True
  ```

  

### 문자열 변경 메소드

- s.replace(old,new[,count]) : 바꿀 대상 글자를 새로운 글자로 바꿔서 반환

  ```python
  'coffee'.replace('e','i') #coffii
  'mooooyaho'.replace('o','@',2) #m@@ooyaho
  ```

- s.strip([chars]) : 공백이나 특정 문자를 제거

  - strip : 양쪽 , lstrip : 왼쪽, rstrip : 오른쪽 제거

  ```python
  '안녕하세요!!!!'.rstrip('!') #'안녕하세요'
  ```

  

- s.split([chars]) : 공백이나 특정 문자를 기준으로 분리

  ```python
  'kim-sp'.split('-') #['kim','sp']
  'a b c'.split() #['a','b','c']
  ```

  

- #'separator'.join([literable]) : 구분자로 iterable 합침

  ```python
  '!'.join('ljm')
  
  #'l!j!m'
  ```

- #s.capitalize() : 가장 첫 번쨰 글자를 대문자로

- #s.title() : `나 공백 이후를 대문자로

- #s.upper() : 모두 대문자

- #s.lower() : 모두 소문자

- #s.swapcase() : 대-소문자 변경





## Print

### f-strings

```python
month = 1
while month <= 12:
    print(f'2022년 {month}월')
    month = month + 1
```

```
2022년 1월
2022년 2월
	--
2022년 12월
```

- 문자열 맨 앞에 f를 붙여주고 {}안에 변수 이름을 넣어 표기하는 방법

```python
pi = 3.141592
f'원주율은 {pi:.3}. 반지름이 2일때 원의 넓이는 {pi*2*2}'
'원주율은 3.14. 반지름이 2일때 원의 넓이는 12.566368'
```

### str.format()

```python
print('Hello, {}! 성적은 {}'.format(name,score))
```

### %-formatting

```python
print('Hello, %s' % name)
print('내 성적은 %d' % score)
print('내 성적은 %f' % score)
```

```
Hello, lee
내 성적은 4
내 성적은 4.5
```

- %s : 문자열, %d : 정수, %f  : 실수

### 소수점 표현

```python
pi = 3.141592
print(f'원주율은 {pi:.3}. 반지름이 2일때 원의 넓이는 {pi*2**2:.7}')
#위와 같이:.자리수
```

### print 이후 \n 변경

```python
print("010","1234","5678", sep="-")
print("010","1234","5678", end=" ")
```

```
010-1234-5678
010 1234 5678
```



## None

- 값이 없음을 표현하는 자료형
