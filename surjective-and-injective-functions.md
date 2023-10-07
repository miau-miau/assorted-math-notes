---
tags:
  - functions-and-maps
order-tag: "0024"
date: 2023-09-07
---
>[!definition]
>[[functions|Function]] $f$ is **onto** (surjective) if $\textnormal{rng }f=B$
>$$\forall\;b\in B, b=f(x) \textnormal{ has a solution } x\in A$$

>[!definition]
>$f$ is **one-to-one** (injective) if different elements of $A$ have different images
>$$f(a_{1})=f(a_{2})\to a_{1}=a_{2}$$

- $f$ is a **bijection** if it is onto and one-to-one.

#### Examples

>[!example]
>$A=\{ 1,2,3,4 \},\;B=\{ x,y,z,w,t \}$
>$f=\{ (1,x),(2,y),(3,w),(4,x) \}$
>- $\textnormal{rng }f=\{ x,y,w,x \}$
>- $f$ is *not* onto since $\textnormal{rng }f\neq B$. In particular, $t\not\in \textnormal{rng }f$ (i.e. $f(x)=t$ has no solution)
>- $f$ is not one-to-one since $f(1)=f(4)=x$.

>[!example]- More examples
>$f:\mathbb{Z}\to \mathbb{Z},\; f(x)=2x-3$
>- What is the range of $f$?
>$b\in \textnormal{rng }f\leftrightarrow b=f(x) \textnormal{ for some } x\in\mathbb{Z}$
>$\hskip 4em\, \leftrightarrow b=2x-3=2(x-2)+1$
>$\hskip 4em\, \leftrightarrow b \textnormal{ is odd}$.
>So $\textnormal{rng }f=\{ \textnormal{ odd integers } \}$
>- If $f$ onto?
>No, since $\textnormal{rng }f\neq \mathbb{Z}$. In particular, $\textnormal{rng }f$ does not contain even integers.
>- If $f$ one-to-one?
>Yes, since
> $$f(x_{1})=f(x_{2})\to 2x_{1}-3=2x_{2}-3\to x_{1}=x_{2}$$

#### Geometric interpretation
If $f:\mathbb{R}\to \mathbb{R}$, then we can tell whether $f$ is one-to-one or onto by looking at its graph.
$$
f \textnormal{ is one-to-one} \leftrightarrow \textnormal{graph of }f \textnormal{ intersects every horizontal line at most once}
$$
$$\qquad\;\, f \textnormal{ is onto}\leftrightarrow \textnormal{graph of }f \textnormal{ intersects every horizontal line at least once}$$
##### Examples

>[!example]
>$f:\mathbb{R}\to \mathbb{R},\;f(x)=3x^{3}-x$ is onto, but not one-to-one.

```tikz
\begin{document}
\begin{tikzpicture}
  % Axes
  \draw[->] (-2,0) -- (2,0) node[right] {$x$};
  \draw[->] (0,-2) -- (0,2) node[above] {$y$};
  
  % Graph of 3x^3-x
  \draw[domain=-1:1,smooth,variable=\x,blue] plot ({\x},{3*\x^3-\x});
\end{tikzpicture}
\end{document}
```


>[!example]
>$f:\mathbb{R}\to \mathbb{R},\;f(x)=x^{2}$ is not one-to one, *but* $f:\mathbb{R}^+ \to \mathbb{R}$ is one-to-one.

```tikz
\begin{document}
\begin{tikzpicture}
  % Axes
  \draw[->] (-2,0) -- (2,0) node[right] {$x$};
  \draw[->] (0,-2) -- (0,2) node[above] {$y$};
  
  % Graph of x^2
  \draw[domain=-1.5:1.5,smooth,variable=\x,blue] plot ({\x},{\x*\x});
\end{tikzpicture}

\begin{tikzpicture}
  % Axes
  \draw[->] (-2,0) -- (2,0) node[right] {$x$};
  \draw[->] (0,-2) -- (0,2) node[above] {$y$};
  
  % Graph of x^2 (R+)
  \draw[domain=0:1.5,smooth,variable=\x,blue] plot ({\x},{\x^2});
\end{tikzpicture}
\end{document}
```


>[!example]
>The **floor function** $f:\mathbb{R}\to \mathbb{R}$ is given by $f(x)=\lfloor x\rfloor=\textnormal{ greatest integers }\leq x$. It is neither onto, nor one-to-one.

```tikz
\begin{document}
\begin{tikzpicture}
  % Axes
  \draw[->] (-5,0) -- (5,0) node[right] {$x$};
  \draw[->] (0,-5) -- (0,5) node[above] {$y$};
  
  % Graph of floor function
  \foreach \x in {-4,-3,-2,-1,1,2,3,4} {
    \draw (-0.15,\x) -- (0.15,\x);
    \node[left] at (-0.15,\x - 0.15) {\x};
    \draw (\x,-0.15) -- (\x,0.15);
    \node[below] at (\x,-0.15) {\x};
    \draw[draw=blue, thick] (\x,\x) -- (\x + 1,\x);
    \draw[draw=blue,thick] (\x,\x) circle [radius=0.1];
  }
  \node at (-0.4,-0.4) {$0$};
  \draw[draw=blue, thick] (0,0) -- (1,0);
  \draw[draw=blue,thick] (0,0) circle [radius=0.1];
  % Labels
  \node at (4.5,-0.5) {$x$};
  \node at (-0.5,4.5) {$y$};
\end{tikzpicture}
\end{document}
```
