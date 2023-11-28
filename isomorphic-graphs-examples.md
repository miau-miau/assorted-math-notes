---
tags:
  - graph-theory
order-tag: "0083"
date: 2023-11-02
---
#### Basic Example
>[!task]
>Show that $G_{1}$ and $G_{2}$ are [[isomorphism-graphs|isomorphic]].
>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (-1, 0) {a};
  \node[main] (b) at (1, 0)  {b};
  \node[main] (c) at (1, 2)  {c};
  \node[main] (d) at (-1, 2) {d};
  \draw (a) -- (b) -- (c) -- (d) -- (a) -- (c);
\end{tikzpicture}\hspace{1.5cm}%
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (w) at (0, 0)  {w};
  \node[main] (x) at (0, 1.2)  {x};
  \node[main] (y) at (1, 2)  {y};
  \node[main] (z) at (-1, 2) {z};
  \draw (w) -- (x) -- (y) -- (w) -- (z) -- (y);
\end{tikzpicture}
\end{document}```

Let $\phi: V_{1}\to V_{2}$ be defined by:

| $v$ | $\phi(v)$ |
| --- |---------|
| $a$ |    $w$    |
| $b$ |    $x$    |
| $c$ |    $y$    |
| $d$ |    $z$    |

Check edges:
- $a,b$ are adjacent and $\phi(a)=w,\,\phi(b)=x$ are adjacent
- $a,c$ are adjacent and $\phi(a)=w,\,\phi(c)=y$ are adjacent
- $\dots$
- $c,d$ are adjacent and $\phi(c)=y,\,\phi(d)=z$ are adjacent

Thus, these graphs are isomorphic.

to be continued