---
tags:
  - number-theory
  - "#application"
order-tag: "0045"
date: 2023-09-21
---
#### ISBN
Most published books have a unique ISBN, which has 10 digits, $a_{1},\dots,a_{10}$ where $0\leq a_{1},\dots,a_{9}\leq 10,\;0\leq a_{10}\leq 10$, and
$$
a_{1}+2a_{2}+3a_{3}+\dots+9a_{9}+10a_{10}\equiv 0\;(\textnormal{mod }11).
$$
First 9 digits identify the book, while $a_{10}$ is a "check digit", where [[congruence]] helps to make sure the ISBN was inputted correctly.

#### Universal Product Codes (and bar codes)
There are (often) $12$ digits below a bar code. As with the ISBN, the $12^{\textnormal{th}}$ digit is a check digit determined by:
$$3(\textnormal{sum of digits in odd positions})+(\textnormal{sum of digits in even positions})\equiv 0\;(\textnormal{mod }10)$$
![[upc-code.png]]
>[!example]
>In the UPC above, $(3+0+0+9+4+2)+3(0+6+0+0+2+1+5)$
>$=18+3(14)=60\equiv 0\;(\textnormal{mod }10)$ ✅

