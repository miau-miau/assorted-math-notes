---
tags:
  - probability
  - worked-example
order-tag: "0073"
date: 2023-10-26
---
>[!example]
>The probability you eat a salad for lunch is 0.6, the probability you eat tuna for lunch is 0.7, and the probability you eat neither is 0.2.
>Let $A$be an event you eat a salad
>Let $B$ be an event you eat tuna
>Show that $A$ and $B$ are not [[independent-events|independent]].
>
>We have $\textnormal{P}(A)=0.6,\,\textnormal{P}(B)=0.7,\,\textnormal{P}(A^\mathbf{c}\cap B^\mathbf{c})=0.2$.
>Now,
>$$\begin{align}
\textnormal{P}(A\cap B)&=\textnormal{P}(A)+\textnormal{P}(B)-\textnormal{P}(A\cup B) \\
&=\textnormal{P}(A)+\textnormal{P}(B)-(1-\textnormal{P}((A\cup B)^\mathbf{c})) \\
&=\textnormal{P}(A)+\textnormal{P}(B)-1+\textnormal{P}(A^\mathbf{c}\cap B^\mathbf{c}) \\
&=0.6+0.7-1+0.2=0.5
\end{align}$$
>But $\textnormal{P}(A)\cdot \textnormal{P}(B)=0.6\cdot 0.7=0.42$
>Since $\textnormal{P}(A\cap B)\neq \textnormal{P}(A)\cdot \textnormal{P}(B)$, the events are not independent.

to be continued