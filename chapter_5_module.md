# 모듈


## 모듈이란

모듈 = 프로그램의 꾸러미

### math 모듈

수학적인 계산 기능이 필요한 경우 math라는 모듈을 불러와서 사용할 수 있다.

```py
# 제곱근(square root) 구하기
>>> import math
>>> math.sqrt(2)
1.4142135623730951
>>> math.sqrt(3)
1.7320508075688772
>>> math.sqrt(4)
2.0
# 원주율 알아보기
>>> math.pi
3.141592653589793
```

### calendar 모듈

```py
# 달력 불러오기
>>> import calendar
>>> calendar.prmonth(2025, 3)
     March 2025
Mo Tu We Th Fr Sa Su
                1  2
 3  4  5  6  7  8  9
10 11 12 13 14 15 16
17 18 19 20 21 22 23
24 25 26 27 28 29 30
31
```

## 모듈 가져오기 (import)

```py
# 방법 1: 모듈 전체를 가져오는 경우
import 모듈
# 방법 2: 모듈 내 필요한 부분만 가져오는 경우
from 모듈 import 이름
```

## 모듈 지우기 (del)

불러온 모듈이 필요 없을 때, 필요없는 모듈을 지워준다. 프로그램을 짜다보면 여러 경우가 있으므로 알아두도록 하자.

```py
del 모듈
```

## 모듈 다시 불러오기 (reload)

한 번 임포트한 모듈을 다시 불러와야 할 때는 reload 할 수 있다.

```py
from importlib import reload
reload(모듈)
```

## 여러 가지 모듈

### sys

파이썬 인터프리터를 제어할 수 있다.

```py
# 파이썬 프롬프트를 변경하기 '>>> ' -> '^^;'
>>> import sys
>>> sys.ps1
'>>> '
>>> sys.ps1 = '^^;'
^^;print('hello')
hello
^^;5 * 3
15
^^;sys.ps1 = '>>> '
# 파이썬 인터프리터를 종료하기
>>> sys.exit()
Console closed.
```

### os

운영체제(OS: Operating System)를 제어할 수 있다.

```py
# 현재 작업 디렉터리(current working directory)를 알아보기
>>> import os
>>> os.getcwd()
'/home/.anon-1c2b182ca5b940d8a3cf7488'
# 이곳에 어떤 파일들이 있는지 알아보기
>>> os.listdir()
['.ipython', '.cache', '.profile', '.virtualenvs', '.bashrc', '.vimrc', '.python_history', '.pythonstartup
.py', '.gitconfig', 'README.txt', '.local']
# 상위 디렉터리로 이동하여 파일목록 출력하기
>>> os.chdir('..')
>>> os.getcwd()
'/home'
```

### re

정규 표현식(regular expression)을 이용해 문자열을 다룰 수 있다.

```py
# 현재 디렉토리에서 R 다음에 M이 나오는 파일명을 추출하기
>>> import re, glob
>>> p = re.compile('.*R.*M.*')
>>> for i in glob.glob('*'):
...     m = p.match(i)
...     if m:
...         print(m.group())
... 
README.txt
```

### webbrowser

```py
# 웹 브라우저를 기동하여 지정 웹사이트에 접속하기
import webbrowser
url='https://www.python.org/'
webbrowser.open(url)
```

### random

```py
>>> import random
# 난수 만들기 1 (0 이상 1 미만)
>>> random.random()
0.8109782013586663
# 난수 만들기 2 (1 이상 7 미만) 
>>> random.randrange(1,7)
6
# 시퀀스를 뒤죽박죽 섞어놓기
>>> abc = ['a', 'b', 'c', 'd', 'e']
>>> random.shuffle(abc)
>>> abc
['b', 'e', 'd', 'c', 'a']
# 아무 원소나 하나 뽑아주기
>>> abc = ['a', 'b', 'c', 'd', 'e']
>>> random.choice(abc)
'e'
```
