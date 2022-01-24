# 에러와 예외

## 에러

- 문법 에러(Syntax Error)
- ZeroDivisionError
  - 0으로 나눌때 발생
- NameError
  - namespace 상에 이름이 없을때

- TypeError

- ValueError
  - 타입은 올바르나 값이 적절하지 않을 경우

- IndexError
  - 인덱스가 존재하지 않거나 범위를 벗어나는 경우
- KeyError
  - Dictionary에서 해당 key가 존재하지 않을 경우
- ModuleNotFoundError
  - 존재하지 않는 모듈을 import 하는 경우
- ImportError
  - Module은 있으나 존재하지 않는 클래스/함수를 가져오는 경우
- KeyboardInterrupt
  - 임의로 프로그램을 종료하였을 때
- IndentationError
  - Indentaion(들여 쓰기)가 적절하지 않을 경우

## 예외(Exception)

### try / except

#### try문

- 오류가 발생할 가능성이 있는 코드를 실행
- 예외가 발생하지 않으면, except없이 실행 종료

### except문

- 예외가 발생시 except 절이 실행

- 예외 상황을 처리하는 코드를 받아 조치

  ```python
  try:
      명령분
      except 예외1 as 변수1 :
          명령문
      except 예외2 as 변수2:
          명령문
      finally(선택):
          명령문
  ```

  ```python
  try:
      num = input()
      print(int(num))
  #except ValueError: 
  #except :    
      print('숫자가 입력되지 않았습니다')
  ```

- try : 코드를 실행

- except : try 문에서 예외가 발생 시 실행

- else : try 문에서 예외가 발생하지 않으면 실행

- finally : 예외 발생 여부와 상관없이 실행

- as 키워드를 활용하여 원본 에러 메세지 사용 가능

  ```python
  try :
      a = []
      print(a[-1])
  except IndexError as b:
      print(f'{b},오류가 발생했습니다.')
  #list index out of range, 오류가 발생했습니다
  ```

  

### 예외 발생시키기

- raise를 통해 예외를 강제로 발생

  - raise <표현식>(메시지)

    ```python
    raise ValueError('값 에러')
    #ValueError : 값 에러
    ```

- assert를 통해 예외를 강제로 발생

  - assert <표현식>, <메시지>

  - 상태를 검증하는데 사용, AssertionError가 발생

  - 디버깅 용도로 사용

    ```python
    assert len([1,2,3]) == 1, '길이가 1이 아닙니다'
    #AssertionError : 길이가 1이 아닙니다
    ```

    