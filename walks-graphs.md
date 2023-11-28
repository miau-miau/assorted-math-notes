---
tags:
  - graph-theory
order-tag: "0084"
date: 2023-11-07
---
#### Walk
>[!definition]
>Let $G$ be a [[graphs-introduction|pseudograph]]. A **walk** is an alternating sequence of incident vertices and edges of $G$, beginning and ending in vertices.
>The **length** of a walk is the number of edges in it.
>A walk is **closed** if the first vertex is the same as the last vertex (otherwise it is called open).
>>[!example]
>>An open walk $d\to e\to f\to a\to f\to b$.
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw=green, thick}]
  \node[main] (a) at (-1, 0.5)  {a};
  \node[main] (b) at (-1.2, 1.5)  {b};
  \node[main, draw=black] (c) at (0, 3) {c};
  \node[main] (e) at (2, 2)   {e};
  \node[main] (d) at (1.7, 0.3)   {d};
  \node[main] (f) at (0, 0){f};
  \draw[green, thick] (f) to [out=60,in=210,looseness=1] (e);
  \draw (f) to [out=30,in=240,looseness=1] (e);
  \draw (a) -- (b) -- (c) -- (e);
  \draw[green, thick] (d) -- (e);
  \draw[green, thick] (f) -- (a) -- (f) -- (b);
\end{tikzpicture}
\end{document}```

>[!definition]
>$G$ is **connected** if there exists a walk between any two vertices.

^393cf7

#### Trail
>[!definition]
>A **trail** is a [[walks-graphs#Walk|walk]] with distinct edges.
>>[!example]
>>An open trail $b\to a\to f\to e\to f$.
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw=green, thick}]
  \node[main] (a) at (-1, 0.5)  {a};
  \node[main] (b) at (-1.2, 1.5)  {b};
  \node[main, draw=black] (c) at (0, 3) {c};
  \node[main] (e) at (2, 2)   {e};
  \node[main, draw=black] (d) at (1.7, 0.3)   {d};
  \node[main] (f) at (0, 0){f};
  \draw[green, thick] (f) to [out=60,in=210,looseness=1] (e);
  \draw[green, thick] (f) to [out=30,in=240,looseness=1] (e);
  \draw (f) -- (b) -- (c) -- (e);
  \draw (d) -- (e);
  \draw[green, thick] (f) -- (a) -- (b);
\end{tikzpicture}
\end{document}```

#### Path
>[!definition]
>A **path** is a [[walks-graphs#Walk|walk]] with distinct vertices (and, consequently, edges).
>By definition, a path is always open.
>>[!example]
>>A path $b\to a\to f\to e\to d$.
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw=green, thick}]
  \node[main] (a) at (-1, 0.5)  {a};
  \node[main] (b) at (-1.2, 1.5)  {b};
  \node[main, draw=black] (c) at (0, 3) {c};
  \node[main] (e) at (2, 2)   {e};
  \node[main] (d) at (1.7, 0.3)   {d};
  \node[main] (f) at (0, 0){f};
  \draw (f) to [out=60,in=210,looseness=1] (e);
  \draw[green, thick] (f) to [out=30,in=240,looseness=1] (e);
  \draw (f) -- (b) -- (c) -- (e);
  \draw[green, thick] (d) -- (e);
  \draw[green, thick] (f) -- (a) -- (b);
\end{tikzpicture}
\end{document}```

#### Circuit
>[!example]
>A **circuit** is a closed [[walks-graphs#Trail|trail]].
>>[!example]
>>A circuit $b\to a\to f\to e\to f\to b$.
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw=green, thick}]
  \node[main] (a) at (-1, 0.5)  {a};
  \node[main] (b) at (-1.2, 1.5)  {b};
  \node[main, draw=black] (c) at (0, 3) {c};
  \node[main] (e) at (2, 2)   {e};
  \node[main, draw=black] (d) at (1.7, 0.3)   {d};
  \node[main] (f) at (0, 0){f};
  \draw[green, thick] (f) to [out=60,in=210,looseness=1] (e);
  \draw[green, thick] (f) to [out=30,in=240,looseness=1] (e);
  \draw (b) -- (c) -- (e);
  \draw (d) -- (e);
  \draw[green, thick] (b) -- (f) -- (a) -- (b);
\end{tikzpicture}
\end{document}```

#### n-cycle
>[!definition]
>An [[n-cycles]] is a [[walks-graphs#Circuit|circuit]] in which the only vertex that appears more than once is the first/last vertex.
>>[!example]
>>A 5-cycle $a\to b\to c\to e\to f\to a$.
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw=green, thick}]
  \node[main] (a) at (-1, 0.5)  {a};
  \node[main] (b) at (-1.2, 1.5)  {b};
  \node[main] (c) at (0, 3) {c};
  \node[main] (e) at (2, 2)   {e};
  \node[main, draw=black] (d) at (1.7, 0.3)   {d};
  \node[main] (f) at (0, 0){f};
  \draw (f) to [out=60,in=210,looseness=1] (e);
  \draw[green, thick] (f) to [out=30,in=240,looseness=1] (e);
  \draw (d) -- (e);
  \draw (f) -- (b);
  \draw[green, thick] (f) -- (a) -- (b) -- (c) -- (e);
\end{tikzpicture}
\end{document}```
