---
tags:
  - set-theory
order-tag: "0017"
date: 2023-08-31
---
We can encode [[binary-relation|relations]] in tables.

$A=\{ 1,2,3 \}$.
$A\times A=\{ (1,1),(1,2),(1,3),$
$\quad\quad\quad\quad\;\;(2,1),(2,2),(2,3)  \}$
$\quad\quad\quad\quad\;\;(3,1),(3,2),(3,3)  \}$

###### [[reflexive-relation|reflexive]] - filled diagonal
$R=\{ (1,1),(2,2),(3,3),(1,2) \}$

|     | 1   | 2   | 3   |
| --- | --- | --- | --- |
| 1   | *x*   | x   |     |
| 2   |     | *x*   |     |
| 3   |     |     | *x*    |

###### [[symmetric-relation|symmetric]] - symmetric about diagonal
$R=\{ (1,1),(1,2),(2,1) \}$

|     | 1   | 2   | 3   |
| --- | --- | --- | --- |
| 1   | x   | x   |     |
| 2   | x   |     |     |
| 3   |     |     |     |

###### [[antisymmetric-relation|antisymmetric]] - reflection over diagonal is blank
$R=\{ (1,1),(1,2),(1,3),(3,2) \}$


|     | 1   | 2   | 3   |
| --- | --- | --- | --- |
| 1   | x   | x   |  x  |
| 2   |     |     |     |
| 3   |     | x   |     |
