---
tags:
  - graph-theory
order-tag: "0085"
date: 2023-11-07
---
>[!definition]
>An **Eulerian circuit** in a [[graphs-introduction|pseudograph]] is a [[walks-graphs#Circuit|circuit]] that contains every vertex and every vertex and every edge.
>If a graph contains an Eulerian circuit, we call it Eulerian.
>>[!example]
>>The [[graph-theory-introduction#The Seven Bridges of Königsberg|The Seven Bridges of Königsberg]] problem can be rephrased as:
>>Is $G$ Eulerian? The answer is no.

More generally, Euler asked:
Which graphs are Eulerian?

#### Theorem (Eulerian graphs)
A pseudograph is Eulerian if and only if it is [[walks-graphs#^393cf7|connected]] and every vertex is even.
##### Proof idea
($\rightarrow$) When traveling around $G$ in a Eulerian circuit, every time you enter a vertex through one edge, you must then leave it through another edge. So the number of edged incident to a given vertex $v$ is even. If $v$ has a loop, then the loop contributes 2 to the degree. Thus every vertex must have even degree.
($\leftarrow$) See the algorithm.

#### Algorithm for finding an Eulerian circuit

1. Find a circuit $C_{1}$ in $G$
   Such circuit exists since each vertex has even degree.
   
```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main, draw=blue!50] (a) at (-2, -1) {a};
  \node[main, draw=blue!50] (b) at (-2, 1)  {b};
  \node[main, draw=blue!50] (c) at (-1, 0)  {c};
  \node[main] (d) at (0, 1)   {d};
  \node[main] (e) at (0, -1)  {e};
  \node[main] (f) at (1.3, 1)   {f};
  \node[main] (g) at (1.3, -1)  {g};
  \node[main] (h) at (2.3, 0)   {h};
  \draw (d) -- (f) -- (h) -- (g) -- (e) -- (c) -- (d) -- (e) -- (f) -- (g) -- (d);
  \draw[blue!50, thick] (a) -- (b) -- (c) -- (a);
  \node[anchor=north] at (current bounding box.south) {$C_{1}=ABCA$};
\end{tikzpicture}
\end{document}
```

2. If $C_{1}$ is Eulerian, done. If not, delete edges of $C_{1}$ from $G$ and the resulting isolated vertices to get $G_{2}$.
   
```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw, thick}]
  \node[main, draw=blue!50] (c) at (-1, 0)  {c};
  \node[main] (d) at (0, 1)   {d};
  \node[main] (e) at (0, -1)  {e};
  \node[main] (f) at (1.3, 1)   {f};
  \node[main] (g) at (1.3, -1)  {g};
  \node[main] (h) at (2.3, 0)   {h};
  \draw (d) -- (f) -- (h) -- (g) -- (e) -- (c) -- (d) -- (e) -- (f) -- (g) -- (d);
  \node[anchor=east] at (current bounding box.west) {$G_{2}=$};
\end{tikzpicture}
\end{document}
```

3. Find a circuit $C_{2}$ in $G_{2}$ starting at a vertex $v$ that was in $c_{1}$
   Such circuit exists since degree of each vertex is even.
   
   ```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, draw=red!60, thick}]
  \node[main, draw=violet!60] (c) at (-1, 0)  {c};
  \node[main] (d) at (0, 1)   {d};
  \node[main] (e) at (0, -1)  {e};
  \node[main] (f) at (1.3, 1)   {f};
  \node[main] (g) at (1.3, -1)  {g};
  \node[main] (h) at (2.3, 0)   {h};
  \draw[thick, red!60] (d) -- (f) -- (h) -- (g) -- (e) -- (c) -- (d);
  \draw (d) -- (e) -- (f) -- (g) -- (d);
  \node[anchor=north] at (current bounding box.south) {$C_{2}=DFHGECD$};
\end{tikzpicture}
\end{document}
```

4. Combine $C_{1}$ and $C_{2}$ by starting with $C_{1}$ and switching to $C_{2}$ when you get to the common vertex $v$ and then go back to $C_{1}$.
   This gives a larger circuit in $G$.
   
```tikz
\begin{document}
\begin{tikzpicture} [rednode/.style={circle, draw=red!60, thick}, bluenode/.style={circle, draw=blue!50, thick}]
  \node[bluenode] (a) at (-2, -1) {a};
  \node[bluenode] (b) at (-2, 1)  {b};
  \node[bluenode, draw=violet!60] (c) at (-1, 0)  {c};
  \node[rednode] (d) at (0, 1)   {d};
  \node[rednode] (e) at (0, -1)  {e};
  \node[rednode] (f) at (1.3, 1)   {f};
  \node[rednode] (g) at (1.3, -1)  {g};
  \node[rednode] (h) at (2.3, 0)   {h};
  \draw[thick, red!60] (d) -- (f) -- (h) -- (g) -- (e) -- (c) -- (d);
  \draw (d) -- (e) -- (f) -- (g) -- (d);
  \draw[blue!50, thick] (a) -- (b) -- (c) -- (a);
  \node[anchor=north] at (current bounding box.south) {$ABCA+CDFHGEC=AB + CDFHGE + CA=ABCDFHGECA$};
\end{tikzpicture}
\end{document}
```

5. Repeat this process until we have an Eulerian circuit
   
```tikz
\begin{document}
\begin{tikzpicture} [main/.style={circle, thick}]
  \node[main, draw=blue!50] (a) at (-2, -1) {a};
  \node[main, draw=blue!50] (b) at (-2, 1)  {b};
  \node[main, draw=violet!60] (c) at (-1, 0)  {c};
  \node[main, draw=orange] (d) at (0, 1)   {d};
  \node[main, draw=orange] (e) at (0, -1)  {e};
  \node[main, draw=orange] (f) at (1.3, 1)   {f};
  \node[main, draw=orange] (g) at (1.3, -1)  {g};
  \node[main, draw=red!60] (h) at (2.3, 0)   {h};
  \draw[thick, red!60] (d) -- (f) -- (h) -- (g) -- (e) -- (c) -- (d);
  \draw[orange, thick] (d) -- (e) -- (f) -- (g) -- (d);
  \draw[blue!50, thick] (a) -- (b) -- (c) -- (a);
  \node[anchor=north] at (current bounding box.south) {$\textcolor{blue!50}{ABCA}+\textcolor{red!60}{CDFHGEC}+\textcolor{orange}{DGFED}=ABCDGFEDFHGECA$};
\end{tikzpicture}
\end{document}
```
