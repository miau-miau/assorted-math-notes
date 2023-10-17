---
tags:
  - number-theory
order-tag: "0044"
date: 2023-09-21
---
Let $n_{1},\dots,n_{k}$ be pairwise [[greatest-common-divisor#^3ec34f|relatively prime]]. Then the system
$$
\begin{align}
x\equiv a_{1}\;(\textnormal{mod }n_{1}) \\
x\equiv a_{2}\;(\textnormal{mod }n_{2}) \\
\dots \\
x\equiv a_{k}\;(\textnormal{mod }n_{k})
\end{align}
$$
has a unique solution $\;(\textnormal{mod }n_{1}\dots n_{k})$.

>[!warning]
>If moduli are not relatively prime, there might not be a solution.

#### Solving
We will focus in the case of two congruences:
$$
\begin{align}
x\equiv a_{1}\;(\textnormal{mod }n_{1}) \\
x\equiv a_{2}\;(\textnormal{mod }n_{2})
\end{align}
$$
To find a solution:
1. [[solving-congruences-with-inverse|Find]] $y,z\in\mathbb{Z}$ such that $1=yn_{1}+zn_{2}$ (this is possible since $\textnormal{gcd}(n_{1},n_{2})=1$).
2. The the solution is $a_{2}yn_{1}+a_{1}zn_{2}\;(\textnormal{mod }n_{1}n_{2})$.

Check:
- $a_{2}yn_{1}+a_{1}zn_{2}\equiv a_{1}zn_{2}\;(\textnormal{mod }n_{1})\equiv a_{1}(1-yn_{1})\equiv a_{1}\;(\textnormal{mod }n_{1})$.
- $a_{2}yn_{1}+a_{1}zn_{2}\equiv a_{2}yn_{1}\;(\textnormal{mod }n_{2})\equiv a_{2}(1-zn_{2})\equiv a_{2}\;(\textnormal{mod }n_{2})$.

>[!example]
>$x\equiv 2\;(\textnormal{mod }4)$ and $x\equiv 6\;(\textnormal{mod }7)$. Find $x$.
>>Since $\textnormal{gcd}(4,7)=1, \;1=4y+7z\textnormal{ for some }x,y\in\mathbb{Z}$. We find $y$ and $z$ to be $y=2,\,z=-1$. So $6(4)(2)+2(7)(-1)=34$ is a solution.
>>By theorem, $x$ is unique $\;(\textnormal{mod }28)$. So $x\equiv 6 \;(\textnormal{mod }28)$.

>[!example]- More examples
>An integer $x$ between $100$ and $500$ has a remainder of $4$ when divided by $12$ and a remainder of $15$ when divided by $25$. What is $x$?
>>We need to solve
>>$$\begin{align} x\equiv 4\;(\textnormal{mod }12) \\ x\equiv 15\;(\textnormal{mod }25) \end{align}$$
>>First, solve $1=12x+25y$ for $x$ and $y$.
>>Since $1=12(-2)+25(1)$, $15(12)(-2)+4(25)(1)=-260$ is a solution.
>>[[congruence#Reduction|Reducing]] $\;(\textnormal{mod }300)$ gives $-260\;(\textnormal{mod }300)\equiv 40$.
>>Since $100\leq x\leq 500$ and congruent to $40\;(\textnormal{mod }300)$, $x=340$.
