# Data_type, 문자열

### 숫자

```python
number = 119
print(type(number))
```

```
<class 'int'>
```

- int = 정수
- float = 부동소수

### 문자

```python
hello = '문자열'
print(type(hello))
```

```
<class 'str'>
```

- str = 문자

### boolean (참/거짓)

```python
bool = True
print(type(bool))
```

```
<class 'bool'>
```



### 형변환

```python
number = '3'
print("str합",number + '5')
print("int합",int(number)+5)
```

```
str합 35
int합 8
```



## f-string

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





