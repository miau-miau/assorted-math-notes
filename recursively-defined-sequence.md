---
tags:
  - sequences-and-series
order-tag: "0056"
date: 2023-10-03
---
>[!definition]
>A **recursively-defined sequence** is [[sequences|sequence]] whose $n^\textnormal{th}$ term is defined using previous terms.
>First term(s) are called *initial condition*, and the way the others are defined is called a *recurrence relation*.
>
>>[!example]
>>$a_{n}=n!$ can be defined recursively by $a_{1}=1$ and $a_{n}=na_{n-1}\quad\forall\,n\geq 2$

>[!example]
>Consider the sequence defined by $a_{1}=1$ and $a_{n}=3a_{n-1}+1$.
>It turns out that $a_{n}=\frac{3^n-1}{2}\quad\forall\,n\geq 1$.
>We can prove this by [[mathematical-induction|induction]]:
>1. **Base Case.** When $n=1$, $a_{1}=\frac{3^1-1}{2}=1$.
>2. **Inductive Step.** Assume $a_{k}=\frac{3^k-1}{2}$ for some $k\geq 1$.
>$$
\begin{align}
\textnormal{Then }a_{k+1}=3a_{k}+1&=3\left( \frac{3^k-1}{2} \right)+1 \\
&=\frac{3^{k+1}-3}{2}+1 \\
&=\frac{3^{k+1}-1}{2}
\end{align}
$$





