---
tags:
  - functions-and-maps
order-tag: "0027"
date: 2023-09-07
---
>[!definition]
>If $f:A\to B$ and $g:B\to C$ are [[functions]], then the **composition of $f$ and $f$** if
>$$g\circ f:A\to C,\textnormal{ given by } (g\circ f)(x)=g(f(x))$$
>
>>[!example]
>>$f(x)=2x-3,\;g(x)=x^{2}+1$
>>- $(g\circ f)(x)=g(f(x))=g(2x-3)=(2x-3)^{2}+1=4x^{2}-12x+10$
>>- $(f\circ g)(x)=f(g(x))=f(x^{2}+1)=2(x^{2}+1)-3=2x^{2}-1$

>[!warning]
>In general, $g\circ f\neq f\circ g$ ($\circ$ is not *commutative*)

But composition is *associative*: $f\circ(g\circ h)=(f\circ g)\circ h$

#### Proposition
$f:A\to B$ and $g:B\to A$ are inverses if and only if $g\circ f=i_{A}$ and $f\circ g=i_{B}$ (see [[identity-function]]).

>[!example]
>Show that $f(x)=2x-1$ and $g(x)=\frac{x+1}{2}$ are inverses.
>$(f\circ g)(x)=\frac{(2x-1)+1}{2}=x\quad \forall x\in\mathbb{R}$
>$(g\circ f)(x)=2\left( \frac{x+1}{2} \right)-1=x\quad \forall x\in\mathbb{R}$

#### Proposition
Show that composition of [[surjective-and-injective-functions#^667413|onto]] functions is onto.
##### Proof
Let $f:A\to B$ and $g:B\to C$ be onto. We need to show that $g\circ f:A\to C$ is onto. That is,
$$
\forall c\in C,\;\exists a\in A \textnormal{ such that } (g\circ f)(a)=c.
$$
Let $c\in C$. 
Since $g$ is onto, $\exists\, b\in B$ such that $g(b)=c$.
Since $f$ is into, $\exists\,a\in A$ such that $f(a)=b$.
Thus $(g\circ f)(a)=g(f(a))=g(b)=c$.