---
tags:
  - algorithms
order-tag: "0050"
date: 2023-09-26
aliases:
  - Big O
---
>[!definition]
>Let $f,g:\mathbb{N}\to \mathbb{N}$. We write $f=O(g)$ (say $f$ is Big O of $g$) if
>$$\exists\,n_{0}\in\mathbb{Z}\textnormal{ and }c\in\mathbb{R}^+\textnormal{ such that } |f(n)|\leq c| g(n)|\quad\forall n\geq n_{0}$$
>
>>[!example]
>>Let $f(n)=n^3$ and $g(n)=15n^3$. Then $f=O(g)$ and $g=O(f)$.
>>- $|f(n)|+|n^3|\leq 15|n^{3}|=|g(n)|\quad\forall n\in\mathbb{Z}$
>>So $n_{0}=1,\;c=1$.
>>- $|g(n)|=|15n^3|=15|f(n)|\quad\forall n\in\mathbb{Z}$
>>So $n_{0}=1,\;c=15$.
>

>[!example]- More examples
>Let $f(n)=n+1$ and $g(n)=n^{2}$. Notice that for $n\geq 1,$
>$$f(n)=n+1\leq n+n=2n\leq 2n^{2}$$
>Thus taking $n_{0}=1$ and $c=2$, we have $f(n)=cg(n)\quad\forall \geq n_{0}\implies f=O(g)$.
>
>However, $g\neq O(f)$.
>Let's prove this by [[proofs#Proof by Contradiction|contradiction]].
>Assume $\exists\,n_{0}\in\mathbb{Z}^+$ and $c\in\mathbb{R}$ such tat $n^{2}\leq c(n+1)\quad n\geq n_{0}$.
>Diving by $n$ gives
>$$n^{2}\leq c\left( 1+\frac{1}{n} \right)\leq 2c\quad \forall \geq n_{0}$$
>But this is not possible since $c$ is a constant and $n$ can be arbitrarily large. Thus $g\neq O(f)$.

