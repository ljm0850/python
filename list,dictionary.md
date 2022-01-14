- 프로그래밍 언어 3형식

  - 저장
  - 조건
  - 반복

  

# 저장

변수 = 박스 ()

`list` = 박스모음 []

`dictionary` = 견출지가 붙은 박스 묶음 {}



## list

- 예시

```python
number = [1,3,6,8,10,32]

print(number[3])
```

- 결과

```
8
```



## dictionary

- 예시

```python
number = {'파':1,'이':2,'썬':3,}
print(number['썬'])

#dictionary 변경
number['썬'] = 4
print(number['썬'])
```

- 결과

```
3
4
```





# 조건

## if elif else

- __ture - false__로 결정하여 진행됨

```python
stress = int(input("오늘의 stress수치를 입력해주세요"))
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



# 반복

## while `----`:

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

  

## for

- 예시

```python
number=[1,22,333]
for i in number:
    print(i)
```

- 결과

```
1
22
333
```

- 정해진 범위를 반복하기에 종료 조건이 필요 없음