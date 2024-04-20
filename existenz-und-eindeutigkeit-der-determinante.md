---
layout: page
title: 'Existenz und Eindeutigkeit der Determinante'
---
## Existenzbeweis Determinante
Um zu beweisen, dass die Determinante einer oberen Dreiecksmatrix das Produkt der Diagonalelemente ist, betrachten wir eine beliebige obere Dreiecksmatrix A$$ A $$A der Größe $$ n \times n $$:

<p>$$ 
A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
0 & a_{22} & a_{23} & \cdots & a_{2n} \\
0 & 0 & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \cdots & a_{nn} \\
\end{pmatrix} 
$$</p>

Wir können die Determinante dieser Matrix $$ \text{det}(A) $$ durch Entwicklung nach der ersten Zeile berechnen:

<p>$$ 
\text{det}(A) = a_{11} \cdot \text{det}(A_{11}) + a_{12} \cdot \text{det}(A_{12}) + \cdots + a_{1n} \cdot \text{det}(A_{1n})
$$</p> 

Wobei $$ A_{ij} $$ die Matrix ist, die aus $$ A $$ entsteht, wenn man die $$i$$-te Zeile und die $$j$$-te Spalte entfernt. Da alle Elemente unterhalb der Diagonale null sind, sind alle $$ A_{ij} $$ ebenfalls obere Dreiecksmatrizen. Wenn $$ i \neq j $$, dann hat $$ A_{ij} $$ mindestens eine Nullzeile und somit ist $$ \text{det}(A_{ij}) = 0 $$. 

Wenn $$ i = j $$, dann besteht $$ A_{ii} $$ aus einem Element (dem Diagonalelement) und ist daher eine 1x1-Matrix, deren Determinante einfach das Diagonalelement selbst ist. Also gilt $$ \text{det}(A_{ii}) = a_{ii} $$.

Daraus folgt:

<p>$$
\text{det}(A) = a_{11} \cdot \text{det}(A_{11}) + a_{22} \cdot \text{det}(A_{22}) + \cdots + a_{nn} \cdot \text{det}(A_{nn}) 
$$</p>
Da alle $$ \text{det}(A_{ij}) $$ für $$ i \neq j $$ null sind, bleibt nur der Ausdruck $$ a_{11} \cdot \text{det}(A_{11}) + a_{22} \cdot \text{det}(A_{22}) + \cdots + a_{nn} \cdot \text{det}(A_{nn}) $$ übrig, und das ist einfach das Produkt der Diagonalelemente der Matrix $$ A $$. Daher ist die Determinante einer oberen Dreiecksmatrix gleich dem Produkt ihrer Diagonalelemente.

