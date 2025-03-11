# 데이터 타입

자료형이란 컴퓨터에서 가지는 정보가 숫자인지 문자인지 표시를 해주는 것, 즉 변수가 저장하는 데이터 형식을 말한다.

파이썬에서는 `type()` 함수를 사용하면 자료형을 쉽게 알 수 있다.

```py
>>> type(6)
<class 'int'>
>>> type('A')
<class 'str'>
>>> type(100000000)
<class 'int'>
>>> type(2.8)
<class 'float'>
>>> type(3+4j) # 복소수
<class 'complex'>
```

## 시퀀스

문자열 `str` , 리스트 `list` , 튜플 `tuple` , 사용자 정의 클래스가 시퀀스에 속한다.

```py
>>> type("Love your Enemies, for they tell you your Faults.")
<class 'str'>
>>> type(['love', 'enemy', 'fault'])
<class 'list'>
>>> type(('love', 'enemy', 'fault'))
<class 'tuple'>
```

## 매핑

딕셔너리 `dict` 즉, key/value의 짝으로 이뤄진 것을 매핑이라고 한다.

```py
>>> type({'one': 1, 'two': 2, 'three': 3})
<class 'dict'>
```

## 불

참, 거짓을 표현 하는 불 `bool`

```py
>>> type(False)
<class 'bool'>
>>> type(3 >= 1)
<class 'bool'>
>>> type(True == 'True')
<class 'bool'>
```

## 세트

집합을 표현하는 세트 `set`

```py
>>> fruits = {'apple', 'banana', 'orange'}
>>> type(fruits)
<class 'set'>
```
