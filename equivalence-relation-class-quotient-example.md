---
tags:
  - worked-example
  - set-theory
order-tag: "0022"
date: 2023-09-05
---
#### Example 1
Define $\sim$ on $\mathbb{Z}$ by:
$$a\sim b\leftrightarrow 3|a-b\quad(a-b \textnormal{ is divisible by }3)$$
$(R=\{ (a,b)\in\mathbb{Z}\mid 3 \textnormal{ divides } a-b \})$

1. Let's check that $\sim$ is an [[equivalence-relation|equivalence relation]]:
- [[reflexive-relation|Reflexive]]: $a-a=0\to 3|a-a\to a\sim a$ ✔️
- [[symmetric-relation|Symmetric]]: $a\sim b\to 3|a-b \to 3|-(a-b)\to 3|b-a\to b\sim a$ ✔️
- [[transitive-relation|Transitive]]: $a\sim b\textnormal{ and }b\sim c\to 3|a-b \textnormal{ and } 3|b-c \to3|(a-b)+(b-c) \to 3|a-c\to a\sim c$ ✔️

2. What are the [[equivalence-class|equivalence classes]] of $\sim$?
$\bar{0}=\{ a\in\mathbb{Z}\mid 3|a-0 \}=$
$\;\;\;\quad\{ a\in\mathbb{Z}\mid a=3k,k\in\mathbb{Z} \}=$
$\;\;\;\quad\{ 0,\pm 3,\pm 6,\pm 9,\dots \}=3\mathbb{Z}$
$\bar{1}=\{ a\in\mathbb{Z}\mid 3|a-1 \}=$
$\;\;\;\quad\{ a\in\mathbb{Z}\mid a=3k+1,k\in\mathbb{Z} \}=$
$\;\;\;\quad\{ 1,\pm 4,\pm 7,\pm 10,\dots \}=3\mathbb{Z}+1$
$\bar{2}=\{ a\in\mathbb{Z}\mid 3|a-2 \}=$
$\;\;\;\quad\{ a\in\mathbb{Z}\mid a=3k+2,k\in\mathbb{Z} \}=$
$\;\;\;\quad\{ 2,\pm 5,\pm 8,\pm 11,\dots \}=3\mathbb{Z}+2$

Notice, $\mathbb{Z}=\bar{0}\cup \bar{1}\cup \bar{2}$. (it is a [[partition-of-sets|partition]]).
The [[quotient-set|quotient set]] is 
$$
\mathbb{Z}/\sim=\{ \bar{0}, \bar{1}, \bar{2}\}=\{ 3\mathbb{Z},\;3\mathbb{Z}+1,\;3\mathbb{Z}+2 \}
$$
#### Example 2
Define $\sim$ on $\mathbb{R}^{2}$ by:
$$
(x,y)\sim(y,x) \leftrightarrow x^{2}+y^{2}=u^{2}+v^{2}
$$
This is an equivalence relation.
Geometrically,
$$(x,y)\sim(u,v)\leftrightarrow(x,y)\textnormal{ and }(u,v)\textnormal{ lie on the same circle centered at the origin}$$
Equivalence classes are circles centered at $(0,0)$:
```tikz
\begin{document}
\begin{tikzpicture}
  \draw[->, thick] (-4,0) -- (4,0);
  \draw[->, thick] (0,-4) -- (0,4);
  \draw[draw=blue!40, thick] (0,0) circle [radius=1.5cm];
  \draw[draw=pink, thick] (0,0) circle [radius=3cm];
  \node at (1.4, 1.4) {$\overline{(1,0)}$};
  \node at (2.45, 2.45) {$\overline{(2,0)}$};
  \node at (-0.5,-0.4) {$(0,0)$};
\end{tikzpicture}
\end{document}
```
