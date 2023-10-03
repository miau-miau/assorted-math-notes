---
tags:
  - sets
  - naive-set-theory
order-tag: "0014"
date: 2023-08-31
---

>[!definition]
>A [[binary-relation|binary relation]] on $A$ is **symmetric** if
>$$(a,b)\in R \to (b,a)\in R$$
>
>>[!example]
>>$R=\{ (x,y)\in\mathbb{R}\mid x\leq y \}$ is not symmetric,
>>since $(2,3)\in R$ ($2\leq 3$),
>>but $(3,2)\notin R$ ($3\not\leq 2$).

>[!example]- More examples
>- $R=\{ (x,y)\in\mathbb{R}\mid x^{2}+y^{2}=1 \}$ is symmetric,
>since $(a,b)\in R\to a^{2}+b^{2}=1\to b^{2}+a^{2}=1\to(b,a)\in R$.
>- $R=\{ (x,y)\in\mathbb{N}\mid x-y$ is even $\}$ is symmetric,
>since $(a,b)\in R\to(a-b)$ is even $\to -(a-b)=b-a$ is even $\to(b,a)\in R$.
##### Geometry
A binary relation on $\mathbb{R}$ is symmetric of the associated graph is symmetric about $y=x$.
For example, $R={(x,y)\in\mathbb{R}\mid x^{2}+y^{2}=1}$ is symmetric.

```tikz
\begin{document}
\begin{tikzpicture}
  \draw[->, thick] (-3,0) -- (3,0);
  \draw[->, thick] (0,-3) -- (0,3);
  \draw[draw=pink, thick] (0,0) circle [radius=2cm];
  \draw[domain=-2.5:2.5, dashed] plot (\x,\x) node[right]{$y=x$};
\end{tikzpicture}
\end{document}
```
