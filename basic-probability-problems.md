---
tags:
  - probability
order-tag: "0070"
date: 2023-10-24
---
>[!example]
>Suppose a die is rolled twice. What is the [[probability-introduction|probability]] that the sum of the numbers that appear is $6$?
>Let $T=\{ 1,2,3,4,5,6 \}$
>Then $S=T\times T$ and $A=\{ (1,5),(2,4),(3,3),(4,2),(5,1) \}$
>Thus $\textnormal{P}(A)=\frac{|\,A\,|}{|\,S\,|}=\frac{5}{36}$.

>[!example]
>A group of five animals is chosen from four dogs and six cats.
>$S=\{ \textnormal{ all possible groups } \}$
>$|\,S\,|=\binom{10}{5}=252$ (see [[combinations]]).
>
>a) What is the probability that four cats are chosen?
>$A=\{ \textnormal{ groups with four cats } \}$
>$|\,A\,|=\binom{6}{4}\binom{4}{1}=60$
>$\textnormal{P}(A)=\frac{60}{252}=\frac{5}{21}$
>b) What is the probability that at least four cats are chosen?
>$A=\{ \textnormal{ groups with at least four cats } \}=\{ \textnormal{ groups with four cats } \}\cup \{ \textnormal{ groups with five cats } \}$
>$|\,A\,|=\binom{6}{4}\binom{4}{1}+\binom{6}{5}\binom{4}{0}=66$.
>So $\textnormal{P}(A)=\frac{66}{252}=\frac{11}{42}$.

>[!example]
>Two couples, the Johnsons and the Millers are arranged randomly.
>$S=\{ \textnormal{ all possible arrangements } \}$
>$|\,S\,|=4!=24$ (see [[permutations]]).
>
>a) Find the probability that the Johnsons are next to each other.
>$A=\{ \textnormal{ arrangements in which, Johnsons are next to each other } \}$
>$|\,A\,|=(2!)(2!)3=12$ (2-permutation for Johnsons, 2-permutation for Millers, and three ways Millers can "surround" Johnsons)
>So $\textnormal{P}(A)=\frac{12}{24}=\frac{1}{2}$
>b) Find the probability that at least one couple is together.
>$A=\{ \textnormal{ at least one couple is together} \}$
>$A^{\mathbf{c}}=\{ \textnormal{ neither couple is together } \}$
>$|\,A^{\mathbf{c}}\,|=(2!)(2!)2=8$
>$|\,A\,|=|\,S\,|-|\,A^{\mathbf{c}}\,|=24-8=16$ (see [[basic-counting#Basics|basics of counting]])
>Thus $\textnormal{P}(A)=\frac{16}{24}=\frac{2}{3}$


 
