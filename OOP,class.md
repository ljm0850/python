## OOP(Object-Oriented-Programming)

- 재사용이 가능한 프로그레밍
- 객체지향
  - class = (청사진) 같은 문제 도메인에 속하는 속성과 행위를 정의
  - 변수 = 값
  - 메서드(실행코드)

## class

```python
class 클래스 명:
    def __init__(self,매개변수):
        ---
    def __del__(self):
        ---

```

- `__init__`객체를 생성하기 위해 호출하는 생성자 메서드

- `__del__` 객체가 소멸되기 전에 호출되는 소멸자 메서드

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
    
    members[0].age = 11     <age@property를 이용해 변수처럼 값 저장>
```

- `self.name = name` **->** `self.__name = name`: 프라이빗 필드 생성

- 데코레이터 기능(@property,@age.setter) 변수처럼 사용 가능
- 클래스 변수 접근
  - 클래스명.클래스변수



## 클래스 상속

- class 클래스명(부모클래스명)

  ```python
  class 클래스이름:
      @staticmethod
      def 메서드(매개변수1, 매개변수2):
          코드
  ```

  - @staticmethod : 정적메서드, 매개변수에 self를 지정x
  - ~~get_`---`~~
    - 값을 가져오는 메서드
  - ~~@`----`.setter~~
    - 값을 저장하는 메서드

  ```python
  def __repr__(self):
  	return "{}".format(self.__class__.__name__,self.name,self.gender)
  ```

  - `def __repr__(self)`: 객체의 표현을 지원