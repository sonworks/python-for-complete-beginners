# 제어 구조

## while 반복문

```py
# 1부터 100까지 출력하기기
>>> num = 1
>>> while num <= 100:
...     print(num)
...     num = num + 1
... 
1
2
3
(생략)
99
100
```
## for 반복문

```py
# 가족 이름과 문자열 길이를 출력하기
>>> for x in family:
...     print(x, len(x))
... 
mother 6
father 6
sexy lady 9
# 2이상 7미만인 숫자만 출력하기
>>> a = [4, 5, 6, 7]
>>> for i in a:
...     print(i)
... 
4
5
6
7
# 2이상 7미만인 숫자만 출력하기 (range이용 예시)
>>> list(range(2, 7))
[2, 3, 4, 5, 6]
```

## if 조건문

```py
# a와 b의 큰 수 찾기
>>> a = 1234 * 4
>>> b = 13456 // 2
>>> if a > b:
...     print('a is big')
... elif a == b:
...     print('both the same')
... else:
...     print('b is big')
... 
b is big
```

## for-else와 while-else

파이썬에서는 반복문에도 else 를 사용 가능하다.

```py
# 리스트의 원소를 차례대로 출력 후, 출력 완료 메시지를 출력하기
>>> for x in [1, 2, 3, 4]:
...     print(x)
... else:
...     print("모두 출력했어요")
... 
1
2
3
4
모두 출력했어요
```

## while-else

```py
# 카운트다운 숫자를 출력 후, 출력 완료 메시지를 출력하기
>>> countdown = 5
>>> while countdown > 0:
...     print(countdown)
...     countdown -= 1
... else:
...     print("모두 출력했어요")
... 
5
4
3
2
1
모두 출력했어요
```
