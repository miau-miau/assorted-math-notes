---
tags:
  - sets
  - naive-set-theory
order-tag: "0016"
date: 2023-08-31
---
>[!definition]
>A [[binary-relation|binary relation]] is **transitive** if
>$$(a,b)\in R \land (b,c)\in R\to (a,c)\in R$$
>
>>[!example]
>>$R=\{ (x,y)\in\mathbb{R}\mid x\leq y \}$ is transitive, since
>>$(a,b),(b,c)\in R\to a\leq b \land b\leq c$
>>$\to a\leq c\to(a,c)\in R$.

>[!example]- More examples
>- $R=\left\{  (a,b)\in\mathbb{Z}\mid \frac{a}{b}\in \mathbb{Z}\right\}$ is transitive since
>$(a,b),(b,c)\in R\to \frac{a}{b}, \frac{b}{c}\in \mathbb{Z}$
>$\to \frac{a}{b} * \frac{b}{c}=\frac{a}{c}\in \mathbb{Z}\to(a,c)\in\mathbb{Z}$.
>- $R=\{ (x,y)\in\mathbb{R}\mid x^{2}=y \}$ is not transitive since
>$(2,4),(4,16)\in\mathbb{R})$, but $(2,16)\notin R\quad(2^{2}\neq 16)$.

