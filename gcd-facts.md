#14-09-2023 

We can use [[linear-combination-of-gcd|Bézout's lemma]] to prove various things about divisibility.

#### Proposition
If $d|a$ and $d|b$, then $d|gcd(a,b)$.
##### Proof
Let $g=gcd(a,b)$. Then $\\\exists m,n\in\mathbb{Z}$ such that $g=am+bn$. Since $d|a$ and $d|b$, $d|am+bn$. Hence $d|g$.

#### Proposition
Let $a$ and $b$ be relatively prime.
	a) if $a|bx$, then $a|x$.
	b) if $a|c$ and $b|c$, then $ab|c$. ^c9e685
##### Proof a)
Since $a$ and $b$ are [[greatest-common-divisor#^7e94d6|relatively prime]], $gcd(a,b)=1$. Thus $\\\exists m,n\in\mathbb{Z}$ such that $1=am+bn\implies x=xam+xbn$. Since $a|bx$, $bx=ka$ for some $k\in\mathbb{Z}$. Therefore, $x=xam+kan=a(xm+kn)\implies a|x$.
##### Proof b)
Since $a$ and $b$ are relatively prime, $gcd(a,b)=1$. Thus $\\\exists m,n\in\mathbb{Z}$ such that $1=am+bn\implies c=cam+cbn$. Since $a|c$ and $b|c$, $c=pa, p\in\mathbb{Z}$ and $c=qb, q\in\mathbb{Z}$. Therefore, $c=qbam+pabn=ab(qm+pn)\implies ab|c$.
