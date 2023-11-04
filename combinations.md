---
tags:
  - combinatorics
order-tag: "0068"
date: 2023-10-19
---
>[!definition]
>A **combination** of a set of objects is a subset of them. A subset of $r$ objects is called an **r-combinations** or a combination of the objects taken $r$ at a time.
>The number of **r-combinations** of $n$ objects is
>$$\frac{n!}{(n-r)!\,r!}$$
>*Notation*: read "n choose r", "binomial coefficient"
>$$C_{n}^r=\binom{n}{r}=\frac{n!}{(n-r)!\,r!}$$
>>[!example]-
>>You flip a coin 8 times. In how many ways can you get 5 heads?
>>The order in which we flip heads doesn't matter. So there are
>>$$\binom{8}{5}=\frac{8!}{5!\,3!}=56\textnormal{ ways}$$
#### Important
In combination problems,
- objects are distinct
- order does not matter

>[!example]
>The car sits five people (owner included). In how many ways can the owner choose 4 colleagues from the math department (out of 20) to join me for lunch?
>
>The order in which I choose 4 colleagues does not matter, so
>$$\binom{20}{4}=\frac{20!}{(20-4)!\,4!}=4845\textnormal{ ways}$$

>[!example]
>How many groups of 5 animals can be chosen from 12 dogs and 20 cats if we must choose exactly 3 cats?
>
>We need to choose 3 cats out of 2at least0. There are $\binom{20}{3}=1140$ ways. For each of these choices, we need to choose 2 dogs out of 12. There are $\binom{12}{2}=66$ ways to do this.
>All together, we have $1140\cdot 66=75240$ possible groups.
>
>>[!faq] What if?
>>What if we can have *at least* 3 cats?
>>$$\begin{align}
\textnormal{\# groups}&=(\textnormal{\# with 3 cats})+(\textnormal{\# with 4 cats})+(\textnormal{\# with 5 cats}) \\
&=\binom{20}{3}\binom{12}{2}+\binom{20}{4}\binom{12}{1}+\binom{20}{5}\binom{12}{0} \\
&=148884
\end{align}$$
