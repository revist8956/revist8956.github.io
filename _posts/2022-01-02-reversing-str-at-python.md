---
layout: post
title: -[Python] 거꾸로 출력하기
date: 2022-01-02 16:00 +0800
tags: [python, grammar]
categories: python
toc:  true
comments: true
---

## 문자열 거꾸로 출력하기 (+ 리스트, 튜플)
  

문자열을 거꾸로 출력하는 방식은 다양하다.   
예를 들어 "안녕하세요" 라는 문자열을 "요세하녕안"으로 바꾸고 싶다고 가정하자.  
<br>
가장 기본적으로 for문을 사용하는 경우가 있다.

```
a = '안녕하세요'
a_reverse = ''   # 역순으로 담아줄 빈 문자열 생성

for i in a:
	a_reverse = i + a_reverse

print(a_reverse)   # 요세하녕안
```
<br>
파이썬에서는 거꾸로 출력하는 함수를 제공하기도 한다.

```
a = '안녕하세요'
print(reversed(a))      # iterator 객체로 반환

print("".join(reversed(a)))   #요세하녕안
```
문자열에서 reversed 함수를 사용하려면 join과 함께 사용하여야 한다.
<sub>+) reverse 함수는 list 형식에서만 가능</sub>
  
<br>
<br>
하지만 slicing을 통해서 더욱 간편하게 만들 수도 있다.

```
a = '안녕하세요'
print(a[::-1])     #요세하녕안
```
<hr>
* reversed 함수는 `str`뿐만 아니라 리스트, 튜플에도 사용할 수 있다.

```
a = [1,2,3]     # 리스트
b = (1,2,3)     # 튜플

print(list(reversed(a)))      # [3,2,1]
print(tuple(reversed(a)))     # (3,2,1)

print(a)					# 원형은 바뀌지 않는다.
print(b)					# 원형은 바뀌지 않는다.
```

* `[::-1]` 인덱스 역시 리스트, 튜플에도 사용할 수 있다.

```
li = ['a', 'b', 'c', 'd', 'e']
tu = ('a', 'b', 'c', 'd')

print(li[::-1])          # ['e', 'd', 'c', 'b', 'a']
print(tu[::-1])          # ('d', 'c', 'b', 'a')
```

