---
tags:
  - combinatorics
order-tag: "0066"
date: 2023-10-19
aliases:
  - permutation
---
>[!definition]
>A **permutation** of a [[sets-naive|set]] of $n$ distinct elements is an arrangement of them in some order.
>The number of permutations of $n$ elements is $n!$
>>[!example]
>>In how many ways can five people stand in a line?
>>
|                    | 1st person | 2nd person | 3rd | 4th | 5th |
| ------------------ | ---------- | ---------- | --- | --- | --- |
| # of possibilities | 5          | 4          | 3   | 2   | 1   |
>> $\implies 5\cdot 4\cdot 3\cdot 2 \cdot 1=5!$ ways

#### R-permutation
>[!definition]
>An **r-permutation** of a set of $n$ distinct elements is a permutation of $r$ of them.
>The number of **r-permutations** of $n$ elements is
>$$\frac{n!}{(n-r)!}=n(n-1)\dots(n-r+1)$$
>*Notation:* $\textnormal{P}(n,r)=\frac{n!}{(n-r)!}$
>>[!example]
>>In a room of 100 people, 5 are chosen to stand in a line. How many ways can these people be chosen?
>>
|                    | 1st person | 2nd person | 3rd | 4th | 5th |
| ------------------ | ---------- | ---------- | --- | --- | --- |
| # of possibilities | 100        | 99         | 98  | 97  | 96  |

An n-permutation of $n$ elements is simply a permutation.

#### Important
In permutation problems:
- elements are distinct
- order matters

>[!example]
>Suppose license plates in some state use 5 distinct letters. How many different license plates are possible?
>$$\textnormal{P}(26,5)=\frac{26!}{(26-5)!}=26\cdot 25\cdot 24\cdot 23\cdot 22=7893600$$
>What if repeated letters are allowed?
>$$26^5=11881376$$

>[!example]
>In how many ways can 10 adults and 5 children stand in a line so that no two children are standing next to each other?
>
>First, there are $10!$ ways to arrange 10 adults in a line. Now there are 11 spots in which the children can be placed:
>$$\textnormal{\_ Adult \_ Adult \_ ... \_ Adult \_}$$
>So there are $\textnormal{P}(11,5)$ ways to arrange children. Altogether, we have $10!\textnormal{P}(11,5)$ arrangements.