---
tags:
  - graph-theory
order-tag: "0079"
date: 2023-10-31
---
#### Complete Graph
>[!definition]
>The **complete graph** of $n$ vertices, $K_{n}$, is the [[graphs-introduction|graph]] with $n$ vertices, every two of which are adjacent.

```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (0, 0) {};
  \node at (0,-1) {$K_1$};
\end{tikzpicture}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-1, 0) {};
  \node[main] (b) at (1, 0) {};
  \draw (a) -- (b);
  \node at (0,-1) {$K_2$};
\end{tikzpicture}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-1, 0) {};
  \node[main] (b) at (1, 0) {};
  \node[main] (c) at (0, 2) {};
  \draw (a) -- (b) -- (c) -- (a);
  \node at (0,-1) {$K_3$};
\end{tikzpicture}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-1, 0) {};
  \node[main] (b) at (1, 0) {};
  \node[main] (c) at (-1, 2) {};
  \node[main] (d) at (1, 2) {};
  \draw (a) -- (b) -- (d) -- (c);
  \draw (d) -- (a) -- (c) -- (b);
  \node at (0,-1) {$K_4$};
\end{tikzpicture}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-0.8, 0) {};
  \node[main] (b) at (-1.2, 1.4) {};
  \node[main] (c) at (0, 2.4) {};
  \node[main] (d) at (1.2, 1.4) {};
  \node[main] (e) at (0.8, 0) {};
  \draw (a) -- (b) -- (c) -- (d) -- (e) -- (a);
  \draw (a) -- (c) -- (e) -- (b) -- (d) -- (a);
  \node at (0,-1) {$K_5$};
\end{tikzpicture}
\end{document}
```

#### Bipartite Graph
>[!definition]
>A **bipartite graph** is one whose vertices can be partitioned into two disjoint sets, $V_{1}$ and $V_{2}$ (called bipartition sets), such that every edge joins a vertex in $V_{1}$ and a vertex in $V_{2}$.

```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (-2, 0) {$a$};
  \node[main] (u) at (-1, 1.5) {$u$};
  \node[main] (b) at (0, 0)  {$b$};
  \node[main] (w) at (1, 1.5)  {$w$};
  \node[main] (c) at (2, 0)  {$c$};
  \draw (a) -- (u) -- (c) -- (w) -- (b) -- (u);
  \node at (0,-1) {$V_1=\{u,w\},\,V_2=\{a,b,c\}$};
\end{tikzpicture}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (-1, 0) {$a$};
  \node[main] (b) at (-1, 2) {$b$};
  \node[main] (c) at (1, 2)  {$c$};
  \node[main] (d) at (1, 0)  {$d$};
  \draw (a) -- (b) -- (c) -- (d) -- (a); 
  \node at (0,-1) {$V_1=\{b,d\},\,V_2=\{a,c\}$};
\end{tikzpicture}
\end{document}
```
##### Triangles in bipartite graphs
Any bipartite graph does not contain a triangle.
###### Proof
Pick any three vertices. By the [[pigeonhole-principle|Pigeonhole Principle]], two of them must be in either $V_{1}$ or $V_{2}$. Then by definition, these two vertices cannot be connected by an edge. Thus the three vertices do not form a triangle.
#### Complete Bipartite Graph
>[!definition]
>Let $|\,V_{1}\,|=n,\,|\,V_{2}\,|=m$. The **complete bipartite graph**, $K_{n,m}$, is a bipartite graph in which every vertex in $v_{1}$ is joined to every vertex in $v_{2}$.
>>[!example]
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (-2, 0) {};
  \node[main] (u) at (-1, 1.5) {};
  \node[main] (b) at (0, 0)  {};
  \node[main] (w) at (1, 1.5)  {};
  \node[main] (c) at (2, 0)  {};
  \draw (u) -- (b) -- (w) -- (c) -- (u) -- (a) -- (w);
  \node at (0,-1) {$K_{2,3}$};
\end{tikzpicture}
\end{document}```

>[!example] Worked Example
>How many edges does $K_{3,6}$ contain?
>$K_{3,6}$ has $3+6=9$ vertices.
>The $3$ vertices in $V_{1}$ each have degree $6$.
>The $6$ vertices in $V_{2}$ each have degree $3$.
>So $\sum\textnormal{deg }v=3\cdot {6}+6\cdot 3=36$.
>By [[degree-sum-formula|Degree Sum Formula]], $|\,E\,|=18$.