---
tags:
  - combinatorics
order-tag: "0062"
date: 2023-10-12
---
If $A_{1},\,\dots,\,A_{n}$ are finite sets, then
$$\begin{align}
|\,A_{1}\cup A_{2}\cup\dots \cup A_{n}\,|=&\sum_{i}|\,A_{i}\,|-\sum_{i<j}|\,A_{i}\cap A_{j}\,| \\
&+\sum_{i<j<k}|\,A_{i}\cap A_{j}\cap A_{k}\,|+\dots (-1)^{n+1}|\,A_{1}\cap A_{2}\cap\dots \cap A_{n}\,|
\end{align}$$
#### Useful Cases
1. $|\,A\cup B\,|=|\,A\,|+|\,B\,|-|\,A\cap B\,|$
```tikz
\begin{document}

% Definition of circles
\def\firstcircle{(0,0) circle (1.5cm)}
\def\secondcircle{(0:2cm) circle (1.5cm)}

\setlength{\parskip}{5mm}

% Set A or B
\begin{tikzpicture}
    \draw[fill=blue!30, fill opacity=0.5] \firstcircle node at (-1.7,1){};
    \draw[fill=red!30, fill opacity=0.5,draw=black,thick] \secondcircle node at (3.7,-1){};
    \draw[draw=black,thick] \firstcircle node at (-1.7,1){};
    \node at (-1.7,1) {$A$};
    \node at (3.7,-1) {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \cup B$};
\end{tikzpicture}

\end{document}

```

2. $|\,A\cup B\cup C\,|=|\,A\,|+|\,B\,|+|\,C\,|-|\,A\cap B\,|-|\,A\cap C\,|-|\,B\cap C\,|+|\,A\cap B\cap C\,|$
#### Examples
>[!example]
>How many integers between $1$ and $300$ (inclusive) are divisible by $3,\,5$ or $7$?
>
>Let $A=\{ n\mid 1\leq n\leq 300 \textnormal{ and } 3|n\}$
>$\quad\;\;\, B=\{ n\mid 1\leq n\leq 300 \textnormal{ and } 5|n\}$
>$\quad\;\;\, C=\{ n\mid 1\leq n\leq 300 \textnormal{ and } 7|n\}$
>
>We need to figure out $|\,A\cup B\cup C\,|$.
>$|\,A\cup B\cup C\,|=|\,A\,|+|\,B\,|+|\,C\,|-|\,A\cap B\,|-|\,A\cap C\,|-|\,B\cap C\,|+|\,A\cap B\cap C\,|$
>
>Using [[application-of-counting-in-divisibility|this strategy]], 
>$|\,A\,|=\lfloor \frac{300}{3} \rfloor=100, \;|\,B\,|=\lfloor \frac{300}{5} \rfloor=20,\;|\,C\,|=\lfloor \frac{300}{7} \rfloor=42$
>$|\,A\cap B\,|=\lfloor \frac{300}{15} \rfloor=20,\;|\,A\cap C\,|=\lfloor \frac{300}{21} \rfloor=14,\;|\,B\cap C\,|=\lfloor \frac{300}{35} \rfloor=8$
>$|\,A\cap B\cap C\,|=\lfloor \frac{300}{105} \rfloor=2$
>$\implies |\,A\cup B\cup C\,|=100+20+42-20-14-8+2=162$



