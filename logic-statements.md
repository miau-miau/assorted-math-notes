---
tags:
  - logic
order-tag: "0001"
aliases:
  - statements
  - logic
  - truth tables
date: 2023-08-22
---
#### AND statement (conjunction)
The statement "$p$ and $q$" ($p\land q$) is true if and only if both statements are true.

>[!example]
>"$2+2=4 \textnormal{ and }17 \textnormal{ is prime}$" is *True*
>"$2+2=4\textnormal{ and }18 \textnormal{ is prime}$" is *False*
##### Truth Table
| $p$ | $q$ | $p\land q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | F          |


#### OR statement (disjunction)
The statement "$p$ or $q$" ($p\lor q$) is true if at least one of the statements is true.

>[!example]
>"$2+2=4\textnormal{ and }18 \textnormal{ is prime}$" is *True*
>"$2+2=5\textnormal{ and }18 \textnormal{ is prime}$" is *False*

##### Truth Table
| p   | q   | $p\lor q$ |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | T         |
| F   | T   | T         |
| F   | F   | F         |


#### Implication (if ..., then ...)
The statement "$p \textnormal{ implies } q$" ($p\to q$) is false only when $p$ is true and $q$ is false.

>[!example]-
>"If it is sunny tomorrow, then I will run"
>
| Sunny | Run | Sunny$\to$ run | Explanation                                          |
| ----- | --- | -------------- | ---------------------------------------------------- |
| T     | T   | T              | It is sunny and I *am* running, so I told the truth  |
| T     | F   | F              | It is sunny but I am *not* running, so I lied        |
| F     | T   | T              | It is not sunny, so the statement is not applicable. | 
| F     | F   | T              | Same as above |
>

##### Truth Table
| p   | q   | $p\to q$ |
| --- | --- | -------- |
| T   | T   | T        |
| T   | F   | F        |
| F   | T   | T        |
| F   | F   | T        |

##### Notes on language
"$\textnormal{If }p, \textnormal{ then } q$" can also be written as "$p\textnormal{ implies }q$". 
$p$ is a **hypothesis** and $q$ is a **conclusion**.

>[!note]
>In many problems, $p$ can be called a **sufficient condition**, meaning that if you want $q$ to be true, it is sufficient to show that $p$ is true, while $q$ can be called a **necessary** condition, meaning that if $q$ is false, then $p$ cannot be true either.
#### The converse of implication
The converse of $p\to q$ is $q\to p$.

>[!example]
>The converse of "if it is sunny tomorrow, then I will run" is "if I run tomorrow, then it is sunny"

##### Truth Table
| p   | q   | $p\to q$ | $q\to p$ |
| --- | --- | -------- | -------- |
| T   | T   | T        | T        |
| T   | F   | F        | T        |
| F   | T   | T        | F        |
| F   | F   | T        | T         |


#### Double Implication (if and only if)
Double implication ($p\leftrightarrow q$) is true if $p$ and $q$ have the same truth value, and false otherwise.

>[!example]
>"$2 \textnormal{ is even }\leftrightarrow 4 \textnormal{ is even}$" is *True*
>"He lives in the United States $\leftrightarrow$ He lives in New York" is *False*, since $\to$ is true, but $\leftarrow$ is false. 

>[!note]
>$(p\to q)\land(q\to p)$ is the same as $p\leftrightarrow q$, which can be seen in the truth table below. This fact will be useful in [[proofs]], i.e. to prove a double implication true, you may prove implication and its converse true.

##### Truth Table
| $p$ | $q$ | $p\to q$ | $q\to p$ | $p\leftrightarrow q$ |
| --- | --- | -------- | -------- | -------------------- |
| T   | T   | T        | T        | T                    |
| T   | F   | F        | T        | F                    |
| F   | T   | T        | F        | F                    |
| F   | F   | T        | T        | T                     |

#### Some definitions

>[!definition]
>A statement that is always true is called a **tautology**.
>>[!example]
>>- $p\lor\neg p$ is a tautology.

>[!definition]
>A statement that is always false is called a **contradiction**.
>>[!example]
>>$p\land\neg p$ is a contradiction.

| $p$ | $\neg p$ | $p\lor\neg q$ | $p\land\neg q$ |
| --- | -------- | ------------- | -------------- |
| T   | F        | T             | F              |
| F   | T        | T             | F               |


