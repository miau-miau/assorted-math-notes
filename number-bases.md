---
tags:
  - number-theory
order-tag: "0030"
date: 2023-09-12
---
Representing natural number in bases is an application of the [[division-algorithm]].

>[!example]-
>Natural numbers are typically presented in *base 10*:
>$$2023=2*1000+0*100+2*10+3*1$$
>$$2023=2*10^3+0*10^2+2*10^1+3*10^0$$
>We can write 2023 in any base. *Base 2*:
>$$2023=1*2^10+1*2^9+1*2^8+1*2^7+1*2^6+1*2^5+0*2^4+0*2^{3}+1*2^{2}+1*2^0=(11111100111)_{2}$$
>The division algorithm provides the digits
>$$2023=2*1000+2*10+3=202*10+3$$
>$$202=20*10+2$$
>$$20=2*10+0$$
>$$2=0*10+2$$
These remainders are the digits of $2023$.
#### General case

>[!definition]
>In general, for a fixed integer $b>1$, the **base b representation** of a natural number $N$ is the expression $(a_{n-1}a_{n-2}\dots a_{1}a_{0})_{b}$, where $0\leq a_{i}<b$ and $N=a_{n-1}b^{n-1}+\dots+a_{1}b^1+a_{0}b^0$.
>Moreover, the numbers $a_{0},\dots,a_{n-1}$ are the **remainders** when $N$ and then successive quotients are divided by $b$.
>>[!note]
>>Some common bases are $2$ (binary), $8$ (octal), $16$ (hexadecimal).

>[!example]
>Find the hexadecimal representation of $2023$. This requires repeated use of the [[division-algorithm]].
>$$2023=126*16+7$$
>$$126=7*16+14$$
>$$7=0*16+7$$
>The hexadecimal digits are $0,1,\dots,A,B,C,D,E,F$, so $2023=(7E7)_{16}$.
