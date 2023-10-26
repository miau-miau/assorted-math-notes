---
tags:
  - combinatorics
order-tag: "0064"
date: 2023-10-17
---
If $A$ and $B$ are finite [[sets-naive|sets]], $|\,A\,|>|\,B\,|$, and $f:A\to B$ is a [[functions|function]], then $f$ cannot be [[surjective-and-injective-functions|one-to-one]].
```tikz
\begin{document}
\begin{tikzpicture}
  % Circle A (left, a little bigger)
  \draw (0,0) circle (1.5);
  \node at (0,1.75) {A};
 % Add bold dots and labels x, y, z, w
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (0,0.75) {x};
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (0,0.25) {y};
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (0,-0.25) {z};
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (0,-0.75) {w};
% Add bold dots and labels a, b, c
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (4,0.5) {a};
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (4,0) {b};
  \node[draw, circle, inner sep=2pt, fill=black, text=white] at (4,-0.5) {c};
  % Circle B (right)
  \draw (4,0) circle (1);
  \node at (4, 1.25) {B};
  
\draw[->, thick] (0.3, 0.75) -- (3.7, 0.5);
\draw[->, thick] (0.3, 0.25) -- (3.7, 0);
\draw[->, thick] (0.3,-0.25) -- (3.7, -0.45);
\draw[->, thick] (0.3,-0.75) -- (3.7, -0.55);
\end{tikzpicture}
\end{document}
```

If $A=\{ \textnormal{ pigeons } \}$ and $B=\{ \textnormal{ birdhouses } \}$, then each pigeon can be assigned to a birdhouse.

#### Pigeonhole Principle (weak)
If $n$ objects are put into $m$ boxes and $n>m$, then at least one box contains more than one object.

>[!example]
>If there are 13 people in a room, at least $2$ of them have birthdays in the same month.
>It is also true if there are more than $13$ people in the room then at least $2$ of them have birthdays in the same month. But we can say more.

#### Pigeonhole Principle (strong)
If $n$ objects are put into $m$ boxes and $n>m$, then some box must contain at least $\lceil \frac{n}{m} \rceil$ objects.

>[!example]
>If $251$ people are in a room, then at least $\lceil \frac{251}{12} \rceil=21$ of them have birthdays in the same month.

#### Applications
The Pigeonhole Principle can be used in creative ways to solve more difficult problems to which it is not obvious that the Pigeonhole Principle appears.

>[!example]
>Let $S$ be a square of side length $2$. If $S$ contains five points, then at least two of the points are within $\sqrt{ 2 }$ units of each other.
>
>Proof: Break $S$ into 4 squares. By the Pigeonhole Principle, two points must lie in the same square. Since the largest distance in each small square is $\sqrt{ 2 }$, the two points are within $\sqrt{ 2 }$ of each other.
>
>```tikz
\begin{document}
\begin{tikzpicture}
  % Draw the large square
  \draw (0,0) rectangle (4,4);
  % Divide the large square into 4 smaller squares
  \draw (0,0) rectangle (2,2);
  \draw (2,0) rectangle (4,2);
  \draw (0,2) rectangle (2,4);
  \draw (2,2) rectangle (4,4);
  % Label the squares
  \node at (1,1) {1};
  \node at (3,1) {2};
  \node at (1,3) {3};
  \node at (3,3) {4};
  % Place 5 points within the large square
  \fill (1.2, 1.6) circle (2pt);
  \fill (2.5, 0.5) circle (2pt);
  \fill (0.3, 3.4) circle (2pt);
  \fill (2.7, 2.7) circle (2pt);
  \fill (1.8, 3.8) circle (2pt);
\end{tikzpicture}
\end{document}```

See more in [[application-of-the-pigeonhole-principle-in-congruence-problems|application of the Pigeonhole Principle in congruence problems]].