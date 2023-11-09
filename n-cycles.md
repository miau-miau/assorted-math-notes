---
tags:
  - graph-theory
order-tag: "0082"
date: 2023-11-02
---
>[!definition]
>Let $v_{1},\dots,v_{n}\;(n\geq 3)$ be $n$ vertices in a [[graphs-introduction|graph]] $G$ such that $v_{i}$ and $v_{i+1}$ are adjacent $\forall\,i\mid1\leq i\leq n-1$ and $v_{1}$ and $v_{n}$ are also adjacent. Then the set of these $n$ vertices and $n$ edges is called an **n-cycle**.
>>[!example]
>>Blue is 4-cycle, and green is 3-cycle (also known as triangle).
>>```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, fill}]
  \node[main, draw=blue] (a) at (-1, 0.5)  {};
  \node[main, draw=blue] (b) at (-1.2, 1.5)  {};
  \node[main, draw=green] (c) at (0, 3) {};
  \node[main, draw=blue] (d) at (2, 1)   {};
  \node[main, draw=green] (e) at (1.2, 0.3)   {};
  \node[main, draw=blue] (f) at (0, 0){};
  \draw (a) -- (c) -- (f) -- (e) -- (b);
  \draw[green, thick] (c) -- (d) -- (e) -- (c);
  \draw[blue, thick]  (a) -- (f) -- (d) -- (b) -- (a);
\end{tikzpicture}
\end{document}```

#### Proposition (n-cycles in isomorphic graphs)
If $G_{1}\cong G_{2}$, i.e. they are [[isomorphism-graphs|isomorphic]], then $G_{1}$ and $G_{2}$ must contain the same number of n-cycles.
##### Proof (idea)
If $\phi:G_{1}\to G_{2}$ is an [[isomorphism-graphs|isomorphism]], then the image of an n-cycle in $G_{1}$ must be an n-cycle in $G_{2}$, Moreover, any n-cycle in $G_{2}$ must be the image of an n-cycle in $G_{1}$. So number of n-cycles in $G_{1}$ = number of n-cycles in $G_{2}$.