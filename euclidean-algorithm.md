---
tags:
  - number-theory
  - algorithms
order-tag: "0033"
date: 2023-09-12
aliases:
  - Euclidean Algorithm
---
#### Lemma
$$\textnormal{If }a=qb+r,\textnormal{ then }gcd(a,b)=gcd(b,r)$$
(see [[greatest-common-divisor|gcd]]).
##### Proof
Let $g_{1}=gcd(a,b)$ and $g_{2}=gcd(b,r)$.
By definition, $g_{2}|b$ and $g_{2}|r$.
By [[basic-division#Proposition|proposition]], $g_{2}|(qb+r)$. Hence $g_{2}|a$.
Now, $g_{2}|a$ and $g_{2}|b\to g_{2}\leq g_{1}$.
Similarly, $g_{1}|b$ and $g_{1}|r\to g_{1}\leq g_{2}$.
$g_{2}\leq g_{1},g_{2}\leq g_{1}\to g_{1}=g_{2}$.

#### Euclidean [[algorithms-introduction|Algorithm]]
Let $a, b \in \mathbb{N}$ and $a<b$. By [[division-algorithm|division algorithm]]:
$a=q_{1}b+r_{1}$ and $0\leq r_{1}\leq b$
If $r_{1}\neq 0$, apply it to $b$ and $r$:    $b=q_{2}r_{1}+r_{2}$ ($0\leq r_{2}<r_{1}$)
If $r_{2}\neq 0$, apply it to $r_{1}$ and $r_{2}$: $r_{1}= q_{3}r_{2}+r_{3}$ ($0\leq r_{3}<r_{2}$)
$$
\dots
$$
Continue until remainder is $0$:
$$r_{k-2}=q_{k}r_{k-1}+r_{k}$$$$r_{k-1}=q_{k+1}r_{k}+0$$
By lemma,  $$
gcd(a,b)=gcd(b,r_{1})=gcd(r_{1},r_{2})=\dots=gcd(r_{k},0)=r_{k}
$$
>[!example]
>Find $gcd(630,196)$.
>$630=3*196+42$
>$196=4*42+28$
>$42=1*28+14$
>$28=2*14+0$
