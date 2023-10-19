---
tags:
  - algorithms
  - number-theory
  - application
  - "#cryptography"
order-tag: "0046"
date: 2023-09-21
aliases:
  - rsa
---
#### [[algorithms-introduction|Algorithm]]
You have set up a website through which anyone can send you a private message. You choose large prime numbers $p$ and $q$ and a number $e$ [[greatest-common-divisor#^3ec34f|relatively prime]] to $p-1$ and $q-1$.
Set $n=pq$ and publish $e,n$ (*public key*).
##### Encryption
How does someone send you a message?
1. Convert the characters in message to numbers (e.g. A, B, ..., Z $\to 01,02,\dots,26$) to get a number $M$.
2. Compute the encrypted message $E=M^e\;(\textnormal{mod }n)$. Send $E$.
##### Decryption
How do you recover $M$?
1. Find integers $a,x,b,y$ such that $1=ae+x(p-1)$ and $1=be+y(q-1)$.
2. [[solving-congruence-equations|Solve]] the system
$$
\begin{align}
x\equiv E^a\;(\textnormal{mod }p) \\
x\equiv E^b\;(\textnormal{mod }q)
\end{align}
$$
Then $M$ is $x\;(\textnormal{mod }n)$.

#### Explanation
to be continued