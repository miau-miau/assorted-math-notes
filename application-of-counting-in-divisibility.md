---
tags:
  - application
  - combinatorics
  - worked-example
order-tag: "0063"
date: 2023-10-12
---
Let $A=\{ n\in\mathbb{Z} \mid 1\leq n\leq b \textnormal{ and } a|n\}$. Then $|\,A\,|=\lfloor \frac{b}{a} \rfloor$.
In other words, the number of integers between $1$ and $b$ that are [[basic-division|divisible]] by $a$ is $\lfloor \frac{b}{a} \rfloor$.
This follows from the [[division-algorithm|Division Algorithm]].

>[!example]
>How many integers between $1$ and $300$ (inclusive) are:
>a) divisible by $3$ and $5$?
>b) divisible by $3$ or $5$?
>c) divisible by $3$ but not $5$?
>d) divisible by $3$ or $5$ but not both?
>
>Let $A=\{ n\mid 1\leq n\leq 300 \textnormal{ and } 3|n \}$,
>$\quad\;\;\,B=\{ n| 1\leq n\leq 300 \textnormal{ and } 5|n \}$.
>Then $|\,A\,|=\lfloor \frac{300}{3} \rfloor=100$, $|\,B\,|=\lfloor \frac{300}{5} \rfloor=60$.
>
>See [[basic-counting|basic counting]].
>a) We want to find $|\,A\cap B\,|$.
>Notice that $n\in A\cap B \leftrightarrow 3|n\textnormal{ and } 5|n \leftrightarrow 15|n$
>So $A\cap B=\{ n\mid 1\leq n\leq 300 \textnormal{ and } 15|n\}\implies |\,A\cap B\,|=\lfloor \frac{300}{15} \rfloor=20$
>
>b) We want to find $|\,A\cup B\,|$. Using [[inclusion-exclusion-principle|Inclusion-Exclusion Principle]], $|\,A\cup B\,|=|\,A\,|+|\,B\,|-|\,A\cap B\,|=100+60-20=40$
>
>c) We want to find $|\,A\setminus B\,|$
>$|\,A\setminus B\,|=|\,A\,|-|\,A\cap B\,|=100-20=80$
>
>d) We want to find $|\,A\oplus B\,|$
>$|\,A\oplus B\,|=|\,A\,|+|\,B\,|-2|\,A\cap B\,|=100+60-2(20)=120$

