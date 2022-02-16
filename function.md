# 함수

## python함수

- Built-in Functions
  - print('hello wolrd')
  - abs(-11) => 11
  - len('hello') =>5

- Non-built-in Functions



## def 함수명 (매개변수)

- 필요한 함수를 직접 만들때 사용
- `def name parameters:`
- `name(Argument)` 로 함수 호출

```python
def calc_sum(x,y):
    return x+y

a,b=2,3

c=calc_sum(a,b)
d=calc_sum(a,c)

print("c결과:{0}".format(c))
print("d결과:{0}".format(d))

#calc_sum = name, x,y = parameters, calc_sum(a,b)에서 a,b가 argument
```

- return = 반환값



```python
def say(*word):
    print(word)
say('hi','hello','안녕')
```

```python
def dictionaryfx(**say):
    for key, value in say:
        print(key,":",value)
        
dictionaryfx(korean='안녕',english1='hello',english2='hi')
```



#### 재귀 함수

- 자기 자신을 호출하는 함수
- 1개 이상의 종료 상황이 존재하고, 수렴하도록 작성

```python
#Factorial n!
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)
```



## Built-in Functions

- `print(dir(__builtins__))`

- lambda

  - 익명 함수, 임시로 함수를 사용하기 위해 

  - ```python
    triangle_area = lambda b, h : 0.5 * b * h
    print(triangle_area(5,6))
    ```

#### 수학과 관련된 함수

- abs() : 절대값

- ~~divmod() : 몫과 나머지를 tuple로 반환~~

- ~~pow(a,b) : a의 b제곱~~

- ~~max(),min() : 최대,최소값 반환~~

- .sort  sorted() :오름차순 정리

  

#### 문장과 관련된 함수

- ~~all()~~ : 모든 항목이 true면 true반환, 한개라도 false이면 false 반환

- ~~any()~~ : 모든 항목이 false면 false반환, 한개라도 true이면 true 반환

- ~~zip()~~ : 인자를 받아 동일 '위치'의 항목을 묶어 튜플 항목으로 객체 생성

- ~~isdigit()~~: 숫자면 true, 문자가 섞이면 false

- 문자열.split(sep='구분자',maxsplit=분할횟수)
  - 문자열을 maxsplit 횟수만큼 sep의 구분자를 기준으로 자름

  - sep 기본값은 none, maxsplit의 기본값은 -1

    ```py
    numbers = '1,2,3,4,5,67 8,9'
    print(numbers.split(',',2))
    #['1', '2', '3,4,5,67 8,9']
    ```

- '구분자'.join()

  ```python
  numbers = [1, 2, 3]
  print(''.join([str(num) for num in numbers]))
  #123
  print('-'.join([str(num) for num in numbers]))
  #1-2-3
  ```

  

#### 변환함수

- 아스키 코드 https://ko.wikipedia.org/wiki/ASCII

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

- ~~filter(function.iterable))~~ : 조건에 해당하는 항목을 걸러내는 함수

  - true인 것들로만 구성하여 `filter object` 로 반환

- map(함수,인자) :  두번째 인자로 반복가능한 자료형을 받아 첫번째 인자로 함수 적용 결과 반환

  ```python
  a=input().split()
  b=map(int,a)
  print(list(b))
  
  n,m = map(int,input().split())
  print(n,m)
  ```

- ~~dir()~~ : 어떤 객체를 인자로 넣어주면 해당 객체가 어떤 변수와 메소드를 가지고 있는지 나열

- ~~globals()~~: 글로벌 심볼 테이블을 딕셔너리 형태로 반환

  - ```
    num = 1
    def local_scope():
        global num
        num = 5
    
    local_scope()
    print(num)
    ```

- ~~locals()~~:지역 심볼 테이블을 딕셔너리 형태로 반환

- ~~id()~~: 고유 주소를 반환하는 함수

- ~~isinstance(객체,클래스)~~:첫번째 객체가 두번째 클래스에 관해 인스턴스 여부

- ~~issubclass(클래스,클래스)~~: 첫번째 클래스가 두번째 클래스의 서브인가 여부

- ~~eval()~~: 식을 실행하는 함수 `eval('abs(-8)') => 8`

- reversed() : 역순으로 만들어 reversed object로 형성

  ```python
  num=10
  for i in reversed(range(num)):
      print(i)
  # 9 8 7 6 5 4 3 2 1 0
  ```

  

## Python module&package

- module:다양한 기능을 하나의 파일로 묶은것

- package:다양한 모듈을 하나의 폴더로 묶은것

- library:다양한 패키지를 하나로 묶은것

- `import "module"`로 불러오는 형식

  - ```python
    import module
    from module import var,function, class
    from module import *
    from module.폴더 import (파일)
    ```

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



### with

- 사용후 반납해야 하는 경우 사용

- ```python
  class hi:
      def __enter__(self):
          print('start')
          return self
      
      def hello(self, name):
          print('hello' + name)
          
  	def __exit__(self, exc_type, exc_val, exc_tb):
          #이부분은 아직 잘 이해x
          print('end')
  ```

  

- ```python
  with hi() as h:
      h.hello('ljm')
  
  # start
  # hello ljm
  # end
  ```



### open

- open('파일명', '파일모드', encoding='인코딩방식')

  - 인코딩 방식 **utf-8**: 다국어 지원 , **ecu-kr** : 한국어 지원
  - 파일모드 write,read,a
    - a: 파일을 이어쓰는 모드

- ```python
  file = open('chobo.txt','w', encoding='utf-8')
  file.write('Hello, world!\n')
  file.write('Hi, python\n')
  file.close()
  ```

  - .close() 안적으면 프로그렘 종료시까지 파일 수정 불가



```python
if __name__ == '__main__':
#메인 함수의 선언,시작    
    bookJson = open('data/book.json', encoding='UTF8')
    #bookJson이 호출되면 해당 주소를 UTF-8로 인코딩하여 open
    book_list = json.load(bookJson)
    #해당 파일을 읽을때 사용
```

