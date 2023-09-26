#12-09-2023

>[!definition]
>Let $A$ be a set and let $*$ be an operation on $A$ (e.g. addition). We say that A is **closed under $*$** if:
>$$a,b\in A\to a*b\in A.$$
>>[!example]-
>>1. $\mathbb{Z}$ is closed under $+$, $-$, $*$ since given any $a,b\in\mathbb{Z}$, $a+b\in \mathbb{Z}$, $a*b\in \mathbb{Z}$, $a-b\in \mathbb{Z}$. However, $\mathbb{Z}$ is not closed under division since $2,3\in \mathbb{Z}$ but $\frac{2}{3}\notin \mathbb{Z}$.
>>2. $A=\{odd\ integers\}$ is not closed under $+$ since $1,3\in A$ but $1+3=4\notin A$.
#### The Well-Ordering Principle
Any nonempty subset of $\mathbb{N}$ has a smallest element.
- useful in proofs

#### Division Algorithm
We know how to divide integers.
$17$ divided by $3$ is $5$ plus remainder $2$ (a.k.a. $5 \frac{2}{3}$).
That is, $17=5(3)+2$, where $5$ is *quotient*, and 2 is a *remainder*.

##### Theorem (Division Algorithm)
Let $a,b\in \mathbb{Z}, b\neq 0$. Then $\\\exists$ unique integers $q$ and $r$ with $0\leq r<|b|$ such that $a=qb+r$.
###### Proof
We will prove the case in which $a,b>0$.

1. Existence ($\exists q,r$ with $0\leq r<b$ such that $a=qb+r$)
Let $A=\{kb\mid kb>a\}$.  By the well-ordering principle, $A$ has a smallest element. Call it $(q+1)b$.
Then $qb\leq a<(q+1)b$.
Set $r=a-qb$, where $r\geq 0$ since $a\geq qb$.
Since $(q+1)b>a$, we have $b>a-qb=r$.
Thus $a=qb+r$, where $0\leq r<b$.

2. Uniqueness ($q$ and $r$ are unique)
Let $q',r'$ be integers such that $0\leq r'<b$ and $a=q'b+r'$.
Then $a=q'b+r'=qb+r\implies b(q'-q)=r-r'$.
Now $$
-b<r-r'<b\implies-b<(q'-q)b<b\implies q'-q=0.
$$
Hence $q'=q$ and $r'=r$.

>[!example]
>- $a=17, b=3\to_{1}7=5(3)+2$
>Notice, $q=5=\lfloor\frac{17}{3}\rfloor$.
>- $a=17, b=-3\to17=-5(3)+1$
>Here, $q=-5=\lceil\frac{17}{3}\rceil$.

##### Proposition
If $a=qb+r$, where $0\leq r<\mid b\mid$, then $$
q=\lfloor \frac{a}{b} \rfloor, b>0
$$$$
q=\lceil \frac{a}{b} \rceil, b<0
$$