---
tags:
  - algorithms
order-tag: "0047"
date: 2023-09-26
big-O: O(n)
storage: "1"
---
>[!task]
>Given $a_{0},a_{1},\dots,a_{n},\;x\in\mathbb{Z}$, output $a_{0}+a_{1}x+\dots+a_{n}x^n$.

#### Explanation
Note that we can factor:
$$
\begin{align}
&\quad\;a_{0}+(a_{1}+a_{2}x+\dots a_{n}x^{n-1})x \\
&=a_{0}+(a_{1}+(a_{2}+a_{3}x+\dots a_{n}x^{n-2})x)x \\
&=\dots \\
&=a_{0}+(a_{1}+(a_{2}+\dots(a_{n-1}+a_{n}x)x)\dots)x
\end{align}
$$
So the algorithm computes each of the terms from inside out:
$a_{n-1}+a_{n}x,\;a_{n-1}+(a_{n-1}+a_{n}x)x, \dots$

#### Algorithm
1. Set $S=a_{n}$
2. For $i=1$ to $n$, replace $S$ by $a_{n-i}+Sx$
3. Output S.

Requires $2n$ computations and no storage requirements.