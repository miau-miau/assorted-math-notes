---
tags:
  - algorithms
order-tag: "0047"
date: 2023-09-26
aliases:
  - algorithm
---
>[!definition]
>An algorithm is a systematic process by which a task is completed.
>>[!example]
>>In grade school, you learned algorithms to add, subtract, multiply, and divide natural numbers.

Such systematic processes allow us to write programs that can quickly carry out these tasks.

>[!example]
>Create an algorithm that adds $n$ integers $a_{1},a_{2},\dots,a_{n}$.
>How might we do this by hand?
>Evaluate $5+3+2+7$.
>$5+3=8$
>$8+2=10$
>$10+7=17$
>So $5+3+2+7=17$.
>
>**Algorithm:**
>1. Let $S=0$ (sum)
>2. For $1\leq i\leq n$, replace $S$ by $S+a_{i}$.
>3. Output $S$.

#### Efficiency
In general, there can be more than one algorithm that completes the same task. However, one might be quicker (e.g. it requires less steps).

>[!example]
>Given $a_{0},a_{1},\dots,a_{n},\;x\in\mathbb{Z}$, output $a_{0}+a_{1}x+\dots+a_{n}x^n$.
>
>**Method 1**.
>Compute $x,x^1,x^2,\dots ,x^n$ and then $a_{0}+a_{1}x^1,a_{0}+a_{1}x^1+a_{2}x^2,\dots,a_{0}+a_{1}x+\dots+a_{n}x^n$
>
>**Algorithm:**
>1. For $i=1$ to $n$, set $x_{i}=x^i$
>2. Set $S=a_{0}$
>3. For $i=1$ to $n$, replace $S$ by $S+a_{i}x_{i}$
>4. Output $S$.
>   
>This requires $3n$ calculations and storing a lot of information ($x_{1},\dots,x_{n}$).
>
>**Method 2.**
>In contrast, [[horners-algorithm|Horner's algorithm]] requires only $2n$ computations and no storage requirements. It is more efficient than method 1.

We will measure how efficient algorithms are in the future.
