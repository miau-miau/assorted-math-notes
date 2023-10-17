---
tags:
  - number-theory
order-tag: "0042"
date: 2023-09-21
---
>[!definition]
>The **multiplicative inverse** of $a\;(\textnormal{mod }n)$ (if it exists) is the integer $b\;(\textnormal{mod }n)$ satisfying $ab\equiv 1\;(\textnormal{mod }n)$.
>>[!example]
>>$2$ and $3$ are inverses $(\textnormal{mod }5)$ since $2(3)=6\equiv 1\;(\textnormal{mod }5)$.

Finding multiplicative inverse of $a\;(\textnormal{mod }n)$ amounts to [[solving-congruence-equations|solving]] $ax\equiv 1\;(\textnormal{mod }n)$.

#### Proposition (existence of inverse)
$ax\equiv 1\;(\textnormal{mod }n)$ has a solution of and only if $\textnormal{gcd}(a,n)=1$.
##### Proof
$(\leftarrow)$ Since $\textnormal{gcd}(a,n)=1$, by [[linear-combination-of-gcd|Bezout's lemma]], $\exists\;x,y\in\mathbb{Z}$ such that $1=xa+yn$, or $ny=1-ax$.
So $n|1-xa$. Hence $ax\equiv 1\;(\textnormal{mod }n)$.
($\rightarrow$) Since $ax\equiv 1\;(\textnormal{mod }n)$, $xa-1=yn\textnormal{ for some }y\in\mathbb{Z}\implies xa-yn=1\implies \textnormal{gcd}(a,n)=1$.

>[!note]
>By the proof, to find the inverse of $a\;(\textnormal{mod }n)$. simply solve $1=xa+yn$. Then $x$ is the inverse.

