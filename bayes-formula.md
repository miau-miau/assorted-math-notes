---
tags:
  - probability
order-tag: "0074"
date: 2023-10-26
---
#### Bayes' Formula

$$
\textnormal{P}(B\mid A)=\frac{\textnormal{P}(B)\cdot \textnormal{P}(A\mid B)}{\textnormal{P}(A)}
$$
##### Proof
Let's use the formula for [[conditional-probability|conditional probability]]:
$$

\begin{align}
\textnormal{P}(A\mid B)=\frac{\textnormal{P}(A\cap B)}{\textnormal{P}(B)}\implies \textnormal{P}(A\mid B)\cdot \frac{\textnormal{P}(B)}{\textnormal{P}(A)} &=\frac{\textnormal{P}(A\cap B)}{\textnormal{P}(B)}\cdot \frac{\textnormal{P}(B)}{\textnormal{P}(A)} \\
&=\frac{\textnormal{P}(B)\cdot \textnormal{P}(A\mid B)}{\textnormal{P}(A)}
\end{align}
$$
