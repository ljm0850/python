### 문장

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



```python
import datetime
today = datetime.datetime.now()
print(today)
```

```py
import math

num1 = 0.1 * 3
num2 = 0.3

abs(num1 - num2) <= sys.float_info.epsilon
isclose(num1, num2)
```

