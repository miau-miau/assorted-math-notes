---
tags:
  - probability
order-tag: "0072"
date: 2023-10-26
---
>[!definition]
>Two [[probability-introduction#^f55be6|events]] $A$ and $B$ are called **independent** if the occurence of one doesn't affect the probability of the other. 
>More precisely,
>$$\textnormal{P}(B\mid A)=\textnormal{P}(B)$$

This implies $\frac{\textnormal{P}(A\cap B)}{\textnormal{P}(A)}=\textnormal{P}(B)\implies \textnormal{P}(A\cap B)=\textnormal{P}(A)\cdot\textnormal{P}(B)$
So $A$ and $B$ are independent if and only if $\textnormal{P}(A\cap B)=\textnormal{P}(A)\cdot\textnormal{P}(B)$.

>[!example]
>You roll a die 10 times. What is the probability that you roll an even number each time?
>
>Let $A_{i}$ be the event that the $i^{\textnormal{th}}$ roll is even. Note that $A_{1},\,A_{2},\,\dots,\,A_{10}$ are all independent. Moreover, $\forall\,i,\;\textnormal{P}(A_{i})=\frac{1}{2}$.
>Thus the probability that all rolls are even is
>$$\textnormal{P}(A_{1}\cap A_{2}\cap\dots A_{n})=\textnormal{P}(A_{1})\cdot \textnormal{P}(A_{2})\dots \textnormal{P}(A_{10})=\left( \frac{1}{2} \right)^{10}=\frac{1}{1024}$$

See more in [[conditional-probability-problems]].