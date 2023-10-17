---
tags:
  - number-theory
  - worked-example
order-tag: "0041"
date: 2023-09-19
---
#### Basic problems (brute force)
In basic [[congruence]] equations, we can brute force the solution.

>[!example]
>Solve $3x\equiv 2\;(\textnormal{mod }5)$.
>>Since the modulus $5$ is small, we can directly plug in all values of $x\;(\textnormal{mod }5)$, namely $0,1,2,3,4$.
>>- $3(0)\equiv 0\;(\textnormal{mod }5)$
>>- $3(1)\equiv 3\;(\textnormal{mod }5)$
>>- $3(2)\equiv 6\equiv 1\;(\textnormal{mod }5)$
>>- $3(3)\equiv 9\equiv 4\;(\textnormal{mod }5)$
>>- $3(4)\equiv 12\equiv 2\;(\textnormal{mod }5)$
>>
>>Thus the only solution is $x\equiv 4\;(\textnormal{mod }5)$.

>[!example]
>Solve $3x\equiv 2\;(\textnormal{mod }6)$
>>This equations has no solutions. We can check this by plugging in all values of $0\leq x\leq 5$.
>>Alternatively, note that since $3x$ is a multiple of $3$, it is either $0\;(\textnormal{mod }6)$ or $3\;(\textnormal{mod }6)$.

#### Using modular arithmetic
For larger moduli, it is not feasible to plug in all values of $0\leq x\leq n-1$. We can apply some [[modulus-operations|algebra]].

>[!example]
>Solve $12x\equiv 300\;(\textnormal{mod }592)$.
>>[[modulus-operations#Proposition (relatively prime modulus)|Since]] $gcd(3,592)=1$, we can divide by 3.
>>$4x\equiv 100\;(\textnormal{mod }592)$.
>>Now we can divide [[modulus-operations#Proposition (diving the modulus)|everything]] by 4.
>>$x\equiv 25\;(\textnormal{mod }148)$.
>>Thus $(\textnormal{mod }592)$, we have
>>$$x\equiv 25,173,321,469\;(\textnormal{mod }592)$$

>[!example]
>Solve $5x\equiv 6\;(\textnormal{mod }29)$.
>>$5x\equiv 6$
>>$\leftrightarrow30x\equiv 36\;(\textnormal{mod }29)$
>>$\leftrightarrow x\equiv 7\;(\textnormal{mod }29)$

>[!example]
>Solve $4x\equiv 301\;(\textnormal{mod }592)$
>>Note that if there is a solution, than $592|(4x-301)$.
>>But, $4x-301=2(2x-151)+1$ is odd.
>>Since $592$ is even, $592\nmid(4x-301)$.
>>Thus there is no solution.

#### Systems of congruences

>[!example]
>Solve $$
\begin{align*}
  x + 3y \equiv 5\;(\textnormal{mod }6) \\
  2x + 3y \equiv 1\;(\textnormal{mod }6)
\end{align*}$$
>> Adding gives
>> $$\begin{align*}
  3x \equiv 0\;(\textnormal{mod }6) \\
  2x + 3y \equiv 1\;(\textnormal{mod }6)
\end{align*}$$
>>This has 3 solutions: $x\equiv 0,2,4\;(\textnormal{mod }6)$
>>1. $x\equiv 0\;(\textnormal{mod }6)$:
>>   Plug into 1st congruence: $3y\equiv 1\;(\textnormal{mod }6)$.
>>   Again, this has no solutions.
>>2. $x\equiv 2\;(\textnormal{mod }6)$
>>   Plug into 1st congruence: $$
\begin{align*}
4+3y \equiv  1\;(\textnormal{mod }6) \\
3y \equiv -3\;(\textnormal{mod }6) \\
3y \equiv  3\;(\textnormal{mod }6)
\end{align*}$$
>   This has $3$ solutions: $y\equiv 1,3,5\;(\textnormal{mod }6)$.
>3. $x\equiv 4\;(\textnormal{mod }6)$:
>   Plug into 1st congruence: $$
\begin{align*}
12+3y \equiv  1\;(\textnormal{mod }6) \\
3y \equiv -1\;(\textnormal{mod }6) \\
3y \equiv  1\;(\textnormal{mod }6)
\end{align*}$$
>   Once again, this has no solutions.
>>
>>So there are three solutions $(\textnormal{mod }6)$:
>>$$x\equiv 2\;(\textnormal{mod }6)\textnormal{ and }y\equiv 1,3,5\;(\textnormal{mod }6)$$






