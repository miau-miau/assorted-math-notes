---
tags:
  - graph-theory
order-tag: "0086"
date: 2023-11-07
---
>[!definition]
>An **Eulerian trail** is a [[walks-graphs#Trail|trail]] that passes through every vertex and includes every edge.
>>[!example]
>>$ABCDEF$ is an Eulerian trail.

```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (-1.5, -0)  {a};
  \node[main] (b) at (0, 0)      {b};
  \node[main] (c) at (1.5, 0)    {c};
  \node[main] (d) at (1.5, -1.5) {d};
  \node[main] (e) at (0, -1.5)   {e};
  \node[main] (f) at (0, 1.5)    {f};
  \draw (a) -- (b) -- (c) -- (d) -- (e) -- (b) -- (f);
\end{tikzpicture}
\end{document}
```

Note that by adding an edge between the first and last vertex of an Eulerian trail, we get an [[eulerian-graphs|Eulerian circuit]] . This means [[eulerian-graphs#Theorem (Eulerian graphs)|all vertices are even]] except the first and last.

#### Theorem (Eulerian graphs)
A pseudograph $G$ has an Eulerian trail between distinct vertices $u$ and $v$ if and only if all vertices of $G$ are even except for $u$ and $v$.