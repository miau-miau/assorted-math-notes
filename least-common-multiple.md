---
tags:
  - number-theory
order-tag: "0036"
date: 2023-09-14
aliases:
  - lcm
---
>[!definition]
>If $a,b\in\mathbb{Z}\setminus\{0\}$, then **the least common multiple** of $a$ and $b$ ($lcm(a,b)$) is the positive integer satisfying:
>1. $a|l\textnormal{ and }b|l$
>2. $\textnormal{if }a|m\textnormal{ and }b|m,\textnormal{ then }m\geq l$.
>
>>[!example]-
>>$lcm(6,9)=18$
>>$lcm(-6,9)=18$
>>$lcm(2,3)=6$

Since $\mid ab\mid$ is a common multiple of $a$ and $b$, $lcm(a,b)\leq\mid ab\mid$.

#### Proposition
$$\textnormal{If }a\textnormal{ and }b\textnormal{ are relatively prime, then }lcm(a,b)=\mid ab\mid$$
##### Proof
We know that $lcm(a,b)\leq\mid ab\mid$. So we need only show that $\mid ab\mid\leq lcm(a,b)$. Let $l=lcm(a,b)$. By definition, $a|l$ and $b|l$. Hence, $\\\exists k_{1},k_{2}\in\mathbb{Z}$ such that $l=k_{1}a$ and $l=k_{2}b$. Since $gcd(a,b)=1$, $\\\exists m,n\in\mathbb{Z}$ such that $1=am+bn$ (by [[linear-combination-of-gcd|Bezout's lemma]]). Multiplying by $l$ gives $$l=aml+bnl=am(k_{2}b)+bn(k_{1}a)=ab(mk_{2}+nk_{1}).$$
Thus, $ab|l\implies\mid ab\mid|l\implies\mid ab\mid\leq l$.

#### General equation
$$
lcm(a,b)=\frac{\mid ab\mid}{gcd(a,b)}
$$
##### Proof
Let $g=gcd(a,b)$ and $l=lcm(a,b)$.
Since $g|a$, $\\\exists m\in\mathbb{Z},\quad a=mg$.
Since $g|b$, $\\\exists n\in\mathbb{Z},\quad b=ng$.
Then $l=lcm(mg,ng)\implies mg|l\implies g|l\implies\\\exists k\in\mathbb{Z}, \quad l=gk$.
Since $mg|gmn$ and $ng|gmn$, $$lcm(mg,ng)=l=gk\leq gmn\implies k\leq mn.$$On the other hand, $mg|l\implies mg|gk\implies m|k$, and similarly, $n|k$. But $m,n$ are coprime, [[gcd-facts#Proposition (coprime divisibility)|which means]] that $mn|k$. Therefore, $k\geq mn.$
Thus, $k=mn\implies lcm(a,b)=gmn$.
$$
\frac{\mid ab\mid}{gcd(a,b)}=\frac{mg*ng}{g}=gmn=lcm(a,b).
$$
