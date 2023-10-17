---
tags:
  - number-theory
  - worked-example
order-tag: "0043"
date: 2023-09-21
---
[[multiplicative-inverse|Inverses]] can be used to solve [[congruence]] equations. If $\textnormal{gcd}(a,n)=1$, and we want to solve $ax\equiv b\;(\textnormal{mod }n)$, simply multiply both sides by $a^{-1}$:
$$
\begin{align}
a^{-1}ax\equiv a^{-1}b\;(\textnormal{mod }n) \\
x\equiv a^{-1}b\;(\textnormal{mod }n)
\end{align}
$$
Moreover, this solution is unique.

>[!example]
>Solve $20x\equiv 101\;(\textnormal{mod }637)$.
>>Since $\textnormal{gcd}(20,637)=1$, $20$ has an inverse. We can find $20^{-1}$ by solving $20x\equiv 1\;(\textnormal{mod }637)$ or using the [[linear-combination-of-gcd|fact]] that $1=20x+637y,\;x,y\in\mathbb{Z}$.
>>Solving for $x$ and $y$ using [[linear-combination-of-gcd#^ee2326|earlier tools]] gives $20(223)+637(-7)=1$.
>>So $20(223)\equiv 1+7(637)\equiv 1\;(\textnormal{mod }637)\implies 20^{-1}\equiv 223\;(\textnormal{mod }637)$.
>>Now $x\equiv(223)(101) \;(\textnormal{mod }637)\equiv 22523 \equiv 228\;(\textnormal{mod }637)$.


