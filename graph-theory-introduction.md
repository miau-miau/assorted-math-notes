---
tags:
  - graph-theory
  - application
order-tag: "0076"
date: 2023-10-31
---
#### Famous problems
##### The Seven Bridges of Königsberg
Can one start on one land mass, walk over each bridge exactly once and arrive at the starting point?
![[Pasted image 20231107123610.png|400]]

**Euler** proved this (and a more general version) by reforming this into a question about graphs:
Does this graph have a *circuit*? No.

```tikz
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
\end{document}
```

##### Three Houses - Three Utilities
3 houses need to be connected to 3 utilities via underground pipes. Can we make these connections without crossovers?
![[Pasted image 20231107164150.png|400]]
Reformulated using graph theory:
Is this graph a *planar graph*? No.

```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw}]
  \node[main] (a) at (-2, 1) {1};
  \node[main] (b) at (0,  1) {2};
  \node[main] (c) at (2,  1) {3};
  \node[main] (w) at (-2,-1) {w};
  \node[main] (h) at (0, -1) {h};
  \node[main] (e) at (2, -1) {e};
  \draw (a) -- (w);
  \draw (a) -- (h);
  \draw (a) -- (e);
  \draw (b) -- (w);
  \draw (b) -- (h);
  \draw (b) -- (e);
  \draw (c) -- (w);
  \draw (c) -- (h);
  \draw (c) -- (e);
\end{tikzpicture}
\end{document}
```

##### The Traveling Salesman Problem
Given a list of cities and distances between each pair of cities, what is the shortest possible route that visits each city and returns to the origin city?
This is solved using *Hamiltonian cycles*.