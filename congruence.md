#14-09-2023 

#### Definitions

>[!definition]
>The equivalence relation defined as
>$$a\sim b\leftrightarrow n\;\vert\;a-b\quad(n\in\mathbb{N})$$
>is called **congruence modulo** $n$ and we write
>$$a\equiv b\enspace mod\enspace n \leftrightarrow n\;\vert\;a-b$$
>The equivalence classes are called **congruence classes**. To recall, these are of the form
>$$n\mathbb{Z}+r=\{na+r\mid a\in\mathbb{Z}\}$$
>These form a partition of $\mathbb{Z}$.
>>[!example]-
>>- What is $\bar{0}$?
>>$\bar{0}=\{x\in\mathbb{Z}\mid x\equiv 0\enspace mod\enspace 5\}$
>>$x\equiv0\enspace mod\enspace 5\leftrightarrow 5\;\vert\;(x-0) \leftrightarrow 5\;\vert\;x \leftrightarrow x=5k,\enspace k\in\mathbb{Z}$
>>So $\bar{0}=5\mathbb{Z}$.
>>- More generally, $\bar{a}=5\mathbb{Z}+a$.

#### Proposition
Any integer congruent mod $n$ to its remainder when divided by $n$. It follows that there are $n$ congruence classes mod $n$, corresponding to each of these $n$ remainders, namely $n\mathbb{Z},\enspace n\mathbb{Z}+1,\enspace n\mathbb{Z}+2,\dots,n\mathbb{Z}+(n-1)$.
##### Proof
Let $a\in\mathbb{Z}$. By the [[division-algorithm|division algorithm]], $a=qn+r,\enspace 0\leq r<n$. Therefore, $a-r=qn$ and so $n\;\vert\; a-r$. Hence $a\equiv r\enspace mod\enspace n$.
Thus $a\in\bar{r}=n\mathbb{Z}+r$ (where $r=0,1,\dots,n-1$). Hence there are at most $n$ equivalence classes, namely $\bar{0},\bar{1},\dots,\overline{(n-1)}$.
Since $\equiv$ is an equivalence relation, the congruence classes $\bar{0},\bar{1},\dots,\overline{(n-1)}$ are disjoint. Therefore, there are exactly $n$ congruence classes.

>[!example]
>- Let $n=32$. To which congruence class does $258$ belong to?
>Since $258=8(32)+2,\quad 258\in\bar{2}=32\mathbb{Z}+2$.


#### Reduction
>[!definition]
>The **reduction** of an integer $x\enspace mod\enspace n$ is the remainder of $x$ after diving by $n$. We express this as $x(mod\;n)$.
>>[!example]
>>- $258(mod\;32)=2$ (previous example)
>>- $-17(mod\;3)=1$ since $-17=-6(3)+1$.
