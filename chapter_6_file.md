# 파일

파일의 내용을 읽고 쓸 수 있다.

## 읽기 (read)
```py
# 파일 목록 중 README.md 파일을 불러와서 출력하기
>>> os.listdir()
['.ipython', '.cache', '.profile', '.virtualenvs', '.bashrc', '.vimrc', '.python_history', '.pythonstartup
.py', '.gitconfig', 'README.txt', '.local']
>>> f = open('README.txt')
>>> f.read()
'# vim: set ft=rst:\n\nSee https://help.pythonanywhere.com/ (or click the "Help" link at the top\nright) f
or help on how to use PythonAnywhere, including tips on copying and\npasting from consoles, and writing yo
ur own web applications.\n'
```

## 쓰기 (write)

```py
# 'w' 는 파일에 데이터를 쓰겠다는 선언
# 'a+' 는 파일에 데이터를 지우지 않고 내용을 추가하겠다는 선언
>>> letter = open('letter.txt', 'w')
>>> letter.write('Dear Father,')
12
>>> letter.close()
>>> os.listdir()
['.ipython', 'letter.txt', '.cache', '.profile', '.virtualenvs', '.bashrc', '.vimrc', '.python_history', '
.pythonstartup.py', '.gitconfig', 'README.txt', '.local']
>>> f = open('letter.txt')
>>> f.read()
'Dear Father,'
```
