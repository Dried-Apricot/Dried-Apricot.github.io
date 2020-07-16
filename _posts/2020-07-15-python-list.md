---
title: "List"
date: 2020-07-15 11:23
categories: python3 algorithm
---

|연산|결과|비고|
|---|---|---|
|`s = []`|s=[]|_len_ = {int} 0 이 된다.|
|`s = [1,2,3]`| s=[1,2,3] |원소는 컴마로 구분|
|`s = [x for x in range(1,3)]`| s = [1,2,3] |복잡한 선언 가능|

*원문에 [x for x in **iterable**] 라는 말이 나오는데 파이썬에서 iterable 을 정의하는 방식에 대해 정리할 필요가 있음.*

[출처:파이썬 공식 docs](https://docs.python.org/3/library/stdtypes.html#list)

#### Common Sequence Operation

List 뿐만 아니라 Sequences 에 적용 가능한 연산이다.


s와 t는 같은 타입의 sequences이고,
x 는 대수이다.

|연산|결과|비고|
|---|---|---|
|`x in s`|만약 s 의 item이 x와 같으면 `True` 다르면 `False`|내용 검출해주는 연산 |
|`x not in s`|만약 s 의 item이 x와 같으면 `False` 다르면 `True`||
|`s + t`|s 뒤에 t 붙이는 연산|예를 들어 s=[1],t=[2]라면 s+t = [1,2]|
|`del s[i:j]`|s[i:j] = [] 와 같은 연산이다|길이가 짧아지고, indedx 도 자연스럽게 내려옴.|
|`s[i:j:k] = t`| s[i:j:k]의 item이 t로 대체된다.|*iterable 정리 필요...*|

[출처: 파이썬 공식 docs](https://docs.python.org/3/library/stdtypes.html#typesseq-common)
#### Mutable Sequence Operation
List 뿐만 아니라 Mutable Sequences 에 적용 가능한 연산이다.

`s[0] = 1`

[출처: 파이썬 공식 docs](https://docs.python.org/3/library/stdtypes.html#typesseq-mutable)

*작성 중*
