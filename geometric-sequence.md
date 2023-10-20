---
tags:
  - sequences-and-series
order-tag: "0058"
date: 2023-10-03
---
>[!definition]
>The **geometric [[sequences|sequence]]** with the first term $a$ and common ratio $r$ is defined by
>$$a_{1}=a\textnormal{ and }a_{n}=ra_{n-1}\quad\forall\,n\geq 2$$

#### General formula
By [[mathematical-induction|induction]],
$$
a_{n}=ar^{n-1}
$$
##### Proof
1. **Base Case.** For $n=1,\;a_{n}=a_{1}=a$ and $ar^{n-1}=ar^0=a$.
2. **Inductive Step.** Assume $a_{k}=ar^{k-1}$. We want to show $a_{k+1}=ar^{(k+1)-1}=ar^k$.
$$a_{k+1}=ra_{k}=r(ar^{k-1})=ar^k$$   Thus $a_{n}=ar^{n-1}\quad\forall\,n\geq 1$.

#### Sum of first n terms
$$
\sum_{i=1}^{n}a_{i}=\frac{a(1-r^n)}{1-r}
$$
##### Proof
1. **Base Case.** 
2. **Inductive Step.** Assume
$$
\sum_{i=1}^{k}a_{i}=\frac{a(1-r^k)}{1-r}
$$
    We want to show
$$
\sum_{i=1}^{k+1}a_{i}=\frac{a(1-r^{k+1})}{1-r}
$$
    Using previous results,
$$
\begin{align}
\sum_{i=1}^{k+1}a_{i}=\sum_{i=1}^k a_{i}+a_{k+1}&=\frac{a(1-r^k)}{1-r}+ar^{(k+1)-1} \\
&=\frac{a(1-r^k)+ar^k(1-r)}{1-r} \\
&=\frac{a(1-r^k+r^k(1-r))}{1-r} \\
&=\frac{a(1-r^k+r^k-r^{k+1})}{1-r} \\
&=\frac{a(1-r^{k+1})}{1-r}
\end{align}
$$

