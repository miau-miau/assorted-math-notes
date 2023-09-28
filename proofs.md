---
tags:
  - logic
  - proofs
order-tag: "0004"
aliases:
  - prove
date: 2023-08-24
---
#### How to prove
To prove a statement is true, we must prove it in general, not in a specific example.

>[!example]
>"If $f$ is differentiable, then $f$ is continuous" must be proven for all functions. Proving it only for $f=x^{2}$ is not a proof of the general fact.

However, to prove a statement is false, it is sufficient to find an example in which it is false.

>[!example]
>The statement "if $f$ is continuous, then it is differentiable" is false since $f(x)=|x|$ is continuous, but not differentiable.

Remember, when we are proving an [[logic-statements#Implication (if ..., then ...)|implication]] $A\to B$, $A$ is called the **sufficient condition** for $B$ and $B$ is called the **necessary condition** for $A$.

#### Direct Proof
To prove $A\to B$, prove a series of implications $A\to A_{1}\to\dots\to A_{x}\to B$.

>[!example]
>Let x be a real number such that $2x+1=5$. Prove that $x=2$.
>>$2x+1=5\to 2x=4\to x=2$.
>>

>[!example]-
>Prove that if $n$ is even, then $n^{2}$ is even.
>>$n$ is even $\to n=2k$ for some integer $k$
>>$\to n^{2}=(2k)^{2}=4k^{2}=2(2k^{2})$
>>$\to n^{2}$ is even.


#### Proof by cases
Breaking a proof into cases.

>[!example]
>Let $n$ be an integer, Prove that $9n^{2}+3n-2$ is even.
>>**Case 1.** $n$ is even.
>>Then $n=2k$ for some integer $k$
>>$\to 9n^{2}+3n-2=9(2k)^{2}+3(2k)-2$
>>$=36k^{2}+6k-2=2(18k^{2}+3k-1)$
>>$9n^{2}+3n-2$ is even.
>>
>>**Case 2.** $n$ is odd
>>Then $n=2k+1$ from some integer $k$
>>$\to 9n^{2}+3n-2=9(2k+1)^{2}+3(2k+1)-2$
>>$=36k^{2}+42k+10=2(18k^{2}+21k+5)$
>>$\to 9n^{2}+3n-2$ is even.


#### Proof by [[negation-of-logic-statements#Contrapositive|Contrapositive]]
Instead of proving $A\to b$, prove $\neg B\to\neg A$, which is [[negation-of-logic-statements#Theorem|logically equivalent.]]

>[!example]
>If the average of four different integers is 10, prove that at least one is greater than 11.
>>*We will prove: If four different integers are at most 11, then their average is not 10.*
>>Let $a,b,c,d$ be the integers. The largest possible average is
>>$$\frac{11+10+9+8}{4}=\frac{38}{4}=9.5<10.$$

>[!example]-
>Prove that if $n^{2}$ is even, then so is $n$.
>>*We will prove: if $n$ is odd, then $n^{2}$ is odd.*
>>$n$ is odd $\to n=2k+1$ for some integer $k$
>>$\to n^{2}=(2k+1)^{2}=4k^{2}+4k+1=2(2k^{2}+2k)+1$
>>$\to n^{2}$ is odd.

>[!example]- Comparison
>Prove that $x^{2}+y^{2}=0\leftrightarrow x=y=0$.
>>($\leftarrow$) Direct: $x=y=0\to x^{2}+y^{2}=0^{2}+0^{2}=0$
>>($\to$) Contrapositive: $x\neq 0$ or $y\neq 0\to x^{2}+y^{2}>0\neq 0$


#### Proof by Contradiction
To prove a statement $A$ true, assume $\neg A$ instead. If this assumption leads to a statement that is false, then we know $\neg A$ cannot be true. This implies that $A$ must be true.

>[!example]
>Prove that there is no largest integer.
>>Assume there is a largest integer $N$. Then $N+1\geq N$, where $N+1$ is also an integer, which is absurd. Hence there is no largest integer.

>[!example]-
>Let $a$ be  a nonzero rational number. Let $b$ be an irrational number. Prove $ab$ is irrational.
>>Assume $ab$ is rational. Then $ab=\frac{x}{y}$, where $x,y$ are integers. Since $a$ is rational, $a=\frac{p}{q}$, where $p,q$ are integers.
>>$$ab=\frac{x}{y}=\frac{p}{q}b=\frac{x}{y}\to b=\frac{xq}{yp}$$
>>This implies $b$ is rational, which contradicts the fact that $b$ is irrational. Therefore, $ab$ must be irrational/

>[!example]-
>Prove that $\sqrt{ 2 }$ is an irrational number.
>>Assume $\sqrt{ 2 }$ is rational. Then $\sqrt{ 2 }=\frac{a}{b}$, where $a,b$ is a reduced fraction (i.e. $a$ and $b$ are integers with no common factor).
>>$\sqrt{ 2 }=\frac{a}{b}\to 2=\frac{a^{2}}{b^{2}}\to 2b^{2}=a^{2}$
>>$\to a^{2}$ is even $\to a$ is even (previous example)
>>$\to a=2k$ for some integer $k\to a^{2}=(2k)^{2}=4k^{2}$
>>$\to 2b^{2}=4k^{2}\to b^{2}=2k^{2}\to b^{2}$ is even
>>$\to b$ is even.
>>But then $\frac{a}{b}$ is *not* a reduced fraction, contradicting the fact that $\frac{a}{b}$ is reduced. Thus $\sqrt{ 2 }$ is irrational.

