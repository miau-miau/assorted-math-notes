---
tags:
  - sets
  - naive-set-theory
order-tag: "0008"
date: 2023-08-29
---
#### Set Difference

>[!definition]
>The **set difference** of $A$ and $B$ ($A\setminus B$) is the [[sets|set]] of $A$ that are not in $B$.
>
>>[!example]
>>$\{ a,b,c \} \setminus \{ c,x \}=\{ a,b \}$
>>$\mathbb{Z} \setminus \{ x=2k+1\mid k\in\mathbb{Z} \}=\{2n\mid n\in\mathbb{Z}\}$

```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(0:2cm) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}
% Set A and B
\begin{tikzpicture}
    \begin{scope}
        \clip \Acircle;
        \fill[filled, even odd rule] \Bcircle \Acircle;
    \end{scope}
    \draw[outline] \Acircle \Bcircle;
    \node at (-1.7,1) {$A$};
    \node at (3.7,-1) {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \setminus B$};
\end{tikzpicture}
\end{document}
```
#### Symmetric Difference

>[!definition]
>The **symmetric difference** of $A$ and $B$ is $A\oplus B=(A\cup B)\setminus(A\cap B)$ or, equivalently, $(A\setminus B)\cup(B\setminus A)$.

```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(0:2cm) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}
% Set A and B
\begin{tikzpicture}
    \begin{scope}
        \clip \Acircle;
        \fill[filled, even odd rule] \Bcircle \Acircle;
    \end{scope}
    \begin{scope}
        \clip \Bcircle;
        \fill[filled, even odd rule] \Bcircle \Acircle;
    \end{scope}
    \draw[outline] \Acircle \Bcircle;
    \node at (-1.7,1) {$A$};
    \node at (3.7,-1) {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \oplus B$};
\end{tikzpicture}
\end{document}
```
