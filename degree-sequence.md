---
tags:
  - graph-theory
order-tag: "0080"
date: 2023-10-31
---
>[!definition]
>Let $d_{1},\,d_{2},\,\dots,\,d_{n}$ be the degrees of the vertices of a [[graphs-introduction|pseudograph]] $G$, ordered so that $d_{1}\geq d_{2}\geq\dots\geq d_{n}$. Then $d_{1},\,d_{2},\,\dots,\,d_{n}$ is called the **degree sequence** of $G$.
>>[!example]
>>Degree sequence: $4,4,3,3,2$
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (0, 0) {};
  \node[main] (b) at (2, 0) {};
  \node[main] (c) at (-1, 1) {};
  \node[main] (d) at (-1, -1) {};
  \node[main] (e) at (-2, 0) {};
  \draw (e) -- (a) -- (c) -- (b) -- (a) -- (d) -- (e);
  \draw (c) to [out=10,in=100,looseness=0.7] (b);
  \draw (d) to [out=350,in=260,looseness=0.7] (b);
\end{tikzpicture}
\end{document}```
