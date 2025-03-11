# 파이썬 시작하기

 * 파이썬 공식 홈페이지: https://www.python.org/
   - `Launch Interactive Shell` 아이콘을 클릭하면 파이선 셸이 기동됨
 * 파이썬 튜터: https://pythontutor.com/
 * ideone : https://ideone.com/

## 사칙 연산

```py
# 덧셈
>>> 1 + 2
3
# 뺄셈
>>> 50 - 4
46
# 곱셈
>>> 12345678 * 3
37037034
# 나눗셈
>>> 5000 / 3
1666.6666666666667
>>> 5000 // 3
1666
# 나머지
>>> 50 % 8
2
# 몫과 나머지를 한번에 구하기
>>> divmod(50, 8)
(6, 2)
```

## 변수
```py
# 변수의 값 계산하기
>>> watch = 1000
>>> lighter = 1500
>>> watch + lighter
2500
# 문자열 변수 더하기
>>> a = "pig"
>>> b = "dad"
>>> a + b
'pigdad'
>>> a + ' ' + b
'pig dad'
```

## 리스트

```py
# 리스트의 요소수 구하기
>>> family = ['mother', 'father', 'gentleman', 'sexy lady']
>>> len(family)
4
# 요소 추출하기
>>> family[2]
'gentleman'
# 요소 제거하기
>>> family.remove('gentleman')
>>> family
['mother', 'father', 'sexy lady']
```
## 인터프리터와 컴파일러

 * 인터프리터: 한마디 할 때마다 동시 통역해주는 방식
 * 컴파일러: 처음부터 끝까지 듣고 나서 한꺼번에 바꿔주는 방식

 > 파이썬은 명령을 한 줄씩 해석해서 일을 하는 인터프이터 방식이다.

 * [인터프리터와 컴파일러를 설명한 애니메이션@YouTube](https://youtu.be/Dx2tSsd3aFc)

## 파이썬 설치

 * 공식 파이썬 다운로드 페이지
   - https://www.python.org/downloads/

### Python for windows

최신버전(2025년 3월 현재): python-3.13.2-amd64.exe

```cmd
> python -V
Python 3.13.2
```

## 파이썬 인터프리터

> 파이썬 코딩규약에서는 반드시 들여쓰기를 지켜주어야 한다. 들여쓰기를 할 때는 공백 4칸씩 들여쓰기 하면 된다.

```py
# ch01-6-triangle.py
print('직각삼각형 그리기\n')
leg = int(input('변의 길이: '))

for i in range(leg):
    print('* ' * (i + 1))

area = (leg ** 2) / 2
print('넓이:', area)
```

```cmd
> python .\ch01-6-triangle.py
직각삼각형 그리기

변의 길이: 4
*
* *
* * *
* * * *
넓이: 8.0
```
