# Built-in-module

## unittest module

- https://docs.python.org/ko/3/library/unittest.html

- **Java**의 `JUnit` , **JavaScript**의 `Jest``Mocha`와 같은 단위 테스트 프레임워크

  ```python
  import unittest
  ```

### TestCase class

- 단위 테스트에 필요한 메소드 제공

  ```python
  from unittest import TestCase
  
  class MyTest(TestCase) :
      def Test_one_plus_two(self):
          self.assertEqual(1 + 2,3)
  ```

  - assert

### asseretion 메소드

```python
from unittest import TestCase

class Mytest(TestCase) :
    def test_other_assertions(self):
        self.assertTrue(1==1)
        self.assertFalse(1==2)
        ...
```

