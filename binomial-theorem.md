---
tags:
  - combinatorics
order-tag: "0075"
date: 2023-10-26
aliases:
  - Binomial Theorem
---
Let's expand $(x+y)^n$, where $n\in\mathbb{N}$
$(x+y)^1=x+y$
$(x+y)^2=x^2+2xy+y^2$
$(x+y)^3=x^3+3x^{2}y+3y^{2}x+y^{3}$
$(x+y)^4=x^4+4x^{3}y+6x^{2}y^{2}+4xy^{3}+y^4$

The coefficients of these expressions can be arranged into **Pascal's Triangle**.
$$
\begin{gather}
1 \\
1\;\;1 \\
1\;\;2\;\;1 \\
1\;\;3\;\;3\;\;1 \\
1\;\;4\;\;6\;\;4\;\;1 \\
1\;\;5\;\;10\;\;10\;\;5\;\;1 \\
1\;\;6\;\;15\;\;20\;\;15\;\;6\;\;1
\end{gather}
$$
The numbers are actually [[combinations]].
$$1\;\;3\;\;3\;\;1\to\binom{3}{0}\;\binom{3}{1}\;\binom{3}{2}\binom{3}{3}$$
More generally, the numbers in the $n^\textnormal{th}$ row are
$$
\binom{n-1}{0}\;\binom{n-1}{1}\;\dots\;\binom{n-1}{n-1}
$$
#### Binomial Theorem
$$
\begin{align}
(x+y)^n&=\sum_{k=0}^n\binom{n}{k}x^{n-k}y^k \\
&=\binom{n}{0}x^n+\binom{n}{1}x^{n-1}y+\binom{n}{2}x^{n-2}y^{2}+ \\
&\qquad\dots\quad+\binom{n}{n-1}xy^{n-1}+\binom{n}{n}y^n
\end{align}
$$
>[!example]
>Find the coefficient of $x^{16}$ in $\left( 2x^{2}+\frac{x}{2} \right)^{12}$.
>
>Terms are of the form
>$$\begin{align}
\binom{12}{k}(2x^{2})^{12-k}\left( \frac{x}{2} \right)^k&=\binom{12}{k}2^{12-k}x^{2(12-k)} \frac{x^k}{2^k} \\
&=\binom{12}{k}2^{12-k}x^{24-k}
\end{align}$$
>We want $24-k=16\implies k=8$
>The coefficient is
>$$\binom{12}{8}2^{-4}=\frac{12!}{(12-8)!8!}\cdot \frac{1}{16}=\frac{12\cdot 11\cdot 10\cdot 9}{4!\cdot 16}=\frac{495}{16}$$

