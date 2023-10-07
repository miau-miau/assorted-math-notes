---
tags:
  - functions-and-maps
order-tag: "0026"
date: 2023-09-07
---
>[!definition]
>Suppose $f:A\to B$ is [[surjective-and-injective-functions|onto and one-to-one]]. Then the **inverse of** $f$ is the [[sets-naive|set]]
>$$f^{-1}=\{ (b,a)\mid (a,b)\in f \}$$
>
>>[!example]
>>$A=\{ 1,2,3,4 \},\;B=\{ x,y,z,w \}$
>>- $f=\{ (1,x),(2,y),(3,z),(4,w) \}$
>>Notice that $f$ is one-to-one since different elements of $A$ have different images. It is also onto.
>>$f^{-1}=\{ (x,1),(y,2),(z,3),(w,4) \}$
>>- $f=\{ (1,x),(2,y),(3,z),(4,x) \}$ is not one-to-one since $f(1)=f(4)=x$.
>>The set $\{ (x,1),(y,2),(z,3),(x,4) \}$ is not a [[functions|function]] (so no inverse exists).
>
>Written differently, $f(a)=b\leftrightarrow a=f^{-1}(b)$.

>[!example]- Worked example
>Define $f:\mathbb{R}\to \mathbb{R}$ by $f(x)=2x-3$. Find $f^{-1}$.
>The inverse is given by $y=f^{-1}(x)$.
>Rewriting, $f(y)=x\leftrightarrow 2y-3=x\leftrightarrow y=\frac{x+3}{2}$.
>So $f^{-1}=\frac{x+3}{2}$.

#### Geometric interpretation
$f$ is the reflection of $f^{-1}$ about $y=x$.

>[!example]
>$f:\mathbb{R}\to\mathbb{R}^+,\;f(x)=3^x$ has inverse
>$f^{-1}(x)=\log_{3}x$. Notice $f^{-1}:\mathbb{R}^+ \to \mathbb{R}$.

```tikz
\begin{document}
\begin{tikzpicture}
  % Axes
  \draw[->] (-2, 0) -- (4, 0) node[right] {$x$};
  \draw[->] (0, -2) -- (0, 4) node[above] {$y$};
  
  % Graph of f(x) = 3^x
  \draw[domain=-2:3,smooth,variable=\x,blue!60] plot ({\x},{3^(\x/2)}) node[right] {$f(x) = 3^x$};
  
  % Graph of f^{-1}(x) = log_3(x)
  \draw[domain=-2:3,smooth,variable=\x,red!60] plot ({3^(\x/2)},{\x}) node[above right] {$f^{-1}(x) = \log_3(x)$};
  
  % y = x line
  \draw[dashed] (-1, -1) -- (4, 4) node[above left] {$y = x$};
\end{tikzpicture}
\end{document}
```

>[!example]
>$f=\mathbb{R}^+ \to \mathbb{R}^+,\;f(x)=x^{2}$ has inverse
>$f^{-1}=\sqrt{ x }$.


```tikz
\begin{document}
\begin{tikzpicture}
  % Axes
  \draw[->] (0, 0) -- (4, 0) node[right] {$x$};
  \draw[->] (0, 0) -- (0, 4) node[above] {$y$};
  
  % Graph of f(x) = 3^x
  \draw[domain=0:2,smooth,variable=\x,blue!60] plot ({\x},{\x^2}) node[right] {$f(x) = x^2$};
  
  % Graph of f^{-1}(x) = log_3(x)
  \draw[domain=0:2,smooth,variable=\x,red!60] plot ({\x^2},{\x}) node[above right] {$f^{-1}(x) = \sqrt{x}$};
  
  % y = x line
  \draw[dashed] (0, 0) -- (4, 4) node[above right] {$y = x$};
\end{tikzpicture}
\end{document}
```

#### Proposition
If $f:A\to B$ is one-to-one and onto, then $f^{-1}:B\to A$ is one-to-one and onto.