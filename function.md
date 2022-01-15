# 함수

## python함수

- Built-in Functions
  - print('hello wolrd')
  - abs(-11) => 11
  - len('hello') =>5

- Non-built-in Functions



## def 함수명 (매개변수)

- 필요한 함수를 직접 만들때 사용

```python
a = input()

def function(a):
    b= list(a)
    c= len(a)
    d= []
    while c > 0 :
        d.append(b[c-1])
        c=c-1
    x = d[0]+d[1]+d[2]
    return x
```

- return = 반환값

## Built-in Functions

#### range

- range(시작값,종료값,증감치)

```python
for i in range(0,5,1):
    print(i)
```

```
0
1
2
3
4
```

#### 수학과 관련된 함수

- abs() : 절대값
- ~~divmod() : 몫과 나머지를 tuple로 반환~~
- ~~pow(a,b) : a의 b제곱~~
- ~~max(),min() : 최대,최소값 반환~~

- ~~sorted() 오름차순 정리~~

#### 문장과 관련된 함수

- ~~all()~~ : 모든 항목이 true면 true반환, 한개라도 false이면 false 반환
- ~~any()~~ : 모든 항목이 false면 false반환, 한개라도 true이면 true 반환
- ~~zip()~~ : 인자를 받아 동일 '위치'의 항목을 묶어 튜플 항목으로 객체 생성

#### 그외

- ~~filter(함수,목록)~~ : 조건에 해당하는 항목을 걸러내는 함수
- ~~map()~~ :  두번째 인자로 반복가능한 자료형을 받아 첫번째 인자로 함수 적용 결과 반환
- 



## Python module

### random

- 함수가 포함된 코드를 불러온다. (import)
- python random 검색

#### random.choice(리스트)

- 리스트 중에서 1개를 랜덤하게 뽑음

```python
import random

menu = ('파스타','토마토달걀볶음','볶음밥','김밥','돈까스','라면','씨리얼')

#print(menu[0])

lunch=random.choice(menu)
print(lunch)
```

#### random.sample(리스트,개수n)

- 리스트에서 요소 n개를 랜덤하게 비복원 추출

```python
import random

lotto = range(1,46)
nunber = random.sample(lotto,6)
print(number)
```

