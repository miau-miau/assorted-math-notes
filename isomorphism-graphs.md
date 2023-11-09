---
tags:
  - graph-theory
order-tag: "0081"
date: 2023-11-02
aliases:
  - isomorphism
---
>[!definition]
>Two [[graphs-introduction|graphs]] $G_{1}=(V_{1},E_{1})$ and $G_{2}=(V_{2},E_{2})$ are **isomorphic** ($G_{1}\cong G_{2}$) if there is [[surjective-and-injective-functions|one-to-one, onto]] [[functions|function]] $\phi:V_{1}\to V_{2}$ such that $V_{1},V_{2}\in V$ are adjacent if and only if $\phi(V_{1}),\,\phi(V_{2})$ are adjacent.
>We say $\phi$ is an **isomorphism** from $G_{1}$ to $G_{2}$ and write $\phi:G_{1}\to G_{2}$.
>>[!example]
>>These two graphs are isomorphic. In both cases, $V=\{ 1,2,3,4 \}$ and $E=\{ \{ 1,2 \},\,\{ 1,3 \},\,\{ 2,4 \},\,\{ 3,4 \} \}$
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (-1, 0) {2};
  \node[main] (b) at (-1, 2) {1};
  \node[main] (c) at (1, 2)  {3};
  \node[main] (d) at (1, 0)  {4};
  \draw (a) -- (b) -- (c) -- (d) -- (a);
\end{tikzpicture}\hspace{1.5cm}%
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (-1, 0) {1};
  \node[main] (b) at (-1, 2) {2};
  \node[main] (c) at (1, 2)  {3};
  \node[main] (d) at (1, 0)  {4};
  \draw (a) -- (b) -- (d) -- (c) -- (a);
\end{tikzpicture}
\end{document}```

In other words, there is a 1-1 correspondence between vertices and edges that "respects" edges.

#### Proposition (basic properties of isomorphic graphs)
If $G_{1}\cong G_{2}$, then
- $G_{1}$ and $G_{2}$ have the same number of vertices
- $G_{1}$ and $G_{2}$ have the same number of edges
- $G_{1}$ and $G_{2}$ have the same [[degree-sequence|degree sequence]]

>[!warning]
>This is not an [[logic-statements#Double Implication (if and only if)|if and only if]] statement. There are non-isomorphic graphs that satisfy all 3 conditions above. These 3 properties should only be used to show that two graphs are *not* isomorphic.
>>[!example]
>>The two graphs below are not isomorphic, which we can prove with [[n-cycles]] (the first graph has no triangles, while the second has two).
>>
|                 | $G_{1}$                  | $G_{2}$                  |
| --------------- | ------------------- | ------------------- |
| edges           | 6                   | 6                   |
| vertices        | 9                   | 9                   |
| degree sequence | $\{ 3,3,3,3,3,3 \}$          | $\{ 3,3,3,3,3,3 \}$         |

```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-1, 0)  {};
  \node[main] (b) at (-1, 1)  {};
  \node[main] (c) at (0, 1.7) {};
  \node[main] (d) at (1, 1)   {};
  \node[main] (e) at (1, 0)   {};
  \node[main] (f) at (0, -0.7){};
  \draw (d) -- (a) -- (f) -- (c) -- (b) -- (e);
  \draw (c) -- (d) -- (e) -- (f);
  \draw (a) -- (b);
\end{tikzpicture}\hspace{1.5cm}%
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-1, 0)  {};
  \node[main] (b) at (-1, 1)  {};
  \node[main] (c) at (0, 1.7) {};
  \node[main] (d) at (1, 1)   {};
  \node[main] (e) at (1, 0)   {};
  \node[main] (f) at (0, -0.7){};
  \draw (a) -- (f) -- (e) -- (d) -- (c) -- (f);
  \draw (c) -- (b) -- (d);
  \draw (b) -- (a) -- (e);
\end{tikzpicture}
\end{document}
```

#### Isomorphism Class
Isomorphism is an [[equivalence-relation|equivalence relation]]:
- $G\cong G$
- if $G_{1}\cong G_{2}$, then $G_{2}\cong G_{1}$
- if $G_{1}\cong G_{2}$ and $G_{2}\cong G_{3}$, then $G_{1}\cong G_{3}$

>[!definition]
>The [[equivalence-class|equivalence class]] of a graph $G$ is called the **isomorphism class** of $G$.

