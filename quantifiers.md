---
tags:
  - logic
order-tag: "0003"
aliases: 
date: 2023-08-22
---
#### There exists (existential quantifier)
There exists $\\\exists$ stipulates the existence of an element for which a statement is true.

>[!example]
>- $\\\exists$ a smallest positive integer.
>- Some polynomials have no roots ($\\\exists$ a polynomial with no roots)
>- $\\\exists x\mid x^{2}-2x+1=0$

#### For all (universal quantifier)
Universal quantifier can be read as "for all", "for any" or "for each" and is denoted by $\forall$.

>[!example]
>- $\forall x\in\mathbb{R}\quad x^{2}+1>0$
>- For any integer $n$, $2n$ is even ($\forall n\in\mathbb{Z}\quad 2n$ is even).


#### Negating quantifiers
[[negation-of-logic-statements|Negating]] a $\\\exists$ gives a $\forall$ statement (and vice versa).
$$
\neg(\forall p, q)=\\\exists p\mid\neg q
$$
$$
\neg(\\\exists p \mid q) = \forall p,\neg q
$$
>[!example]
>- Negation of "$\forall$ real numbers $x$, $x^{2}+1>0$" is "$\\\exists$ real number $x$ such that $x^{2}+1\leq 0$"
>- Negation of "$\\\exists$" $a$ and $b$ such that $ab\neq ba$ is "$\forall$ $a$ and $b$, $ab=ba$".

