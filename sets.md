---
tags:
  - sets
  - naive-set-theory
order-tag: "0005"
aliases: 
date: 2023-08-29
---
>[!definition]
>A set is a collection of objects called **elements**.
>
>>[!example]
>>- $\{1,2,10,-3\}$
>>- $\{$Boston, Chicago, New York$\}$
>>- $\{$even integers$\} = \{2n \mid n$ is an integer $\}$
>>- $\{$odd integers$\} = \{2n+1\mid n$ is an integer $\}$

>[!info] Notation
>- $\in$ means that an element belongs to the set
>- $\mid$ means "such that" and can be used to "build" a set

#### Common sets
- $\mathbb{N}=\{1,2,3,\dots\}$ (natural numbers)
- $\mathbb{Z}=\{\dots,-1,0,1,2,3,\dots\}$ (integers)
- $\mathbb{Q}=\left\{ \frac{p}{q},\enspace p,q\in\mathbb{Z} \right\}$ (rational numbers)
- $\mathbb{R}=$ set of real numbers
- $\mathbb{C}=\{a+ni\mid a,b\in\mathbb{R}\}$
- $\emptyset=\{\}$ ([[empty-set-naive|empty set]])

>[!definition]
>Two sets are **equal** ($A=B$) is both sets contain the same elements or they are both empty (i.e. $x\in A\leftrightarrow x\in B$)
>
>>[!example]
>>- $\{ 1,2,1 \}=\{ 1,2 \}=\{ 2,1 \}$
>>- $\{ (x,y)\in \mathbb{R}^{2} \mid x^{2}+y^{2}=0 \} = \{ (0,0) \}$

#### Subsets
>[!definition]
>A set $A$ is a **subset** of $B$ ($A\subseteq B$) if every element of $A$ is an element of $B$ (i.e. $x\in A\to x\in B$). It also means that $B$ contains every element in $A$, and sometimes it is called a **superset** ($B\supseteq A$).
>>[!example]
>>$\mathbb{N}\subset \mathbb{Z}\subset \mathbb{Q}\subset \mathbb{R}\subset \mathbb{C}$

>[!info] Notation
>- $A\subset B$ means $B$ contains an element not in $A$ ($A$ is a **proper subset**)
>- $A\nsubseteq B$ means $A$ is not a subset of B

##### Proposition
$A=B$ if and only if $A\subseteq B$ and $B\subseteq A$.
###### Proof
1. If $A=B$, then $B$ contains every element in $A$, and $A$ contains every element in $B$. Therefore, $A\subseteq B$ and $B\subseteq A$.
2. Suppose that $A\subseteq B$ and $B\subseteq A$ and $A\neq B$. Then there exists either $x\in A,\;x\notin B$, or $x\in B,\;x \notin A$. But first situation is impossible since $A\subseteq B$, and the second one since $B\subseteq A$. Therefore, $A$ must be equal to $B$.

##### Proposition (empty set)
For any set $A$, $\emptyset \subseteq A$.
###### Proof
Assume $\emptyset\not\subseteq A$. Then $\\\exists x\in\emptyset$ such that $x\notin A$. But this is absurd since $\emptyset$ is empty. Thus $\emptyset\subseteq A$.

#### Power Set

>[!definition]
>The **power set** of a set $A$, denoted $P(A)$, is the set of all subsets of A.
>>[!example]
>>$A=\{ a,b,c \}$
>>$P(A)=\{ \emptyset,\{a\},\{b\},\{c\},\{a,b\},\{a,c\},\{b,c\},\{ a,b,c \} \}$

