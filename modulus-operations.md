---
tags:
  - number-theory
order-tag: "0038"
date: 2023-09-19
---
Let $a\equiv x\;(\textnormal{mod }n)$ and $b\equiv y\;(\textnormal{mod }n)$.
(see [[congruence]])

#### Addition
$$a+b\equiv x+y\;(\textnormal{mod }n)$$
##### Proof
$a\equiv x\;(\textnormal{mod }n)\textnormal{ and }b\equiv y\;(\textnormal{mod }n)$
$\to n|a-x \textnormal{ and } n|b-y$
$\to n|(a-x)+(b-y)$ (see [[basic-division#Proposition|proposition]])
$\to n|(a+b)-(x-y)$
$\to a+b\equiv x+y\;(\textnormal{mod }n)$

#### Multiplication
$$ab\equiv xy\;(\textnormal{mod }n)$$
##### Proof
$a\equiv x\;(\textnormal{mod }n)\textnormal{ and }b\equiv y\;(\textnormal{mod }n)$
$\to n|a-x \textnormal{ and } n|b-y$
$\to n|b(a-x)+x(b-y)$ (see [[basic-division#Proposition|proposition]])
$\to n|ab-bx+bx-xy$
$\to n|ab-xy$
$\to ab\equiv xy\;(\textnormal{mod }n)$

>[!note]
>These operations are helpful to [[congruence#Reduction|reduce]] $\textnormal{mod }n$ as you go.

#### Division

>[!warning]
>We cannot simply divide both sides by any number.
>
>>[!example]
>>$28\equiv 16\;(\textnormal{mod }12)$, but $14\not\equiv 8\;(\textnormal{mod }12)$

However, we can divide with some additional conditions.

#### Proposition (relatively prime modulus)
$$
\textnormal{If }ac\equiv bc\;(\textnormal{mod }n)\textnormal{ and } gcd(c,n)=1,\textnormal{ then } a\equiv b\;(\textnormal{mod }n)
$$
##### Proof
Since $ac\equiv bc\;(\textnormal{mod }n)$, we have that $n|ac-bc$, or $n|c(a-b)$.
Since $gcd(n,c)=1$, by a [[gcd-facts#Proposition (coprime divisibility)|proposition]], $n|a-b$.
Hence $a\equiv b\;(\textnormal{mod }n)$.

#### Proposition (diving the modulus)
$$
\textnormal{If }ac\equiv bc\;(\textnormal{mod }nc),\textnormal{ then } a\equiv b\;(\textnormal{mod }n)$$
>[!example]
>Back to our example with $28\equiv 16\;(\textnormal{mod }12)$.
>If we want to divide by $2$, we must also divide the modulus by $2$ to get a valid congruence:
>$14\equiv 8\;(\textnormal{mod }6)$ ✅
##### Proof
Since $ac\equiv bc\;(\textnormal{mod }nc)$, $nc|ac-bc$.
Therefore, $nc=k(ac-bc)$ for some $k\in\mathbb{Z}$.
Diving by $c$ gives $n=k(a-b)$, so $n|a-b$.
Thus $a\equiv b\;(\textnormal{mod }n)$.