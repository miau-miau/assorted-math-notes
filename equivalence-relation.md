---
tags:
  - set-theory
order-tag: "0018"
date: 2023-09-05
---
>[!definition]
>A [[binary-relation|binary relation]] $R$ on a [[sets-naive|set]] $A$ is called an **equivalence relation** if $R$ is [[reflexive-relation|reflexive]], [[symmetric-relation|symmetric]], and [[transitive-relation|transitive]].
>>[!info] Notation
>>If $(a,b)\in R$, we write $a\sim b$.

With this notation, there are three requirements for a binary relation to be an equivalence class:
- *Reflexive*: $a\sim a\quad\forall a\in A$
- *Symmetric*: $a\sim b\to b\sim a\quad\forall a,b\in A$
- *Transitive*: $a\sim b,b\sim c\to a\sim c\quad\forall a,b,c\in A$.

>[!example]
>Equality is an equivalence relation. Let $R=\{ (a,b)\in A\times A\mid a=b \}$.
>- reflexive: $a=a\quad\forall a\in A$
>- symmetric: $a=b\to b=a$
>- transitive: $a=b\land b=c\to a=c$
>
>The relation $\leq$ is not an equivalence relation on $\mathbb{R}$, since it is not symmetric.

