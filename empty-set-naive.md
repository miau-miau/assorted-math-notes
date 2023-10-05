---
tags:
  - set-theory
order-tag: "0006"
date: 2023-08-29
---
An empty set is a set that contains no elements.
Dealing with the empty set can be confusing. While [[sets-naive#Proposition (empty set)|empty set is a subset of any set]], it is not an element of any set. Let's look at some examples.

- $\emptyset\neq \{ \emptyset \}$, since $\emptyset$ is a set with no elements, and $\{ \emptyset \}$ is a set with one element, $\emptyset$.
- $\emptyset\subseteq \{ \emptyset \}$, by previously mentioned proposition
- $\{ \emptyset \}\not\subset \{ \{ \emptyset \} \}$, since $\{ \emptyset \}$ has an element $\emptyset$, which is not an element of $\{ \{ \emptyset \} \}$.
- Let $A=\{ \emptyset,a,b \}$. Then $\emptyset\subset A,\{ \emptyset \}\subseteq A,\{ \emptyset \}\subseteq A$.
- $P(\emptyset)=\{ \emptyset \}$.