---
tags:
  - set-theory
order-tag: "0010"
date: 2023-08-29
---
#### De Morgan's Laws
$$a)\;(A\cup B)^{\mathsf{c}}=A^{\mathsf{c}}\cap B^{\mathsf{c}}$$
$$b)\;(A\cap B)^{\mathsf{c}}=A^{\mathsf{c}}\cup B^{\mathsf{c}}$$
See [[unions-and-intersections|unions, intersections]] and [[set-complement|complements]].
##### Proof a)
$x\in(A\cup B)^{\mathsf{c}}\leftrightarrow x\notin A\cup B \leftrightarrow \neg(x\in A\cup B)\leftrightarrow$
$\neg(x\in A \lor x\in B) \leftrightarrow$ (see [[negation-of-logic-statements#Negation of logic-statements OR statement (disjunction) disjunction|negation of or statement]])
$x\notin A \land x\notin B\leftrightarrow x\in A^{\mathsf{c}}\cap B^{\mathsf{c}}$.
Hence $(A\cup B)^{\mathsf{c}}=A^{\mathsf{c}}\cap B^{\mathsf{c}}$.

##### Proof b)
$x\in(A\cap B)^{\mathsf{c}}\leftrightarrow x\notin A\cap B\leftrightarrow\neg(x\in A\cap B)\leftrightarrow$
$\neg(x\in A \land x\in B) \leftrightarrow$
$x\notin A \lor x\notin B\leftrightarrow x\in A^{\mathsf{c}}\cap B^{\mathsf{c}}$
Hence $(A\cap B)^{\mathsf{c}}=A^{\mathsf{c}}\cap B^{\mathsf{c}}$.
#### Venn diagrams
```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(2,0) circle (1.5cm)}
\def\Ccircle{(0,0) circle (3.6cm)}
\def\Dcircle{(2,0) circle (3.6cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\setlength{\parskip}{5mm}

\begin{tikzpicture}
\begin{scope}
        \clip \Ccircle;
        \fill[fill=blue!30, fill opacity = 0.5, even odd rule] \Acircle \Ccircle;
\end{scope}
    \draw[draw=circle edge, thick] \Acircle \Bcircle;
    \draw[draw opacity=0] \Ccircle \Dcircle;
    \node at (0,0) {$A$};
    \node at (2,0) {$B$};
    \node at (-1.3,1.3) {$A^{\mathsf{c}}$};
    \node at (3.3,1.3) {$B^{\mathsf{c}}$};

\begin{scope}
        \clip \Dcircle;
        \fill[fill=blue!30, fill opacity = 0.5, even odd rule] \Bcircle \Dcircle;
\end{scope}
    \draw[draw=circle edge, thick] \Acircle \Bcircle;
    \draw[draw opacity=0] \Ccircle \Dcircle;
    \node at (0,0) {$A$};
    \node at (2,0) {$B$};
    \node at (-1.3,1.3) {$A^{\mathsf{c}}$};
    \node at (3.3,1.3) {$B^{\mathsf{c}}$};
    \node[anchor=south] at (current bounding box.north) {$A^{\mathsf{c}}, B^{\mathsf{c}}$};
\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(2,0) circle (1.5cm)}
\def\Ccircle{(0,0) circle (3.7cm)}
\def\Dcircle{(2,0) circle (3.7cm)}

\colorlet{circle edge}{pink}
\colorlet{circle area}{pink!20}

\tikzset{
    invclip/.style={
        clip,
        insert path={{[reset cm](-16383.99999pt,-16383.99999pt) rectangle (16383.99999pt,16383.99999pt)}}
    }
}

\setlength{\parskip}{5mm}

\begin{tikzpicture}
    \draw[draw=circle edge, thick] \Acircle \Bcircle;
    \draw[draw opacity=0] \Ccircle \Dcircle;
    \node at (0,0) {$A$};
    \node at (2,0) {$B$};
	\begin{pgfinterruptboundingbox}
        \path [invclip] \Acircle;
        \path [invclip] \Bcircle;
    \end{pgfinterruptboundingbox}
	\begin{scope}
	    \clip \Ccircle;
	    \draw[fill=blue!30, fill opacity = 0.5, draw opacity = 0] \Dcircle;
    \end{scope}
    \node at (-1.3,1.3) {$A^{\mathsf{c}}$};
    \node at (3.3,1.3) {$B^{\mathsf{c}}$};
    \node[anchor=south] at (current bounding box.north) {$A^{\mathsf{c}}\cap B^{\mathsf{c}}=(A\cup B)^{\mathsf{c}}$};
\end{tikzpicture}
\end{document}
```

```tikz
\begin{document}

% Definition of circles
\def\Acircle{(0,0) circle (1.5cm)}
\def\Bcircle{(2,0) circle (1.5cm)}
\def\Ccircle{(0,0) circle (3.7cm)}
\def\Dcircle{(2,0) circle (3.7cm)}

\tikzset{
    invclip/.style={
        clip,
        insert path={{[reset cm](-16383.99999pt,-16383.99999pt) rectangle (16383.99999pt,16383.99999pt)}}
    }
}

\setlength{\parskip}{5mm}

\begin{tikzpicture}
	\begin{scope}
		\clip \Acircle;
		\draw[fill=blue!30, fill opacity = 0.5, even odd rule] \Acircle \Bcircle;
	\end{scope}
    \begin{scope}
		\clip \Bcircle;
		\draw[fill=blue!30, fill opacity = 0.5, even odd rule] \Bcircle \Acircle;
	\end{scope}
	\draw[draw=pink, thick] \Acircle \Bcircle;
    \draw[draw opacity=0] \Ccircle \Dcircle;
    \node at (0,0) {$A$};
    \node at (2,0) {$B$};
	\begin{pgfinterruptboundingbox}
        \path [invclip] \Acircle;
        \path [invclip] \Bcircle;
    \end{pgfinterruptboundingbox}
	\draw[fill=blue!30, fill opacity = 0.5, draw opacity = 0] \Ccircle \Dcircle;
    \node at (-1.3,1.3) {$A^{\mathsf{c}}$};
    \node at (3.3,1.3) {$B^{\mathsf{c}}$};
    \node[anchor=south] at (current bounding box.north) {$A^{\mathsf{c}}\cup B^{\mathsf{c}}=(A\cap B)^{\mathsf{c}}$};
\end{tikzpicture}
\end{document}
```
