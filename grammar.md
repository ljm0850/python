- 프로그래밍 언어 3형식

  - 저장
  - 조건
  - 반복

  

# 저장

변수 = 박스 ()

`list` = 박스모음 []

`dictionary` = 견출지가 붙은 박스 묶음 {}



## tuple

```python
tuple=(1,2,3,4,5,6,7)
```

- 불변
- `tuple()`를 통해 변환 가능

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

- 가변
- `list()`를 통해 변환 가능

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

- `dict()`를 통해 변환 가능



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

#### break continue

- 끝내고 건너 뜀



### 문장

```
\n = 줄바꿈
\t = 탭
\\= \ 문자 출력
\' = '문자 출력
\" = "문자 출력
```

```
%s = 문자열 포맷, 그 이후 %다음의 값을 문자열로 변환
%c = 유니코드 변환 
%d = 10진 정수
%o = 8진수
%x = 16진수
%f = 부동소수점 숫자로 출력
%% = %문자 출력
```

```
좌측정렬
"{0:<10}".format("좌측정렬")  
중앙정렬
"{0:^10}".format("중앙정렬") ->   중앙정렬   
공백 채우기
"{0:=^10}".format("중앙정렬") -> 공백이 '='로 채워짐
소수점 ".2f"
"{0:10.4f}".format(3.14592) -> 3.1459
```

```
비트연산 bin(number) -> 2진수로 변환
& 양변 비트 값 모두 1일경우 1
| 양변값 모두 0일경우 0 <수직선>
^ 양변값 다를경우 1 같으면 0
~ 비트값 1일경우 0, 0일경우1
<< 비트 왼쪽 이동
>> 비트 오른쪽 이동
```



### 전역,지역

- global :전역변수에서 찾음
- nonlocal : 지역변수가 아닌곳에서 찾음

- local :지역변수에서 찾음
