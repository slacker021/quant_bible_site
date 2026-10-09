---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-corollary-for-limit-inequalities/","dg-note-properties":{}}
---

Suppose $\lim_{n \to \infty} x_n = A$ and $\lim_{n \to \infty} y_n = B$.

---
# Corollaries 1 and 2
Assume that $x_n \ge y_n$ for all $n > N$, but contrary to the statement, $A < B$. By the theorem regarding strict inequalities involving limits, if $A < B$, there's an index $N^*$ such that $x_n < y_n$ for all $n > N^*$. Let $M = \max(N, N^*) + 1$. Because $M > N$, the initial premise dictates that $x_M \ge y_M$. Because $M > N^*$, the theorem of limit inequalities dictates that $x_M < y_M$. This yields the simultaneous truth of $x_M \ge y_M$ and $x_M < y_M$, an absolute contradiction. Thus, the assumption that $A < B$ must be false. It strictly follows that $A \ge B$. 

---
# Corollaries 3 and 4
Let $\{y_n\}$  be an ultimately constant sequence, where $y_n = b$ for all $n \in \mathbb{N}$. The limit of this sequence is definitively $B = b$. Substituting $\{y_n\}$ into the proven result of corollaries 1 and 2 directly yields that if $x_n \ge b$ for all $n > N$, then the limit $A$ must satisfy $A \ge b$. 
$$
\textbf{Q.E.D}
$$
