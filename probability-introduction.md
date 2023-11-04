---
tags:
  - probability
order-tag: "0069"
date: 2023-10-24
---
>[!definition]
>Let $S$ be the [[sets-naive|set]] of all outcomes of an experiment ($S$ is called the **sample space**).
>A [[sets-naive#Subsets|subset]] $A\subseteq S$ is called an **event**.
>**The probability** that $A$ occurs is denoted as $\textnormal{P}(A)$.
>If all outcomes are equally likely, then, assuming $S$ is finite,
>$$\textnormal{P}(A)=\frac{|\,A\,|}{|\,S\,|}$$
>>[!example]
>>Find the probability that an even number appears when a fair dice is rolled.
>>$S=\{ 1,2,3,4,5,6 \}$
>>$A=\{ 2,4,6 \}$
>>$\textnormal{P}(A)=\frac{3}{6}=\frac{1}{2}$

See more in [[basic-probability-problems]].

#### Properties
Let $S$ be the sample space of some experiment and $A,B$ events.

a) $0\leq \textnormal{P}(A)\leq 1,\;\textnormal{P}(\emptyset)=0,\;\textnormal{P}(S)=1$
b) $\textnormal{P}(A^{\mathbf{c}})=1-\textnormal{P}(A)$
c) $\textnormal{P}(A\cup B)=\textnormal{P}(A)+\textnormal{P}(B)-\textnormal{P}(A\cap B)$
d) If $A$ and $B$ are mutually exclusive (i.e. $A\cap B=\emptyset$), then $\textnormal{P}(A\cup B)=\textnormal{P}(A)+\textnormal{P}(B)$
e) $\textnormal{P}(A\setminus B)=\textnormal{P}(A\cap B)$

>[!example]
>A basket contains:
>- 3 red balls
>- 4 green balls
>- 9 yellow balls
>
>a) What is the probability that the two randomly chosen balls are both the same color?
>Let $$\begin{align}
R&=\{ \textnormal{ choose 2 red } \} \\
G&=\{ \textnormal{ choose 2 green } \} \\
B&=\{ \textnormal{ choose 2 blue } \}
\end{align}$$
>They are all mutually exclusive. We need to find
>$$\textnormal{P}(R\cup G\cup B)=\textnormal{P}(R)+\textnormal{P}(G)+\textnormal{P}(B)$$
>$|\,S\,|=16\cdot 16=256$
>$|\,R\,|=3\cdot 3=9$
>$|\,G\,|=3\cdot 3=16$
>$|\,Y\,|=3\cdot 3=81$
>So $\textnormal{P}(R\cup G \cup B)=\frac{9}{256}+\frac{16}{256}+\frac{81}{256}=\frac{53}{128}$

