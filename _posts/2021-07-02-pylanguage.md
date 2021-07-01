---
title:  "파이썬 용어"
excerpt: "파이썬 사전을 볼 때 쓰이는 용어를 정리"

categories:
  - Blog
tags:
  - [Blog, TIL, 생각]

toc: true
toc_sticky: true
 
date: 2021-07-02
last_modified_at: 2021-07-02


---

## 파이썬 용어

```iterable``` *(이터러블)* : **member**를 한 번에 하나씩 차례로 반환이 가능한 object를 말한다.

ex> list, str, tuple, dict

`iterator` *(이터레이터)* : next() 메소드로 데이터를 순차적으로 호출 가능한 object를 말한다.

`iterable`한 object라고 해서 무조건 `iterator`가 아니다.

**예제1**

```python
arr = ['a', 'b', 'c']
next(arr)
```

**결과**

```python
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: list object is not an iterator
```

**Solution**

```python
arr = iter(arr) # <type 'listiterator'>
next(arr)
# a

next(arr)
# b

next(arr)
# c

next(arr)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
StopIteration
```

- iter(호출가능한객체, 반복을끌낼값)  : 반복을 끝낼 값을 지정하면 특정 값이 나올 때 반복을 끝내는 함수
- next(반복가능한객체, 기본값) : 기본값을 지정할 수 있고 지정한다면 `stopIteration`이 발생하지 않고 기본값을 출력하는 함수 



`Sequence` : 여러 객체를 저장하는 자료형. 각 객체에 **순서**를 지닌다. int  인덱스를 통해, 원소에 접근할 수 있는 iterable.

ex> list, str, tuple

`packing`  : 인자로 받은 **여려개의 값을 하나의 객체**로 합쳐셔 받을 수 있도록 하는 것.

**예제**

```python
def func(*args):
      print(args)
      print(type(args))
    
func(1, 2, 3, 4, 5, 6, 'a', 'b')
```

**결과**

```python
(1, 2, 3, 4, 5, 6, 'a', 'b')
<class 'tuple'>
```

`unpacking` : 여러개의 객체를 포함하고 있는 하나의 객체를 풀어주는 것.

**예제**

```python
a = 7
b = 5
print(*divmod(7,5))
```

**결과**

```python
1 2
```

