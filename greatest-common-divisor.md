#12-09-2023 

>[!definition]
>Given $a,b\in\mathbb{Z}, b\neq 0$, we say $b$ is a **divisor** of $a$ if and only if $a=bq$ for some $q\in\mathbb{Z}$. We write $b|a$.
#### Proposition
Let $R={(a,b)\in\mathbb{N}\mid b|a}$. Then $R$ is reflexive, antisymmetric, transitive.
- $a|a\quad\forall a\in\mathbb{N}$
- $a|b$ and $b|a\to a=b$
- $a|b$ and $b|c\to a|c$ 

#### Proposition
If $c|a$ and $c|b$, then $c|(xa+yb)\quad\forall x,y\in\mathbb{Z}$.
##### Proof
$c|a$ and $c|b\to a=kc$ and $b=lc$. Therefore,$$
xa+yb=x(kc)+y(lc)=c(xk+yl)\to c|(xa+yb).
$$
#### Greatest Common Divisor (gcd)
Let $a, b\in\mathbb{Z}$, not both 0. The **greatest common divisor** of $a$ and $b$, written $g=gcd(a,b)$ is the integer satisfying:
1. $g|a$ and $g|b$
2. If $d|a$ and $d|b$, then $d\leq g$.

>[!definition]
>$a,b\in\mathbb{Z}\setminus{0}$ are **relatively prime** (coprime) if $gcd(a,b)=1$.
>>[!example]
>>- $gcd(12,-16)=4,gcd(17,0)=17$
>>- $6$ and $35$ are coprime.



^7e94d6


^e11ce0
