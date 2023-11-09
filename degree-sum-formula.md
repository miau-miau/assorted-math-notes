---
tags:
  - graph-theory
order-tag: "0078"
date: 2023-10-31
aliases:
  - Degree Sum Formula
---
#### Degree Sum Formula (Euler)
Let $G=(V,E)$ be a [[graphs-introduction|pseudograph]]. Then
$$
\sum_{v\in V}\textnormal{deg }v=2|\,E\,|
$$
>[!example]
>```tikz
\begin{document}
\begin{tikzpicture}[main/.style={circle, draw, thick}]
  \node[main] (a) at (0, 0) {4};
  \node[main] (b) at (-2, 0) {2};
  \node[main] (c) at (1, 1) {5};
  \node[main] (d) at (2, -1) {3};
  \draw (a) -- (b);
  \draw (c) to [out=120,in=40,looseness=10] (c);
  \draw (d) -- (c);
  \draw (d) -- (a);
  \draw (a) to [out=60,in=210,looseness=1] (c);
  \draw (a) to [out=30,in=240,looseness=1] (c);
  \draw (b) to [out=330,in=180,looseness=1] (d);
  \node at (5, 0) {$\sum\textnormal{deg }v=4+2+5+3=14=2\cdot7$};
\end{tikzpicture}
\end{document}```
##### Proof
Recall that a [[graphs-introduction#Other Terminology|degree]] is the number of edges incident to $v$.
When we count $\sum\textnormal{deg }v$, we count each edge twice since each edge joins two vertices. Any loop also gets counted twice. So $\sum\textnormal{deg }v=2|\,E\,|$.

#### Corollary (Handshaking Lemma)
The number of odd vertices in a pseudograph is even.
##### Proof
$$
\begin{align}
2|\,E\,|=&\sum_{v\in V}\textnormal{deg }v=\sum_{V\textnormal{ odd}}\textnormal{deg }v+\sum_{V\textnormal{ even}}\textnormal{deg }v \\
\implies &\sum_{V\textnormal{ odd}}\textnormal{deg }v=2|\,E\,|-\sum_{V\textnormal{ even}}\textnormal{deg }v
\end{align}
$$
Since $2|\,E\,|$ is even and $\sum_{V\textnormal{ even}}\textnormal{deg }v$ is even, $\sum_{V\textnormal{ odd}}\textnormal{deg }v$ is even. For this sum to be even, the number of odd vertices must be even.