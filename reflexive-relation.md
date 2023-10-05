---
tags:
  - set-theory
order-tag: "0013"
date: 2023-08-31
---
>[!definition]
>A [[binary-relation|binary relation]] on $A$ is **reflexive** if
>$$(a,a)\in R\quad\forall a\in R$$
>
>>[!example]
>>$A=\{ 1,2 \}$
>>$R_{1}=\{ (1,1),(1,2) \}$ is not reflexive since $(2,2)\notin R_{1}$.
>>$R_{2}=\{ (1,1),(1,2),(2,2) \}$ is reflexive.

>[!example]- More examples
>- $R=\{ (x,y)\in\mathbb{R}^{2}\mid x=y \}$ is reflexive, since
>$\forall a\in\mathbb{R}\quad a=a\to \forall a\in\mathbb{R},(a,a)\in R$.
>- $R=\{ (x,y)\in\mathbb{R}^{2}\mid y=x^{2}\}$ is not reflexive since $(2,2)\notin \mathbb{R}$.
>- $R=\{ (x,y)\in\mathbb{R}^{2}\mid x\leq y \}$ is reflexive since
>$\forall a\in\mathbb{R}\quad a\leq a\to\forall a\in\mathbb{R},(a,a)\in R$.

