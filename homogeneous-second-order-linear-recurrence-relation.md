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

#### Theorem (characteristic roots)
Let $x^{2}-rx-s$ have roots $x_{1}$ and $x_{2}$. The the recurrence relation
$$
a_{n}=ra_{n-1}+sa_{n-1},\;n\geq 2
$$
has $n^{\textnormal{th}}$ term:
$$
\left\{
\begin{array}{ll}
    c_{1}x_{1}^n+c_{2}x_{2}^n & \text{if } x_{1}\neq x_{2} \\
    c_{1}x^n+c_{2}nx^n & \text{if } x_{1}=x_{2}=x \\
\end{array}
\right.
$$
where $c_{1}$ and $c_{2}$ are determined by initial conditions.

>[!example]
>Consider the recurrence relation
>$$a_{0}=-3,\,a_{1}=2,\,a_{n}=5a_{n-1}-6a_{n-2}$$
>We know $x_{1}=2$ and $x_{2}=3$.
>Thus $a_{n}=c_{1}2^n+c_{2}3^n$.
>What is $c_{1}$ and $c_{2}$?
>When $n=0,\,n=1$:
>
>$$
>\begin{align}
a_{0}&=c_{1}+c_{2}=-3 \\
a_{1}&=2c_{1}+3c_{2}=2 \\
\implies c_{1}&=-11 \textnormal{ and } c_{2}=8
\end{align}
>$$
>So $a_{n}=-11(2^n)+8(3^n)$.

>[!example] Fibonacci Sequence
>A similar computation gives the formula for the Fibonacci Sequence:
>$$f_{n}=\frac{1}{\sqrt{ 5 }}\left( \frac{1+\sqrt{ 5 }}{2} \right)^{n+1}-\frac{1}{\sqrt{ 5 }}\left( \frac{1-\sqrt{ 5 }}{2} \right)^{n+1}$$
