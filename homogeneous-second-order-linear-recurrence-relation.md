---
tags:
  - sequences-and-series
order-tag: "0060"
date: 2023-10-03
---
>[!definition]
>A **homogeneous second-order linear [[recursively-defined-sequence|recurrence]] relation** has a form
>$$a_{n}=ra_{n-1}+sa_{n-2},$$
>where $r$ and $s$ are constants.
>>[!example]
>>The [[fibonacci-sequence|Fibonacci Sequence]] is a homogeneous second-order recurrence relation.

Such a recurrence can be rewritten in the form:
$$a_{n}-ra_{n-1}-sa_{n-2}=0$$
>[!definition]
>The associated polynomial
>$$x^{2}-rx-s$$
>is called **characteristic polynomial**.
>It's roots are called **characteristic roots**.
>>[!example]
>>The recurrence relation
>>$$a_{n}=5a_{n-1}-6a_{n-2}$$
>>has a characteristic polynomial
>>$$x^{2}-5x+6$$
>>Its roots are $x=2,3$ since $x^{2}-5x+6=0 \implies x=2,3$.

