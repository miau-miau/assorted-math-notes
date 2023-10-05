---
tags:
  - logic
order-tag: "0002"
aliases:
  - contrapositive
date: 2023-08-22
---
#### NOT (negation)
The negation of $p$ is "it is not the case that $p$", written as $\neg p$.

>[!example]
>- "$\neg(n<10)$" is $n\geq 10$
>- "$\neg$(it is sunny)" is "it is not sunny"

The rules for negating logic statements can be proven with truth tables.


#### Negation of [[logic-statements#AND statement (conjunction)|conjunction]]

$$
\neg(p\land q)=\neg p\land\neg q
$$

>[!example]
>"$\neg$(x is even and y is even)" is "it is not the case that x is even and y is even", which means that at least one of them is not even. Rewording, we have "x is odd or y is odd".


#### Negation of [[logic-statements#OR statement (disjunction)|disjunction]]

$$
\neg(p\lor q)=\neg p \land \neg q
$$

>[!example]
>"$\neg$(he can swim or he can fly)" is "it is not the case that he can fly or he can swim". This can only be true if he can neither swim nor fly, which can be written as "he cannot fly and he cannot swim."


#### Negation of [[logic-statements#Implication (if ..., then ...)|implication]]

$$
\neg(p\to q)=p\land \neg q
$$

>[!example]
>"If it is sunny, then I am running". The only way for it to be false is that it is sunny *and* I am not running. So "$\neg$(if it sunny, then I am not running)" if "it is sunny and I am not running".


#### Contrapositive
The contrapositive of $p\to q$ if $\neg q\to\neg p$.

>[!example]
>The contrapositive of "if he lives in Boston, then he lives in the United States" is "I he doesn't live in the United States, he doesn't live in Boston".

##### Theorem
$p\to q$ and $\neg q\to\neg p$ are logically equivalent. 
That is $p\to q$ is true if and only if $\neg q\to\neg p$.
###### Proof
| $p$ | $q$ | $p\to q$ |
| --- | --- | -------- |
| T   | T   | T        |
| T   | F   | F        |
| F   | T   | T        |
| F   | F   | T        |

| $\neg p$ | $\neg q$ | $\neg q\to\neg p$ |
| -------- | -------- | ----------------- |
| F        | F        | T                 |
| F        | T        | F                 |
| T        | F        | T                 |
| T        | T        | T                  |

