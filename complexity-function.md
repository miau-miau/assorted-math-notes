---
tags:
  - algorithms
order-tag: "0049"
date: 2023-09-26
aliases:
  - complexity function
---
>[!definition]
>The **complexity [[functions|function]]** $f:\mathbb{N}\to \mathbb{N}$ provides an upper bound for the number of operations to carry out an algorithm.
>
>>[!example]
>>The complexity of [[horners-algorithm|Horner's algorithm]] is $f(n)=2n$.

We don't always know the precise number of operations.

>[!example]
>Adding two natural numbers with $n$ digits.
>If this process does not include carryovers, then there are $n$ operations. But there can be at most $n-1$ carryovers. So, $f(n)=2n-1$.
>$$\begin{align*} &\phantom{+} 9\,9\,9 \\+ &\phantom{+} 1\,1\,1 \\
\hline
  &\,1\,1\,1\,0
\end{align*}$$
