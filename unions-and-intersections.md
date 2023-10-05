---
tags:
  - set-theory
order-tag: "0007"
date: 2023-08-29
---
#### Union

>[!definition]
>The **union** of $A$ and $B$ ($A\cup B$) is the set of elements in $A$ *or* in $B$.
>$$x\in A\cup B \leftrightarrow x\in A \lor x\in B$$
>>[!example]
>>$A=\{ a,b,c,d \},\;B=\{ x,y,z,a,b \},\;C=\{ c,d,q \}$
>>$A\cup B=\{ a,b,c,d,x,y,z \}$
>>$B\cap C=\{ x,y,z,a,b,c,d,q \}$
>>$A\cap C=\{ a,b,c,d,q \}$

```tikz
\begin{document}

% Definition of circles
\def\firstcircle{(0,0) circle (1.5cm)}
\def\secondcircle{(0:2cm) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}

% Set A or B
\begin{tikzpicture}
    \draw[filled] \firstcircle node at (-1.7,1){}
                  \secondcircle node at (3.7,-1){};
    \node at (-1.7,1) {$A$};
    \node at (3.7,-1) {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \cup B$};
\end{tikzpicture}

\end{document}

```
#### Intersection

>[!definition]
>The **intersection** of $A$ and $B$ ($A\cap B$) is the set of elements that belong to both $A$ and $B$.
>$$x\in A\cap B\leftrightarrow x\in A \land x\in B$$
>
>>[!example]
>>$A=\{ a,b,c,d \},\;B=\{ x,y,z,a,b \},\;C=\{ c,d,q \}$
>>$A\cap B=\{ a,b \}$
>>$B\cap C=\emptyset$
>>$A\cap C=\{ c,d \}$

```tikz
\begin{document}

% Definition of circles
\def\firstcircle{(0,0) circle (1.5cm)}
\def\secondcircle{(0:2cm) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}
% Set A and B
\begin{tikzpicture}
    \begin{scope}
        \clip \firstcircle;
        \fill[filled] \secondcircle;
    \end{scope}
    \draw[outline] \firstcircle \secondcircle;
    \node at (-1.7,1) {$A$};
    \node at (3.7,-1) {$B$};
    \node[anchor=south] at (current bounding box.north) {$A \cap B$};
\end{tikzpicture}
\end{document}
```
#### Properties

##### Associativity
$\cup$ and $\cap$ are **associative**:
$$(A\cup B)\cup C=A\cup(B\cup C)$$
$$(A\cap B)\cap C=A\cap(B\cap C)$$
So we just write $A\cup B\cup C$ and $A\cap B\cap C$.

##### Property
$A\cap B=A$ if and only if $A\subseteq B$.
###### Proof
($\rightarrow$) Let $A\cap B=A$.
Then $x\in A\to x\in A\cap B\to x\in B$.
Thus $A\subseteq B$.
($\leftarrow$) Let $A\subseteq B$.
To show $A\cap B=A$, we will show $A\subseteq A\cap B$ [[sets-naive#Proposition|and]] $A\cap B\subseteq A$.
- $x\in A\to x\in B\to (x\in A\land x\in B)\to x\in A\cap B$. Thus $A\subseteq B$.
- $x\in A\cap B\to x\in A$. Thus $A\cap B\subseteq A$.

Venn diagrams can help visualize properties.
##### Property (intersection and union)
For any sets $A$, $B$, and $C$, $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$

###### Proof (not rigorous)
Venn diagrams help visualize properties. Let's look at the left side:

```tikz
\begin{document}

% Definition of circles
\def\firstcircle{(0,0) circle (1.5cm)}
\def\secondcircle{(2,0) circle (1.5cm)}
\def\thirdcircle{(1,1.5) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}

% B or C
\begin{tikzpicture}
    \draw[filled] \thirdcircle \secondcircle;
    \draw[outline] \firstcircle;
    \node at (-0.5,-0.5) {$A$};
    \node at (2.5,-0.5) {$B$};
    \node at (1,2.3) {$C$};
    \node[anchor=south] at (current bounding box.north) {$B\cup C$};
\end{tikzpicture}

\hspace{1cm}

%A and (B or C)
\begin{tikzpicture}
	\begin{scope}
        \clip \firstcircle;
        \fill[filled] \secondcircle \thirdcircle;
    \end{scope}
    \draw[outline] \firstcircle \secondcircle \thirdcircle;
    \node at (-0.5,-0.5) {$A$};
    \node at (2.5,-0.5) {$B$};
    \node at (1,2.3) {$C$};
    \node[anchor=south] at (current bounding box.north) {$A \cap (B\cup C)$};
\end{tikzpicture}

\end{document}
```

At the same time,
```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(2,0) circle (1.5cm)}
\def\Ccircle{(1,1.5) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}

% A and B
\begin{tikzpicture}
    \begin{scope}
        \clip \Bcircle;
        \fill[filled] \Acircle;
    \end{scope}
    \draw[outline] \Acircle \Bcircle \Ccircle;
    \node at (-0.5,-0.5) {$A$};
    \node at (2.5,-0.5) {$B$};
    \node at (1,2.3) {$C$};
    \node[anchor=south] at (current bounding box.north) {$A\cap B$};
\end{tikzpicture}

\hspace{1cm}

%A and C
\begin{tikzpicture}
	\begin{scope}
        \clip \Ccircle;
        \fill[filled] \Acircle;
    \end{scope}
    \draw[outline] \Acircle \Bcircle \Ccircle;
    \node at (-0.5,-0.5) {$A$};
    \node at (2.5,-0.5) {$B$};
    \node at (1,2.3) {$C$};
    \node[anchor=south] at (current bounding box.north) {$A \cap C$};
\end{tikzpicture}

\end{document}
```

Combining these two,
```tikz
\begin{document}

% Definition of circles
\def\firstcircle{(0,0) circle (1.5cm)}
\def\secondcircle{(2,0) circle (1.5cm)}
\def\thirdcircle{(1,1.5) circle (1.5cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{filled/.style={fill=circle area, fill opacity = 0.5, draw=circle edge, thick},
    outline/.style={draw=circle edge, thick}}

\setlength{\parskip}{5mm}

%(A or B) (A or C)
\begin{tikzpicture}
	\begin{scope}
        \clip \firstcircle;
        \fill[filled] \secondcircle \thirdcircle;
    \end{scope}
    \draw[outline] \firstcircle \secondcircle \thirdcircle;
    \node at (-0.5,-0.5) {$A$};
    \node at (2.5,-0.5) {$B$};
    \node at (1,2.3) {$C$};
    \node[anchor=south] at (current bounding box.north) {$(A\cup B)\cup(A\cup C)$};
\end{tikzpicture}

\end{document}
```
