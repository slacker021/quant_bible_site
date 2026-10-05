---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-the-countability-of-rational-numbers/","dg-note-properties":{}}
---

The set of rational numbers $\mathbb{Q}$ consists of all numbers that can be expressed as a fraction $p/q$, where $p$ is an integer ($p \in \mathbb{Z}$) and $q$ is a non-zero natural number ($q \in \mathbb{N}$).

Let $A_q$ be the set of all rational numbers with a fixed denominator $q$:
$$
\begin{gather} 
A_q = \{ \frac{p}{q} \ \Big| \  p \in \mathbb{Z} \} \tag{1} \end{gather}
$$
For any specific $q \in \mathbb{N}$, the mapping $f_q: \mathbb{Z} \to A_q$ defined by $f_q(p) = p/q$ is a distinct bijection between the integers and the set $A_q$. Since the set of integers $\mathbb{Z}$ is countable, each set $A_q$ must also be countable.

The entire set of rational numbers can then be expressed as the union of all such sets across all possible denominators $q \in \mathbb{N}$:
$$
\begin{gather} \mathbb{Q} = \bigcup_{q=1}^\infty A_q \tag{2} \end{gather}
$$
This formulation represents $\mathbb{Q}$ as the union of a countably infinite family of countable sets. By the previously established theorem regarding the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of Proposition 2 for Countable Sets\|union of countable sets]], the union of a countable collection of countable sets is strictly countable. Therefore, the set of all rational numbers $\mathbb{Q}$ is countable.
$$\textbf{Q.E.D}$$