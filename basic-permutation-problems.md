---
tags:
  - combinatorics
  - worked-example
order-tag: "0067"
date: 2023-10-17
---
Recall the [[permutations|permutation]] formula.

>[!example]
>How many numbers between $1000$ and $9999$ inclusive do not have repeating digits?
>Let's go left to right.
>The first digit can be from $1$ to $9$ (so it has $9$ choices).
>The second digit can be from $0$ to $9$, but cannot be the same as first (so it has $9$ choices).
>The third can be from $0$ to $9$, but cannot be the same as the first or second (so there are $8$ choices).
>The fourth can be from $0$ to $9$, but cannot be the same as the first three (so there are $7$ choices).
>By the [[basic-counting#Multiplication Rule|multiplication rule]], there are $9\cdot 9\cdot 8\cdot 7=4536$ choices.

to be continued