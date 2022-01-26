## OOP(Object-Oriented-Programming)

- 여러 독립된 객체들과 상호작용으로 하는 프로그래밍
- 객체(object)
  - type(타입) : 어떤 연산자(operator)와 상호작용 하는가
  - Attribute(속성) : 어떤 상태(데이터)인가
  - method(조작법) : 어떤 함수를 할 수 있는가
- 장점
  - 프로그램이 유연하고 변경이 용이
  - 배우기가 쉽고, 개발과 보사가 간편
  - 직관적인 코드 분석


## class

```python
#class Rectangle 
class Rectangle:
    # area라는 이름의 메소드 선언
    # self 대신 다른 단어를 써도 되긴 하지만 암묵적으로 self 고정
    def area(self):
        return self.x * self.y

#r1은 Rectangle class의 instance 선언
r1 =Rectangle()
r1.x = 10
r1.y = 20
# instace.MethodName 으로 접근
print(r1.area())

```

```python
class Rectangle:
    def __init__(self,x,y=1):
        # x,y는 instance 변수
        # y=1 값이 없을경우 기본값 설정
        self.x = x
        self.y = y
        
    def area(self):
        return self.x * self.y

r1 = Rectangle(10,20)
print(r1.area())
```

- `__init__`객체를 생성될때 호출하는 생성자 메소드

- `__del__` 객체가 소멸되기 직전에 호출되는 소멸자 메소드

- 매직 메소드

  - 특정 상황에 자동으로 불리는 메소드

  ```python 
  __str__(self), __len(self)__ , __repr__(self)
  __lt__(self,other) <lt 대신 le, eq, gt, ge, ne 등>
  ```

  - `__str__`: 해당 객체의 비형식적인(보기 좋게) print시 표현하는 문자열
  - `__repr__` :해당 객체의 형식적인 문자열 표현, 디버깅에 사용 (map~~~과 같이 표현되는것들) 

---------

```python
class person:
    def __init__(self,name,age):
        self.__name = name
        self.__age = age
        print("{0} 객체가 생성되었습니다.".format(self.name))
    
    def __del__(self):
        print("{0}객체가 제거되었습니다".format(self.name))
    
    def to_str(self):
    	return "{0}\t{1}".format(self.__name, self.__age)
    
    @property
    def name(self):
        return self.__name

    @property
    def age(self):
        return self.__age
    
    @age.setter
    def age(self, age):
        if age < 0 :
            reaise TypeError("나이는 0이상의 값만 허용합니다.")
            self.__age = age
    
    members= [
        person("일재민", 11)
		person("이재민", 22)
		person("삼재민",33)
    	]	
    
    members[0].age = 11 
```



#### 클래스 메소드

- `@classmethod` 데코레이터를 사용하여 정의

- 호출 시, 첫번째 인자로 클래스(cls)가 전달됨

  ```python
  class testclass:
      
      @classmethod
      def testclass_method(cls, x,y,z,...):
  ```

  

#### 스태틱 메소드

- @staticmethod 데코레이터 사용
- instance 변수, class 변수를 전혀 다루지 않는 메소드
  - 호출 시 어떠한 인자도 전달x, 클래스 정보 접근/수정 불가
- 속성을 다루지 않고 단지 기능만을 하는 메소드를 정의시 사용



#### getter 메소드, setter 메소드

- **변수에 접근할 수 있는 메소드를 별도로 생성**

- getter 메소드 : 변수의 값을 읽는 메소드
  - @property

- setter 메소드 : 변수의 값을 설정하는 메소드
  - @변수.setter



### 접근 제어자

- Public
  - 언더바(_)가 없이 시작하는 메소드나 속성
  - 어디서나 호출이 가능, 하위 클래스 override 허용

- Protected
  - 언더바(_) 1개로 시작하는 메소드나 속성
  - 암묵적으로 부모,자식 클래스에서만 호출 가능

- Private Member

  - 언더바(_) 2개로 시작하는 메소드나 속성
  - 본 클래스 내부에서만 사용이 가능

  

- **호출을 하고자 하면 할수는 있음**



## 클래스 상속

```python
class Person:
    def __init__(self,name,age):
        pass

class student(Person):
    def __init__(self,name,age,id):
        super().__init__(name,age)
        self.id = id
```

- class 선언시 위와 같이 선언
- issubclass(student,Person)
- **`super()`**
  - 하위 클래스에서 상위 클래스를 사용하고 싶을 경우 사용

- 하위 클래스에서 상위 클래스의 요소를 재정의 가능



##### 다중 상속

- 두개 이상의 클래스 상속 받는 경우
- 상속 받은 모든 클래스의 요소 사용 가능
- 중복된 속성이나 메서드의 경우 먼저 상속된 것이 적용됨<앞순서 먼저 상속>



### 다형성

- 동일한 메소드가 클래스에 따라 다르게 행동함
- 메소드 오버라이딩
  - 클래스 상속 시 상위 클래스에서 정의한 메소드를 자식 클래스에서 변경
  - 특정 기능을 바꾸고 싶을때 사용
  - 부모 클래스의 메소드를 실행하고 싶으면 super()활용



- 오버로딩(Python 해당x)
  - 함수 이름은 같으나, 매개변수 숫자에 따라 함수가 다르게 적용되는것