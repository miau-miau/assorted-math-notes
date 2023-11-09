---
tags:
  - graph-theory
order-tag: "0077"
date: 2023-10-31
aliases:
  - graph
  - pseudograph
---
#### Graph
>[!definition]
>A **graph** $G$ is a pair $(V,E)$ of [[sets-naive|sets]] such that
>- $V$ is nonempty
>- elements of $E$ are sets of two distinct elements of $V$
>
>$V$ represents **vertices**, and $E$ represents **edges**.
>>[!example]
>>$V=\{ a,b,c,d \}$
>>$E=\{ \{ a,b \},\;\{ a,c \}\;\{ c,d \},\;\{ a,d \} \}$
>>We can encode this in a drawing.
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main] (a) at (0, 0) {a};
  \node[main] (b) at (-2,  0) {b};
  \node[main] (c) at (2,  1) {c};
  \node[main] (d) at (2,-1) {d};
  \draw (a) -- (b);
  \draw (a) -- (c);
  \draw (a) -- (d);
  \draw (c) -- (d);
\end{tikzpicture}
\end{document}```

>[!faq] What about multiple edges?
>Notice that the "graph" we drew for the [[graph-theory-introduction#The Seven Bridges of Königsberg|the Seven bridges of Konigsberg]] problem is *not* a graph. Why? It has multiple edges between two vertices.
>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main] (a) at (0, 0) {};
  \node[main] (b) at (2, 0) {};
  \node[main] (c) at (-1, 1) {};
  \node[main] (d) at (-1, -1) {};
  \draw (a) -- (b);
  \draw (c) to [out=0,in=90,looseness=0.7] (a);
  \draw (c) to [out=270,in=180,looseness=0.7] (a);
  \draw (d) to [out=0,in=270,looseness=0.7] (a);
  \draw (d) to [out=90,in=180,looseness=0.7] (a);
  \draw (c) to [out=10,in=100,looseness=0.7] (b);
  \draw (d) to [out=350,in=260,looseness=0.7] (b);
\end{tikzpicture}
\end{document}```
#### Pseudograph
>[!definition]
>A **pseudograph** is a "graph" in which multiple edges between two vertices and an edge from a vertex to itself (called a **loop**) can exist.
>>[!example]
>>```tikz
\begin{document}
\begin{tikzpicture}[main/.style={circle, fill}]
  \node[main] (a) at (0, 0) {};
  \node[main] (b) at (-2, 0) {};
  \node[main] (c) at (1, 1) {};
  \node[main] (d) at (2, -1) {};
  \draw (a) -- (b);
  \draw (c) to [out=120,in=40,looseness=10] (c);
  \draw (d) -- (c);
  \draw (d) -- (a);
  \draw (a) to [out=60,in=210,looseness=1] (c);
  \draw (a) to [out=30,in=240,looseness=1] (c);
  \draw (b) to [out=330,in=180,looseness=1] (d);
\end{tikzpicture}
\end{document}```

#### Other Terminology
- Two vertices sharing an edge are called **adjacent**.
- Two edges sharing a vertex are called **adjacent**.
- An edge is **incident** to its vertex endpoints.
- The degree of a vertex $v$, $\textnormal{deg }v$, is the number of edges incident to $v$:
```tikz
\begin{document}
\begin{tikzpicture}[main/.style={circle, draw, thick}]
  \node[main] (a) at (0, 0) {4};
  \node[main] (b) at (-2, 0) {2};
  \node[main] (c) at (1, 1) {5};
  \node[main] (d) at (2, -1) {3};
  \node[main] (e) at (3, 2) {0};
  \draw (a) -- (b);
  \draw (c) to [out=120,in=40,looseness=10] (c);
  \draw (d) -- (c);
  \draw (d) -- (a);
  \draw (a) to [out=60,in=210,looseness=1] (c);
  \draw (a) to [out=30,in=240,looseness=1] (c);
  \draw (b) to [out=330,in=180,looseness=1] (d);
\end{tikzpicture}
\end{document}
```
- A vertex of degree 0 is **isolated**.
- $v$ is **even** if $\textnormal{deg }v$ is even, and **odd** if $\textnormal{deg }v$ is odd
- $G'=(V',E')$ is a **subgraph** of $G=(V,E)$ is $V'\subseteq V$ and $E'\subseteq E$.