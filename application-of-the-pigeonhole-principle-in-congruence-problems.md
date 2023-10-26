---
tags:
  - combinatorics
  - application
order-tag: "0065"
date: 2023-10-17
---
The [[pigeonhole-principle|Pigeonhole Principle]] can be helpful in solving problems involving [[congruence]] classes.

>[!example]
>Let $a_{1},\,a_{2},\,\dots,\,a_{n+1}\in\mathbb{Z}$ be $n+1$ randomly chosen distinct integers, Show that there are two whose difference is divisible by $n$.
>*Example:* $4,\,15,\,5,\,7,\;(n=3)\to 7-4=3$
>
>$\mathbb{Z}$ is [[partition-of-sets|partitioned]] into the congruence classes $\overline{0},\overline{1},\dots ,\overline{n+1}$. Each $a_{i}$ belongs to a congruence class. By the Pigeonhole Principle, $\exists$ two integers $a_{j},\,a_{k}$ n the same congruence class.
>Thus $a_{j}\sim a_{k}\;(\textnormal{mod }n)\implies n\mid a_{j}-a_{k}$.

>[!example]
>Given a list of $10$ numbers $a_{1},\,a_{2},\,\dots,\,a_{10}\in\mathbb{Z}$, there is a string of consecutive numbers whose sum is divisible by 10.
>
>Consider the ten sums:
>$s_{1}=a_{1}$
>$s_{2}=a_{1}+a_{2}$
>$\dots$
>$s_{10}=a_{1}+a_{2}+\dots+a_{10}$
>
>**Case 1**. One of these sums is divisible by $10$. In this case, we are done.
>**Case 2**. None of these sums is divisible by $10$.
>In this case, consider the congruence classes $\;(\textnormal{mod } 10)$. Now, $s_{i}\notin\overline{0}\quad\forall\,i$.
>Thus each $s_{i}$ is in $\overline{1},\,\overline{2},\dots,\,\overline{8}$ or $\overline{9}$. By the Pigeonhole Principle, at least two of these sums are in the same congruence class, i.e. $\exists\,i<j$ such that $s_{i}$ and $s_{j}$ are in the same congruence class. Thus
>$$\begin{align}
s_{j}&\equiv s_{i}\;(\textnormal{mod }10) \\
a_{1}+a_{2}+\dots+a_{j}&\equiv a_{1}+\dots+a_{i}\;(\textnormal{mod }10) \\
a_{i+1}+a_{i+2}+\dots+a_{j}&\equiv 0\;(\textnormal{mod }10)
\end{align}$$
>So $10\mid(a_{i+1}+\dots+a_{j})$.





