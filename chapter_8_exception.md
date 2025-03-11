# 예외

## 예외처리 (try, except)

```py
>>> def f(a, b):
...     try:
...         if a and b:
...             return (a * b) + (a / b)
...         elif a:
...             return '불능'
...         else:
...             return '부정'
...     except:
...         return '똑 바로 살아라'
... 
>>> f(10, 6)
61.666666666666664
>>> f('십', '육')
'똑 바로 살아라'
```

