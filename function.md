# 함수

## python함수

- Built-in Functions
  - print('hello wolrd')
  - abs(-11) => 11
  - len('hello') =>5

- Non-built-in Functions



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

