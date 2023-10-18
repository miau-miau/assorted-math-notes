---
tags:
  - algorithms
  - functions-and-maps
order-tag: "0050"
date: 2023-09-26
---
>[!definition]
>If $f=O(g)$ and $g\neq O(f)$ (*see [[big-o-notation|Big O]]*), we say $f$ has **smaller order** than $g$ and write $f\prec g$.
>If $f=O(g)$ and $g=O(f)$, we say $f$ and $g$ have the **same order** and write $f\asymp g$.
>
>>[!note]
>>$\asymp$ is an [[equivalence-relation|equivalence relation]].

>[!example]
>We've seen that:
>- $n+1\prec n^{2}$
>- $n^{3}\asymp 15n^{3}$

We can figure out whether $f\prec g$, $g\prec f$, or $f\asymp g$ using limits.

#### Proposition
$$
\begin{align}
&a)\;\textnormal{If } \lim_{ n \to \infty }{\frac{f(n)}{g(n)}}=0,\textnormal{ then } f\prec g  \\
&b)\;\textnormal{If } \lim_{ n \to \infty }{\frac{f(n)}{g(n)}}=\infty, \textnormal{ then } g\prec f \\
&c)\;\textnormal{If }\lim_{ n \to \infty }{\frac{f(n)}{g(n)}}=L,\;L\in\mathbb{R}\setminus \{ 0 \}, \textnormal{ then } f\asymp g
\end{align}
$$
##### Polynomials
From calculus,
$$\lim_{n \to \infty} \frac{a_{t}n^t + a_{t-1}n^{t-1} + \dots + a_{1}n + a_{0}}{b_{s}n^s + b_{s-1}n^{s-1} + \dots + b_{1}n + b_{0}} =
\left\{
\begin{array}{ll}
    0 & \text{if } s\geq t \\
    \infty & \text{if } t\geq s \\
    \frac{a_{t}}{b_{s}} & \text{if }t=s \\
\end{array}
\right.
$$
Thus if $f$ and $g$ are polynomials,
$$
\begin{align}
&f\prec g \textnormal{ if degree of } f<\textnormal{degree of }g \\
&f\asymp g \textnormal{ if degree of } f = \textnormal{degree of }g
\end{align}
$$
##### Other useful examples
We can also show for $a,b>1$:
$$
1\prec\log_{b}n\prec n\prec n^a\prec b^n \prec n!\prec n^n
$$

#### Proposition (operations with Big O)
$$
\begin{align}
&a)\;\textnormal{ If }f=O(g),\textnormal{ then } f+g=O(g) \\
&b)\;\textnormal{ If }f=O(g) \textnormal{ and } f_{1}=O(g_{1}), \textnormal{ then } ff_{1}=O(gg_{1})
\end{align}
$$
>[!example]
>Show $n\asymp n+\log n$
>- Since $n\leq n + \log n\quad\forall n>0,\;n=O(n+\log n)$
>- We know $\log n\prec n$ and so $\log n=O(n)$.
>By proposition, $n+\log n=O(n)$.
>Thus $n\asymp n+\log n$.

