---
tags:
  - "#functions-and-maps"
order-tag: "0023"
date: 2023-09-07
---
>[!definition]
>A **function** from $A$ to $B$ ($f:A\to B$) is a [[binary-relation|binary relation]] from $A$ to $B$ satisfying
>$$\forall a\in A, \exists \textnormal{ exactly one } b\in B \textnormal{ such that } (a,b)\in f$$
>
>>[!example]
>>Let $A$ be a [[sets-naive|set]] of all adults and $B$ a set of all children on Earth. The relation
>>$$R=\{ (a,b)\in A\times B\mid a \textnormal{ is a parent of } b \}$$
>>is not a function since one adult can have several children.

#### Terms
If $f:A\to B$ is a function and $(a,b)\in f$, we write $b=f(a)$.

```tikz
\begin{document}
\begin{tikzpicture}
    \draw[fill=blue!30,fill opacity=0.5,draw=blue,thick] (-2,0) circle [radius=1cm];
    \draw[->, thick] (-0.7,0) -- (0.7,0);
    \draw[fill=orange!30,fill opacity=0.5,draw=orange,thick] (2,0) circle [radius=1cm];
    \draw[fill=red!30,fill opacity=0.5,draw=red,thick](2,0) circle [radius=0.5cm];
    \node at (0,0.3) {$f$};
    \node at (-3,1) {$A$};
    \node at (3,1) {$B$};
    
% Add a diagonal line to the red circle
	\draw[thick] (2.2, -0.2) -- (2.8, -0.8);
	
	% Add a label "rng f" near the red circle
	\node at (3.4, -0.8) {rng $f$};
\end{tikzpicture}
\end{document}
```
- $f(a)$ is the **image** of $a$
- $A$ is the **domain** of $f$
- $B$ is the **target** of $f$
- The **range** of $f$ is the set of images of $f$
$$\textnormal{rng }f=\{ b\in B\mid b=f(a)\textnormal{ for some } a\in A \}$$