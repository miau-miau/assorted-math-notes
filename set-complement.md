---
tags:
  - set-theory
order-tag: "0009"
date: 2023-08-29
aliases:
  - complement
---
#### Complement

>[!definition]
>The **complement** of a [[sets-naive|set]] $A$ ($A^{\mathsf{c}}$) is $U\setminus A$, where $U$ is some universal set made clear by context.
>
>>[!example]
>>- $\{ \textnormal{ Mon, Tue, Wed, Thu, Fri, Sat }\}^{\mathsf{c}}=\{ \textnormal{ Sun }\}$. The universal set is days of the week.
>>- $A=\{ 1,2,5,6,\dots \}^{\mathsf{c}}=\{ 3,4 \},\;U=\mathbb{N}$

```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(0,0) circle (3cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}
\colorlet{outside area}{blue!30}

\setlength{\parskip}{5mm}
% Set A and B
\begin{tikzpicture}
    \draw[fill=circle area, fill opacity = 0.5, draw=circle edge, thick] \Acircle;
    \draw[fill=circle area, fill opacity = 0, draw opacity=0] \Bcircle;
    \node at (0,0) {$A$};
\end{tikzpicture}

\begin{tikzpicture}
\begin{scope}
        \clip \Bcircle;
        \fill[fill=outside area, fill opacity = 0.5, even odd rule] \Acircle \Bcircle;
\end{scope}
    \draw[draw=circle edge, thick] \Acircle;
    \draw[draw opacity=0] \Bcircle;
    \node at (0,0) {$A$};
    \node at (-1.3,1.3) {$A^{\mathsf{c}}$};
\end{tikzpicture}
\end{document}
```
