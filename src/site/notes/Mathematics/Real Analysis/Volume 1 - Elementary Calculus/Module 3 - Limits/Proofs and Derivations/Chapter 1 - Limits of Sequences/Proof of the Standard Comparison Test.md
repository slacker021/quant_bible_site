---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-standard-comparison-test/","dg-note-properties":{}}
---

# Theorem 1
Let $S_n = \sum_{k=1}^n a_k$ and $T_n = \sum_{k=1}^n b_k$ be the sequences of partial sums. Because $a_n \ge 0$ and $b_n \ge 0$ for all $n$, both $\{S_n\}$ and $\{T_n\}$ are strictly nondecreasing sequences. Assume the dominant series $\sum_{n=1}^\infty b_n$ converges. By the convergence criterion for non-negative series, its sequence of partial sums $\{T_n\}$ is bounded above by some real number $M$.

Without loss of generality, it is assumed that the inequality $a_n \le b_n$ holds for all $n \in \mathbb{N}$. (If it only holds after an index $N$, a finite constant offset can be added to the bound without affecting asymptotic convergence). Because $a_k \le b_k$ for every term, the partial sums maintain the inequality 
$$S_n = \sum_{k=1}^n a_k \le \sum_{k=1}^n b_k = T_n \tag{1}$$
Because $T_n \le M$ for all $n$, transitivity dictates that $S_n \le M$ for all $n$. The sequence $\{S_n\}$ is nondecreasing and definitively bounded above. Therefore, by the Weierstrass Theorem on Monotonic Sequences, $\{S_n\}$ must converge. Consequently, $\sum_{n=1}^\infty a_n$ converges. 

---
# Theorem 2
This is an immediate consequence of the contrapositive of what was just proven. Assume the lesser series $\sum_{n=1}^\infty a_n$ diverges. Because its terms are non-negative, the only possible manner of divergence for $\{S_n\}$ is unbounded growth toward positive infinity. Given that $S_n \le T_n$, if $S_n \to \infty$, the bounding constraint mechanically forces $T_n$ to also trend to infinity. Therefore, $\{T_n\}$ diverges, proving that the dominant series $\sum_{n=1}^\infty b_n$ diverges. 
$$
\textbf{Q.E.D}
$$
