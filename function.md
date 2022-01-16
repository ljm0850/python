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
- ~~isdigit()~~: 숫자면 true, 문자가 섞이면 false

#### 변환함수

- chr(정수) : 정수를 입력하면 그 숫자의 유니코드에 대응하는 문자 반환

- ord(문자): 문자를 입력하면 그 문자의 유니코드에 대응하는 정수 반환

  ```python
  chr=chr(97)
  print(chr)
  =>a
  ord=ord(a)
  print(ord)
  =>97
  ```

- hex(): 10진 정수값을 16진수로 변환

#### 그외

- ~~filter(함수,목록)~~ : 조건에 해당하는 항목을 걸러내는 함수
- map(함수,인자) :  두번째 인자로 반복가능한 자료형을 받아 첫번째 인자로 함수 적용 결과 반환
- ~~dir()~~ : 어떤 객체를 인자로 넣어주면 해당 객체가 어떤 변수와 메소드를 가지고 있는지 나열
- ~~globals()~~: 글로벌 심볼 테이블을 딕셔너리 형태로 반환
- ~~locals()~~:지역 심볼 테이블을 딕셔너리 형태로 반환

- ~~id()~~: 고유 주소를 반환하는 함수
- ~~isinstance(객체,클래스)~~:첫번째 객체가 두번째 클래스에 관해 인스턴스 여부
- ~~issubclass(클래스,클래스)~~: 첫번째 클래스가 두번째 클래스의 서브인가 여부
- ~~eval()~~: 식을 실행하는 함수 `eval('abs(-8)') => 8`

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

