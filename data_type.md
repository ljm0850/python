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

## None

- 값이 없음을 표현하는 자료형
