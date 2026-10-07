---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-the-uncountability-of-the-real-numbers/","dg-note-properties":{}}
---

Assume, for the sake of contradiction, that the set of real numbers $\mathbb{R}$ is countable. If $\mathbb{R}$ is countable, then any subset of $\mathbb{R}$, including the open interval $(0, 1)$, must also be at most countable.

If $(0,1)$ is countable, there exists a bijection with the natural numbers, allowing every real number in this interval to be listed in a sequential enumeration: $x_1, x_2, x_3, \dots, x_n, \dots$. Every real number in this interval can be represented by an infinite decimal expansion. The enumerated list can be written as a grid of digits:
$$
\begin{gather} x_1 = 0.d_{11} d_{12} d_{13} d_{14} \dots \ x_2 = 0.d_{21} d_{22} d_{23} d_{24} \dots \ x_3 = 0.d_{31} d_{32} d_{33} d_{34} \dots \ \vdots \tag{1} \end{gather}
$$
Here, $d_{ij} \in \{0, 1, \dots, 9\}$ represents the $j$-th decimal digit of the $i$-th number in the sequence. To avoid ambiguity caused by dual representations (e.g., $0.4999\dots = 0.5000\dots$), one specifies that representations ending in an infinite sequence of nines are prohibited. 

A new real number $y \in (0,1)$ is now constructed digit by digit: 
$$
\begin{gather} y = 0.y_1 y_2 y_3 y_4 \dots \tag{2}  \\
\end{gather}
$$
The value of the $n$-th digit of $y$, denoted as $y_n$, is determined exclusively by examining the $n$-th digit of the $n$-th number in the list ($d_{nn}$) on the main diagonal of the grid. The construction rule is defined as follows:
$$
\begin{gather} y_n = \begin{cases} 1 & \text{if } d_{nn} \neq 1 \ 2 & \text{if } d_{nn} = 1 \end{cases} \tag{3} \end{gather}
$$
By this definition, $y_n \in \{1, 2\}$, ensuring that $y$ is a valid real number strictly between 0 and 1, and averting the dual representation issue.

By hypothesis, the list contains _every_ real number in $(0,1)$. Therefore, $y$ must appear somewhere in the sequence, meaning there exists some integer $k \in \mathbb{N}$ such that $y = x_k$.

If $y = x_k$, then the $k$-th decimal digit of $y$ must perfectly match the $k$-th decimal digit of $x_k$, requiring $y_k = d_{kk}$. However, the construction rule in Step 3 explicitly defined $y_k$ such that it inherently differs from $d_{kk}$. This yields the contradiction:
$$
\begin{gather} y_k \neq d_{kk} \implies y \neq x_k \quad \forall k \in \mathbb{N} \tag{4} \end{gather}
$$
The number $y$ cannot exist in the presumed complete enumeration. Thus, the assumption that the interval $(0,1)$ can be listed sequentially is false. Consequently, the set of real numbers $\mathbb{R}$ cannot be placed in a one-to-one correspondence with the natural numbers and is therefore uncountable.
$$\textbf{Q.E.D}$$