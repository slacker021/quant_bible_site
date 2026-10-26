---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-proposition-2-for-countable-sets/","dg-note-properties":{}}
---

Consider first a countably infinite family of nonempty sets $\{A_i\}_{i \in \mathbb{N}}$, where each set $A_i$ is at most countable. Because each $A_i$ is nonempty and either finite or countably infinite, its elements can be indexed as an infinite sequence $a_{i,1}, a_{i,2}, a_{i,3}, \dots$ (if a particular set $A_i$ is finite with $m_i$ elements, one simply repeats the final element by setting $a_{i,j} := a_{i,m_i}$ for all $j > m_i$). The elements of the union $U := \bigcup_{i=1}^\infty A_i$ can then be arranged into an infinite two-dimensional array in which the row index $i \in \mathbb{N}$ identifies the set $A_i$ and the column index $j \in \mathbb{N}$ identifies the position within that sequence:
$$
\begin{gather}
A_1 : \quad a_{1,1}, \quad a_{1,2}, \quad a_{1,3}, \quad a_{1,4}, \quad \dots \\[2mm]
A_2 : \quad a_{2,1}, \quad a_{2,2}, \quad a_{2,3}, \quad a_{2,4}, \quad \dots \\[2mm]
A_3 : \quad a_{3,1}, \quad a_{3,2}, \quad a_{3,3}, \quad a_{3,4}, \quad \dots \\[2mm]
\vdots \tag{1}
\end{gather}
$$
To enumerate all entries of the array in step 1 sequentially, one applies *Cantor's zig-zag (or pairing) enumeration*, traversing the grid along its finite anti-diagonals. For each entry $a_{i,j}$, the sum of its indices is a natural number $k := i + j \ge 2$. For any fixed sum $k \in \{2, 3, 4, \dots\}$, there are exactly $k - 1$ ordered pairs $(i, j) \in \mathbb{N} \times \mathbb{N}$ satisfying $i + j = k$, which can be listed in order of decreasing row index $i = k - 1, k - 2, \dots, 1$:
- $k = 2$: $a_{1,1}$
- $k = 3$: $a_{2,1}, \ a_{1,2}$
- $k = 4$: $a_{3,1}, \ a_{2,2}, \ a_{1,3}$
- $k = 5$: $a_{4,1}, \ a_{3,2}, \ a_{2,3}, \ a_{1,4}$

Concatenating these finite anti-diagonals for $k = 2, 3, 4, \dots$ produces a single linear sequence $y_1, y_2, y_3, \dots$ containing every element of the array:
$$
\begin{gather}
(y_n)_{n \in \mathbb{N}} = \left(a_{1,1}, \ a_{2,1}, \ a_{1,2}, \ a_{3,1}, \ a_{2,2}, \ a_{1,3}, \ a_{4,1}, \ \dots\right) \tag{2}
\end{gather}
$$
Explicitly, because the anti-diagonals prior to $k = i + j$ contain $1 + 2 + \dots + (i + j - 2) = \frac{(i + j - 2)(i + j - 1)}{2}$ entries, each pair $(i, j) \in \mathbb{N} \times \mathbb{N}$ appears at the unique position $n = \pi(i, j) := \frac{(i + j - 2)(i + j - 1)}{2} + j \in \mathbb{N}$. Thus, the mapping $\phi: \mathbb{N} \to U$ defined by $\phi(n) := y_n$ is surjective onto $U$.

Because the sets $A_i$ need not be mutually disjoint (and finite sets $A_i$ have repeated tail entries), an element of $U$ may appear multiple times in the sequence of step 2. To eliminate duplicates rigorously, associate to each element $u \in U$ the minimal index at which $u$ first appears in the sequence $(y_n)_{n \in \mathbb{N}}$:
$$
\begin{gather}
\iota(u) := \min \{ n \in \mathbb{N} \mid \phi(n) = u \} \tag{3}
\end{gather}
$$
which is well-defined by the surjectivity of $\phi$ and the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Well-Ordering Principle]]. If $\iota(u_1) = \iota(u_2) = n$, then $u_1 = \phi(n) = u_2$, so $\iota: U \to \mathbb{N}$ is an injective mapping that places $U$ in bijective correspondence with the subset $S := \iota(U) \subset \mathbb{N}$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of First Proposition for Countable Sets\|First Proposition for Countable Sets]], $S \subset \mathbb{N}$ is at most countable, and therefore $U$ is at most countable (if some $A_i = \emptyset$, omitting the empty sets from the union leaves $U$ unchanged, or yields $U = \emptyset$ if all $A_i$ are empty).

Finally, if the family is finite, say $\{A_1, A_2, \dots, A_m\}$, setting $A_i := A_m$ for all $i > m$ reduces the finite union $\bigcup_{i=1}^m A_i = \bigcup_{i=1}^\infty A_i$ immediately to the countable family case above. Moreover, if at least one set $A_{i_0}$ in the family is countably infinite, then $A_{i_0} \subset U$ implies that $U$ cannot be finite; since $U$ is at most countable and infinite, $U$ is a countable set.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
