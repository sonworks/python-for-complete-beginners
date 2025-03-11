# 함수

함수를 사용하면 반복적인 코드를 줄이면서 코드를 사용하기 좋게 정리할 수 있다.

```py
# 리스트의 원소들을 출력하는 함수
>>> def print_list(a):
...     for i in a:
...         print(i)
... 
>>> a_list = [3, 4, 62, 27, 83, 956, 26, 58, 3, 78, 168, 64, 78]
>>> print_list(a_list)
3
4
62
27
83
956
26
58
3
78
168
64
78
```

## 반환문

```py
# 입력값이 '참' 인지 '거짓' 인지 맞추는 함수
>>> def quiz():
...     ans = input('1 + 2 = ')
...     return 1 + 2 == int(ans)
... 
>>> quiz()
1 + 2 = 3
True
>>> quiz()
1 + 2 = 2
False
```

## 람다(lambda)

> 람다 형식은 인공지능 분야나 AutoCAD라는 설계 프로그램에서 쓰이는 Lisp 언어에서 물려받았다고 하며, 딱 한 줄만으로 함수의 기술이 가능하다.

```py
lambda 매개변수 : 표현식
```

```py
# 함수를 이용하여 두 수의 합을 구하기
>>> def hap(x, y):
...     return x + y
... 
>>> hap(10, 20)
30
# lambda 를 이용하여 두 수의 합을 구하기
>>> (lambda x,y: x + y)(10, 20)
30
```

### map()

```py
map(함수, 리스트)
```

```py
# x값을 5회 제곱한 값을 리스트로 출력하기
>>> list(map(lambda x: x ** 2, range(5)))
[0, 1, 4, 9, 16]
```

### reduce()

```py
reduce(함수, 시퀀스)
```

```py
# 5개의 값을 누직적으로 더하기
>>> from functools import reduce # 파이썬3에서는 기술하여야 함
>>> reduce(lambda x, y: x + y, [0, 1, 2, 3, 4])
10
# 문자를 누직적으로 더하기
>>> reduce(lambda x, y: y + x, 'abcde')
'edcba'
```

### filter()

```py
filter(함수, 리스트)
```

```py
# 5보다 작은 수만 출력하기
>>> list(filter(lambda x: x < 5, range(10)))
[0, 1, 2, 3, 4]
```
