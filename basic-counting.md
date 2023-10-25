---
tags:
  - combinatorics
order-tag: "0061"
date: 2023-10-12
---
>[!notation]
>$|\,S\,|$ is the number of elements of [[sets-naive|set]] $S$.

Let $A$ and $B$ be [[sets-naive|sets]] of a finite [[set-complement|universal]] set $U$.
#### Basics
- Number of elements in [[set-difference#Set Difference|set difference]]:
$$|\,A\setminus B\,|=|\,A\,|-|\,A\cap B\,|$$
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

- Number of elements in [[set-complement|set complement]]:
$$|\,A^{\mathbf{c}}\,|=|\,U\setminus A\,|=|\,U\,|-|\,A\cap U\,|=|\,U\,|-|\,A\,|$$
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
- Number of elements in [[set-difference#Symmetric Difference|symmetric difference]]:
$$\begin{align}
|\,A\oplus B\,|&=|\,(A\cup B)\setminus(A\cap B)\,| \\
&=|\,A\cup B\,|-|\,A\cap B\,| \\
&=(|\,A\,|+|\,B\,|-|\,A\cap B\,|)-|\,A\cap B\,| \\
&=|\,A\,|+|\,B\,|-2|\,A\cap B\,|
\end{align}$$
- $|\,A\cap B\,|\leq \textnormal{min}\{|\,A\,|,\,|\,B\,|\}$
It is true because $|\,A\cap B\,|\leq |\,A\,|$ and $|\,A\cap B\,|\leq |\,B\,|$.

#### Unions
For number of elements in [[unions-and-intersections#Union|set union]], see [[inclusion-exclusion-principle|Inclusion-Exclusion Principle]].
In case of only 2 sets,
$$|\,A\cup B\,|=|\,A\,|+|\,B\,|-|\,A\cap B\,|$$
##### Addition Rule
If $A_{1},\,\dots,\,A_{n}$ are all disjoint sets (that is $A_{i}\cap A_{j}=\emptyset\quad\forall\,i\neq j$), then
$$
|\,A_{1}\cup A_{2}\cup\dots \cup A_{n}\,|=|\,A_{1}\,|+|\,A_{2}\,|+\dots+|\,A_{n}\,|
$$
>[!example]-
>You want to see a movie and go to trivia tonight. There are $8$ movies playing and $3$ venues hosting trivia.
>Let $A=\{ \textnormal{ movies } \},\;B=\{ \textnormal{ trivia venues } \}$.
>
>a) You don't want to get home too late, so decide you will do only one activity. How many options do you have?
>Since the events of "movie" and "trivia" are mutually exclusive, there are $|\,A\cup B\,|=|\,A\,|+|\,B\,|=8+3=11$ options.

#### [[cartesian-product-sets|Cartesian Product]]
In case of two sets,
$$|\,A\times B\,|=|\,A\,|\times |\,B\,|$$
##### Multiplication Rule
In general,
$$|\,A_{1}\times\dots\times A_{n}\,|=|\,A_{1}\,|\times |\,A_{2}\,|\times\dots\times |\,A_{n}\,|=\prod_{i=1}^n |\,A_{i}\,|$$
>[!example]-
>You want to see a movie and go to trivia tonight. There are $8$ movies playing and $3$ venues hosting trivia.
>Let $A=\{ \textnormal{ movies } \},\;B=\{ \textnormal{ trivia venues } \}$.
>
>b) You're an adult and you don't have a bedtime. You want to see a movie first, the go to trivia. How many options do you have?
>
>Your options belong to the set $A\times B$.
>Therefore, you have $|\,A\times B\,|=|\,A\,|\times |\,B\,|=8\cdot 3=24$ options.