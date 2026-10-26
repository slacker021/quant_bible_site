---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-pigeonhole-principle/","dg-note-properties":{}}
---

Let $n \in \mathbb{N}$ be a natural number, and suppose that $m \ge n + 1$ objects are distributed into $n$ boxes. For each box $i \in \{1, 2, \dots, n\}$, let $k_i \in \mathbb{N} \cup \{0\}$ denote the number of objects placed in the $i$-th box. Because every object is placed into one of the $n$ boxes, the total number of objects is the sum of the box occupancies:
$$
\begin{gather}
\sum_{i=1}^n k_i = m \ge n + 1 \tag{1}
\end{gather}
$$
Assume, for the sake of contradiction, that the conclusion of the theorem is false, meaning that no box contains two or more objects. Then every box contains at most one object:
$$
\begin{gather}
k_i \le 1 \quad \forall i \in \{1, 2, \dots, n\} \tag{2}
\end{gather}
$$
Summing the inequalities in step 2 across all $n$ boxes via the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Order with Addition and Multiplication\|order compatibility axioms]] yields an upper bound on the total number of objects $m$:
$$
\begin{gather}
m = \sum_{i=1}^n k_i \le \sum_{i=1}^n 1 = \underbrace{1 + 1 + \dots + 1}_{n \text{ terms}} = n \tag{3}
\end{gather}
$$
Combining step 1 and step 3 requires $n + 1 \le m \le n$, which implies $n + 1 \le n \iff 1 \le 0$, a contradiction. Therefore, the assumption that every box contains at most one object is false, and at least one box must contain at least two objects.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
