---
tags:
  - proofs
  - worked-example
  - number-theory
order-tag: "0054"
date: 2023-09-28
---
Let's look at a few examples of how [[mathematical-induction|induction]] is a useful proof strategy.

>[!example]
>Prove that $\forall\,n\geq 1,$
>$$1+3+5+\dots+(2n-3)+(2n-1)=n^{2}$$
>> 1. **Base Case**. When $n=1$, we have $2n-1=2(1)-1=1=1^{2}$. Thus for $n=1,\;1+3+\dots+(2n-1)=n^{2}$.
>> 2. **Inductive Step**. Assume $S'=1+3+5+\dots+(2k-1)=k^{2}$ for some $k\geq 1$. We want to prove $S=1+3+\dots+(2k-1)+(2(k+1)-1)=(k+1)^{2}$.
>>    Note that $S=S'+(2(k+1)-1)=k^{2}+(2(k+1)-1)$ by inductive hypothesis. Therefore, $S=k^{2}+2k-1=(k+1)^{2}$, which is what we needed to show.

>[!example]
>Prove that $\forall\,n\geq 1,$
>$$\sum_{i=1}^{n} i^{2}=\frac{n(n+1)(2n+1)}{6}$$
>>1. **Base Case**. When $n=1$,
>>   $$\sum_{i=1}^{n}i^{2}=\sum_{i=1}^{1}i^{2}=1^{2}=1$$
>>   $$\frac{n(n+1)(2n+1)}{6}=\frac{1(2)(3)}{6}=1$$
>> 2. **Inductive Step**. Assume
>>    $$\sum_{i=1}^{k}i^{2}=\frac{k(k+1)(2k+1)}{6}\textnormal{ for some }k\geq 1$$
>>    We need to prove
>>    $$\sum_{i=1}^{k+1}i^{2}=\frac{(k+1)((k+1)+1)(2(k+1)+1)}{6}=\frac{(k+1)(k+2)(2k+3)}{6}$$
>>    $$
\begin{align}
\sum_{i=1}^{k+1}=\sum_{i=1}^{k}+(k+1)^{2}&=\frac{k(k+1)(2k+1)}{6}+(k+1)^{2} \\
&=\frac{k(k+1)(2k+1)+6(k+1)^{2}}{6} \\
&=\frac{(k+1)(k(2k+1)+6(k+1))}{6} \\
&=\frac{(k+1)(2k^{2}+7k+6)}{6} \\
&=\frac{(k+1)(k+2)(2k+3)}{6}
\end{align}
$$


to be continued
