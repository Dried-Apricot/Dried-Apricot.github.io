---
title: "List"
date: 2020-07-20 19:38
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


(List, tuple, range)


s와 t는 같은 타입의 sequences이고,
x 는 대수이다.


|연산|결과|비고|
|---|           ---|---|
|`x in s`| 만약 s 의 item이 x와 같으면 `True` 다르면 `False`|      내용 검출해주는 연산 |
|`x not in s`|만약 s 의 item이 x와 같으면 `False` 다르면 `True`||
|`s + t`|s 뒤에 t 붙이는 연산                              |예를 들어 s=[1],t=[2]라면 s+t = [1,2]|
|`s * n` or `n * s`|각각의 item에 n을 곱하는 연산||
|`s[i]`|0부터 시작해 s의 i번째 item||
|`s[i:j]`|s의 i이상 j미만 자른 결과|j번째 아이템은 미포함|
|`s[i:j:k]`|s의 i이상 j미만 k 단위로 자른 결과||
|`len(s)`|s의 길이||
|`min(s)`|s중 가장 작은 item||
|`max(s)`|s중 가장 큰 item||
|`s.index(x[, i[, j]])`|*파이썬 3.8.4 메뉴얼에 있지만, 파이썬 3.5 기준으로 syntax error 발생 중. 신기능으로 보임.*||
|`s.count(x)`|s 안의 x 개수||


[출처: 파이썬 공식 docs](https://docs.python.org/3/library/stdtypes.html#typesseq-common)

#### Mutable Sequence Operation
List 뿐만 아니라 Mutable Sequences 에 적용 가능한 연산이다.



|연산|결과|비고|
|---|           ---|---|
|`s[i] = x`|||
|`s[i:j] = t`|||
|`del s[i:j]`|s[i:j] = [] 와 같은 연산이다                 |길이가 짧아지고, indedx 도 자연스럽게 내려옴.|
|`s[i:j:k] = t`| s[i:j:k]의 item이 t로 대체된다. 
|`s.append(x)`|s의 마지막에 x가 추가된다.|s의 크기와 상관 없이 추가된다.|
|`s.clear()`|s를 비운다.||
|`s.copy()`|s를 복제한다?|*언제쓰는 것인지 모르겠음. 그냥 a = s 도 되는데.*|
|`s.extend(t)` or `s +=t`|s 뒤에 t를 붙인다.||
|`s *= n`|n번 만큼 s를 반복하여 뒤에 이음||
|`s.insert(i,x)`|i 번째 아이탬에 x 추가|i+1 번 이후 아이탬은 모두 한 칸씩 뒤로 밀린다.|
|`s.pop([i])`|i 번째 아이탬을 pop 연산|return 및 삭제|
|`s.remove(x)`|s안에 있는 아이템이 x이면 지운다.|[0]부터 검출하여 가장 먼저 만나는 아이탬 삭제. s의 길이가 줄어든다.|
|`s.reverse()`|s 아이템의 배열 순서를 바꾼다.||


[출처: 파이썬 공식 docs](https://docs.python.org/3/library/stdtypes.html#typesseq-mutable)


확실히 파이썬은 C언어보다 다양한 기능을 지원한다.
아무래도 n 복잡도의 연산을 다 지원하기로 마음 먹은 것처럼 만들어져있다.

tuple 및 range 도 정리해보자.