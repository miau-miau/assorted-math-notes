---
tags:
  - sequences-and-series
order-tag: "0057"
date: 2023-10-03
---
>[!definition]
>The **arithmetic [[sequences|sequence]]** with first term $a$ and common difference $d$ is given by:
>$$a_{1}=a\textnormal{ and } a_{n}=a_{n-1}+d\quad\forall\,n\geq 2$$

#### General formula
Using [[mathematical-induction|induction]], we can show
$$a_{n}=a+(n-1)d$$
>[!example]-
>You have 100 dollars in your shoebox and you began selling cupcakes. You earn 30 dollars per week, which you put in the shoebox.
>Here, $a=100,\;d=30$.
>In 10 weeks, you have $a_{11}=100+10(30)=400$.
##### Proof
1. **Base Case.** For $n=1$, $a_{1}=a+(1-1)d=a$.
2. **Inductive Step.** Assume $a_{k}=a+(k-1)d$. We want to show $a_{k+1}=a+((k+1)-1)d=a+kd$.
   $$a_{k+1}=a_{k}+d=a+(k-1)d+d=a+kd$$
Thus $a_{n}=a+(n-1)d\quad\forall\,n\geq 1$.

#### Sum of first n terms
It is also easy to show that
$$\sum_{i=1}^{n}a_{i}=\frac{n(2a+(n-1)d)}{2}$$
##### Proof
1. **Base Case.** For $n=1$,
$$\sum_{i=1}^n a_{i}=\sum_{i=1}^1 a_{i}=a_{1}=a$$
$$\frac{n(2a+(n-1)d)}{2}=\frac{1(2a)}{2}=a$$
2. **Inductive Step.** Assume $$\sum_{i=1}^{k}a_{i}=\frac{k(2a+(k-1)d)}{2}$$We want to show
 $$\sum_{i=1}^{k+1}a_{i}=\frac{(k+1)(2a+((k+1)-1)d)}{2}=\frac{(k+1)(2a+kd)}{2}$$    Using previous results,
$$
\begin{align}
\sum_{i=1}^{k+1}a_{i}=\sum_{i=1}^{k}a_{i}+a_{k+1}&=\frac{k(2a+(k-1)d)}{2}+(a+((k+1)-1)d) \\
&=\frac{k(2a+kd-d)}{2}+(a+kd) \\
&=\frac{k(2a+kd)-kd+2a+2kd}{2} \\
&=\frac{k(2a+kd)+2a+kd}{2} \\
&=\frac{(k+1)(2a+kd)}{2}
\end{align}
$$

