---
tags:
  - proofs
order-tag: "0053"
date: 2023-09-28
aliases:
  - induction
---
Induction is a [[proofs|proof]] strategy that establishes the truth of a statement for all natural numbers or sometimes for all sufficiently large numbers.

>[!definition] Principle of Mathematical Induction
>To prove a statement $P$ is true $\forall\,n\geq n_{0}$:
>1. **Base Case.** Show $P$ is true for $n=n_{0}$.
>2. **Inductive Step**. Assume $P$ is true for $n=k$ (this is *inductive hypothesis*). Use this to show $P$ is true for $n=k+1$.
>
>Then $P$ is true for all $n\geq n_{0}$.
>
>>[!faq] Why?
>>We showed $P$ is true for $n=n_{0}$, so by (2), it is true for $n_{0}+1$. Then by (2), it is true for $n_{0}+2$. Continuing this process, we can show that $P$ is true for $n_{0}+3,\,n_{0}+4,\dots,\, n_{0}+m$, where $m$ is any natural number. Therefore, $P$ is true for any $n=n_{0}+m\geq n_{0}$.

#### Connection with Well-Ordering Principle
The principle of mathematical induction is logically equivalent to the [[well-ordering-principle|Well-Ordering Principle]]. That is we can use induction to prove the Well-Ordering Principle and vice versa.
##### Proof of Well-Ordering Principle via induction
1. **Base Case**. When $n=1,\,S=\{ a \}$ has one element $a$. Moreover, $a$ is the smallest element. Thus $S$ has a smallest element.
2. **Inductive Step**. Assume every subset of $\mathbb{N}$ with $k\geq 1$ elements has a smallest element. Let $S=\{ a_{1},\dots,a_{k}, a_{k+1} \}$. Consider $S'=S\setminus\{ a_{k+1} \}$. Since $S'$ has $k$ elements, by the inductive hypothesis, it has a smallest element $a_{i},\;1\leq i\leq k$. Thus the smaller of the two numbers $a_{i}$ and $a_{k+1}$ is the smallest element of $S$.
Thus $S$ has a smallest element.


