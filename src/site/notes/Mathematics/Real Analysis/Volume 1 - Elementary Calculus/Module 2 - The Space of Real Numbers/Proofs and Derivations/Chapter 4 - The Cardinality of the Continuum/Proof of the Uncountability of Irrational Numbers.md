---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-the-uncountability-of-irrational-numbers/","dg-note-properties":{}}
---

Let $\mathbb{R}$ represent the set of all real numbers, and let $\mathbb{Q}$ represent the set of all rational numbers. The set of irrational numbers is defined as the set difference $\mathbb{R} \setminus \mathbb{Q}$.

By definition, the entire real number line can be partitioned into the union of rational numbers and irrational numbers:
$$
\begin{gather} \mathbb{R} = \mathbb{Q} \cup (\mathbb{R} \setminus \mathbb{Q}) \tag{1} \end{gather}
$$
Assume, for the sake of contradiction, that the set of irrational numbers $\mathbb{R} \setminus \mathbb{Q}$ is countable.

It has been rigorously established in prior theorems that the set of rational numbers $\mathbb{Q}$ is a countable set. Furthermore, operating under the established algebraic properties of cardinality, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of Proposition 2 for Countable Sets\|union of a finite or countable family of countable sets is itself a countable set]].

Under the assumption that $\mathbb{R} \setminus \mathbb{Q}$ is countable, the equation of step 1 represents the union of two countable sets. This logical sequence forces the conclusion that the universal set of real numbers $\mathbb{R}$ is countable.

However, Cantor's Diagonalization proof has decisively proven that the set of real numbers $\mathbb{R}$ is uncountable. This creates an irreconcilable contradiction:
$$
\begin{gather} \text{If } (\mathbb{R} \setminus \mathbb{Q}) \text{ is countable} \implies \mathbb{R} \text{ is countable (Contradiction)} \tag{2} \end{gather}
$$
To preserve the uncountability of $\mathbb{R}$, the assumption must be false. The set of irrational numbers cannot be countable. Because the uncountable "bulk" of $\mathbb{R}$ is not composed of the countable set $\mathbb{Q}$, it must be contained entirely within the irrational partition. Therefore, the set of irrational numbers has the cardinality of the continuum and is uncountable.
$$\textbf{Q.E.D}$$