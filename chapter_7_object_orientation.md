# 객체지향

## 클래스 (class)

```py
>>> class Singer:
...     def sing(self):
...         return "Lalala~"
... 
>>> taeji = Singer()
>>> taeji.sing()
```

### 클래스 상속

```py
# ch07-3.py
class Person:
    eyes = 2
    nose = 1
    mouth = 1
    ears = 2
    arms = 2
    legs = 2

    def eat(self):
        print('얌냠...')

    def sleep(self):
        print('쿨쿨...')

    def talk(self):
        print('주절주절...')

class Student(Person): # Person 클래스를 상속받음
    def study(self):
        print('열공열공...')

lee = Person()
print('=== lee ===')
print(lee.mouth)

lee.talk()

kim = Student()
print('=== kim ===')
print(kim.mouth)
kim.talk()
kim.study()
```

```cmd
> python .\ch07-3.py
=== lee ===
1
주절주절...
=== kim ===
1
주절주절...
열공열공...
```

## 특별한 메서드들

### __init__ 메서드 (생성자)

객체가 생성될 때 호출된다.

```py
# bookstore.py
class Book:
    # 생략
    def __init__(self):
        print('책 객체를 새로 만들었어요~')
```

### __del__ 메서드 (소멸자)

생성자와 반대로 객체가 소멸될 때 호출된다.
