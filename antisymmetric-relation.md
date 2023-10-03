---
tags:
  - sets
  - naive-set-theory
order-tag: "0015"
date: 2023-08-31
---
>[!definition]
>A [[binary-relation|binary relation]] on $A$ is **antisymmetric** if
>$$(a,b)\in R \land (b,a)\in R\to a=b$$
>More intuitively,
>if $a\neq b$, then $(a,b)$ and $(b,a)$ are not both in $R$.
>
>>[!example]
>>$A=\{$ people in the world $\}$
>>- $R=\{ (a,b)\in A\times A\mid a$ is related to $b\}$ is [[symmetric-relation|symmetric]] since
>>$(a,b)\in R\to a$ is related to $b$
>>$\to b$ is related to $a$
>>$\to(b,a)\in R$.
>>- $R = \{ (a,b)\in A\times A\mid a$ is a parent of $b\}$ is antisymmetric since
>>$(a,b)\in R\to a$ is a parent of $b$
>>$\to b$ is not a parent of $a$
>>$\to(b,a)\notin R$.

>[!example]- More examples
>- $R=\{ (x,y)\in\mathbb{R}\mid x\leq y \}$ is antisymmetric, since
>$(a,b),(b,a)\in R\to a\leq b\land b\geq a\to a=b$.
>- $R=\{ (x,y)\in\mathbb{R}\mid x^{2}+y^{2}=1 \}$ is not antisymmetric, since
>$(1,0),(0,1)\in R$, but $(1,0)\neq(0,1)$.
#### Symmetric vs. Antisymmetric

>[!warning]
>These are not disjoint notions. $R$ can be both antisymmetric and symmetric or neither.
>>[!example]
>>- $R=\{ (x,y)\in \mathbb{R}\mid x=y \}$ is both.
>>*symmetric*: $(x,y)\in R\to x=y\to y=x\to(y,x)\in R$
>>*antisymmetric*: $(x,y),(y,x)\in R\to x=y$.
>>- $R=\{ (1,1),(1,2),(2,1),(3,1) \}\subset \mathbb{Z}^{2} \}$ is neither.
>>*not symmetric*: $(3,1)\in R$, but $(1,3)\notin R$
>>*not antisymmetric*: $(1,2),(2,1)\in R$, but $1\neq 2$.

