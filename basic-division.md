---
tags:
  - number-theory
order-tag: "0031"
date: 2023-09-12
---
>[!definition]
>Given $a,b\in\mathbb{Z}, b\neq 0$, we say $b$ is a **divisor** of $a$ if and only if $a=bq$ for some $q\in\mathbb{Z}$. We write $b|a$.
#### Proposition (partial order)
Let $R=\{(a,b)\in\mathbb{N}\mid b|a\}$. Then $R$ is [[reflexive-relation|reflexive]], [[antisymmetric-relation|antisymmetric]], and [[transitive-relation|transitive]].
- $a|a\quad\forall a\in\mathbb{N}$
- $a|b\textnormal{ and }b|a\to a=b$
- $a|b\textnormal{ and }b|c\to a|c$ 
#### Proposition
$$\textnormal{If }c|a\textnormal{ and }c|b,\textnormal{ then }c|(xa+yb)\quad\forall x,y\in\mathbb{Z}$$
##### Proof
$c|a$ and $c|b\to a=kc$ and $b=lc$. Therefore,
$$xa+yb=x(kc)+y(lc)=c(xk+yl)\to c|(xa+yb).$$
