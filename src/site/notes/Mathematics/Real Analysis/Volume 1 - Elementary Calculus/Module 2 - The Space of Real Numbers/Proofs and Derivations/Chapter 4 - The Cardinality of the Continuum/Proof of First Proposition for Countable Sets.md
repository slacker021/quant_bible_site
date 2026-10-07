---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-first-proposition-for-countable-sets/","dg-note-properties":{}}
---

Let $X$ be a countable set and let $A$ be a subset of $X$ ($A \subset X$). If $A$ is an empty set, it is finite and therefore at most countable. Assume $A$ is non-empty.

Since $X$ is countably infinite, there exists a bijective mapping $f: \mathbb{N} \to X$. This allows the elements of $X$ to be enumerated as a sequence $x_1, x_2, \dots, x_n, \dots$, where $x_n = f(n)$.

Because $A \subset X$, every element of $A$ appears in this sequence. An indexing function can be constructed to extract only the elements that belong to $A$. Let $n_1$ be the smallest natural number such that $x_{n_1} \in A$. Proceeding recursively, let $n_k$ be the smallest natural number greater than $n_{k-1}$ such that $x_{n_k} \in A$:
$$
\begin{gather} n_k = \min { n \in \mathbb{N} \mid n > n_{k-1} \text{ and } x_n \in A } \tag{1} \end{gather}
$$
This process creates a strictly increasing sequence of indices $n_1 < n_2 < \dots < n_k < \dots$. A new mapping $g$ is defined such that $g(k) = x_{n_k}$.

There are two potential outcomes for this selection process:
1. **The process terminates:** If there is no natural number $n > n_k$ such that $x_n \in A$, the subset $A$ contains exactly $k$ elements. In this case, $A$ is finite.
2. **The process does not terminate:** If the process continues indefinitely, the mapping $g: \mathbb{N} \to A$ is constructed for all $k \in \mathbb{N}$. Because the indices $n_k$ are strictly increasing, each element mapped by $g$ is distinct, ensuring injectivity. Because every element of $A$ must appear somewhere in the original sequence of $X$, every element of $A$ is eventually selected, ensuring surjectivity. Thus, $g$ is a bijection, making $A$ countably infinite.

In either case, the subset $A$ is either finite or countably infinite, satisfying the definition of being at most countable.
$$\textbf{Q.E.D}$$