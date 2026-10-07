---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-proposition-2-for-countable-sets/","dg-note-properties":{}}
---

Let $\{A_i\}_{i \in \mathbb{N}}$ be a countably infinite family of sets, where each individual set $A_i$ is also countably infinite. The objective is to prove that the union $U = \bigcup_{i=1}^\infty A_i$ is a countable set.

Because each set $A_i$ is countable, its elements can be enumerated as a sequence. Let the elements of $A_i$ be denoted by $a_{i,j}$, where the first index $i$ represents the set to which the element belongs, and the second index $j$ represents the position of the element within that set. The elements of the union can therefore be arranged into an infinite two-dimensional grid:
$$
\begin{gather} A_1 = {a_{1,1}, a_{1,2}, a_{1,3}, a_{1,4}, \dots} \ A_2 = {a_{2,1}, a_{2,2}, a_{2,3}, a_{2,4}, \dots} \ A_3 = {a_{3,1}, a_{3,2}, a_{3,3}, a_{3,4}, \dots} \ \vdots \tag{1} \end{gather}
$$
To demonstrate that the union is countable, a systematic method must be formulated to enumerate every element in this grid sequentially without missing any, assigning each a unique natural number. This can be achieved using *Cantor's diagonal argument*.

The elements are traversed along the anti-diagonals of the grid. For any element $a_{i,j}$, the sum of its indices is $k = i + j$. The enumeration proceeds by tracking elements with a constant sum $k$, starting from $k=2$ and incrementing $k$ by 1 at each stage:
- $k=2$: $a_{1,1}$  
- $k=3$: $a_{2,1}, a_{1,2}$  
- $k=4$: $a_{3,1}, a_{2,2}, a_{1,3}$  
- $k=5$: $a_{4,1}, a_{3,2}, a_{2,3}, a_{1,4}$  

This generates a linear sequence:
$$\begin{gather} U = {a_{1,1}, a_{2,1}, a_{1,2}, a_{3,1}, a_{2,2}, a_{1,3}, a_{4,1}, \dots} \tag{2} \end{gather}
$$
Every element $a_{i,j}$ will eventually be reached when the diagonal sum $k$ reaches $i+j$. If the sets $A_i$ are not disjoint, some elements may appear multiple times in the grid. To maintain a strict bijection with $\mathbb{N}$, one simply omits any element that has already been added to the enumerated sequence.

Because every element of the union can be mapped to a unique natural number through this diagonal counting procedure, the union of a countable family of countable sets is itself a countable set.
$$\textbf{Q.E.D}$$