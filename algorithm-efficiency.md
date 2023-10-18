---
tags:
  - algorithms
order-tag: "0051"
date: 2023-09-26
---
Let $A$ and $B$ be [[algorithms-introduction|algorithms]] that complete the same task and let $f$ and $g$ be their [[complexity-function|complexity functions]].
- If $f\prec g$ (see [[function-order|function order]]), then $A$ is more efficient
- If $f\asymp g$, then $A$ and $B$ are considered similarly efficient
- If $f\asymp n$, then $A$ is said to be **linear** and run in linear time
- If $f\asymp n^a\;(a>1)$, $A$ is said to be **polynomial** and run in polynomial time
- If $f\asymp \log n$, $A$ is said to be **logarithmic** and run in logarithmic time
- If $f\asymp b^n\;(b>1)$, $A$ is said to be **exponential** and run in exponential time

In order of efficiency:
*logarithmic* is more efficient than
*linear* which is more efficient than
*polynomial* which more efficient than 
*exponential*
(see [[function-order#Other useful examples|useful examples in function order]])

>[!examples]
>The [[euclidean-algorithm|Euclidean Algorithm]] applied to $a$ and $b$ runs in $\log b$ time, so it is *very* efficient. This is why lately we used it so much to create systematic ways to solve problems.

