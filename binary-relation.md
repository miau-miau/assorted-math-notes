---
tags:
  - set-theory
order-tag: "0012"
date: 2023-08-31
---
>[!definition]
>Let $A$ be a set. A **binary relation** on $A$ is a [[sets-naive#Subsets|subset]] of $A\times A$ (see [[cartesian-product-sets|cartesian product]]).
>
>>[!example]
>>Let $A=\{ 1,2 \}, A\times A=\{ (1,1),(1,2),(2,1),(2,2) \}$.
>>$R=\{ (1,1),(1,2) \}$ is a binary relation on $A$

>[!example]- More examples
>- Let $A=\mathbb{R}$. Then $R=\{ (x,y)\in\mathbb{R}^{2}\mid x\leq y \}$ is a binary relation on $\mathbb{R}$ (it "relates" pairs of elements of $\mathbb{R}$).
>- Let $A=\mathbb{Z}$. Then $R=\left\{  (a,b)\in \mathbb{Z}^{2}\mid \frac{a}{b}\in\mathbb{Z} \right\}$ is a binary relation on $\mathbb{Z}$.

More generally, 
>[!definition]
>A **binary relation** from $A$ to $B$ is a subset of $A\times B$.
>
>>[!examples]
>>$A=\{ \textnormal{ baseball players } \}$
>>$B=\mathbb{N}\cup \{ 0 \} = \textnormal{nonnegative integers}$
>>$R=\{ (a,b)\in A\times B\mid a \textnormal{ has } b \textnormal{ homeruns} \}$
>>$(\textnormal{Albert Pujols}, 703)\in R$.

