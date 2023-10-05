---
tags:
  - sets
  - naive-set-theory
order-tag: "0021"
date: 2023-09-05
---
>[!definition]
>A **partition of** $A$ is a collection of disjoint subsets of $A$ whose union is $A$.

#### Theorem (partition)
Let $\sim$ be an [[equivalence-relation|equivalence relation]] on a set $A$. Then $$\forall a,b\in A,\quad a\sim b \leftrightarrow \bar{a}=\bar{b}$$
Moreover, if $a\not\sim b$, then $\bar{a}\cap \bar{b}=\emptyset$. 
Consequently, the equivalence classes of $A$ from a partition of $A$.
##### Proof
($\rightarrow$) Let $a\sim b$. We need to show $\bar{a}=\bar{b}$.
Let $x\in\bar{a}$. Then $x\sim a$. Since $a\sim b$, by transitivity, $x\sim b$.
Thus $x\in\bar{b}\to \bar{a}\subseteq \bar{b}$.
A similar argument shows $\bar{b}\subseteq \bar{a}$.
Therefore, $\bar{a}=\bar{b}$.
($\leftarrow$) Let $\bar{a}=\bar{b}$. By reflexivity, $a\sim a$, and so $a\in\bar{a}=\bar{b}$. Thus $a\sim b$.

We have thus shown $a\sim b\leftrightarrow \bar{a}=\bar{b}$.
Now let $a\not\sim b$. Assume $\bar{a}\cap \bar{b}\neq\emptyset$. Then $\exists\;x\in(\bar{a}\cap \bar{b})\to x\sim a \textnormal{ and } x\sim b\to a\sim b$ (by transitivity). But this is a contradiction. This $\bar{a}\cap \bar{b}=\emptyset$.