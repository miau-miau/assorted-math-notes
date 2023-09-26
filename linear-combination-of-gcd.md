#14-09-2023 #number_theory

#### Bézout's lemma
There exists $x,y\in\mathbb{Z}$ such that $gcd(a,b)=ax+by$.

We can use the [[euclidean-algorithm|Euclidean algorithm]] backwards to write $gcd(a,b)$ as a **linear combination** of a and b, i.e. $gcd(a,b)=ax+by$ for some $x,y\in\mathbb{Z}$.

>[!example]-
>Write $14$ as a linear combination of 630 and 196 (i.e. find $x,y\in\mathbb{Z}$ such that $14=630x+196y$).
>$630=3*196+42$
>$196=4*42+28$
>$42=1*28+14$
>$28=2*14+0$
>Now working from top to bottom, write each remained as linear combo of $630$ and $196$.
>$42=1*630-3*196$
>$28=1*196-4*42=1*196-4(1*630-3*196)=13*196-4*630$
>$14=42-1*28=1*630-3*196-1(13*196-4*630)=5*630-16*196\implies$ $\implies14=(5)*630+(-16)*196$