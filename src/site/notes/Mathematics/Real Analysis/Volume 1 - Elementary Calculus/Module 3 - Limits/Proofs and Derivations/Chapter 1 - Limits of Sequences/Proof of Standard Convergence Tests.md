---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-standard-convergence-tests/","dg-note-properties":{}}
---

# Theorem 

### Convergence
Assume $\alpha < 1$. Choose a real number $q$ such that $\alpha < q < 1$. By the definition of the superior limit, there exists an index $N \in \mathbb{N}$ such that for all $n > N$:  
$$\sqrt[n]{\vert a_n \vert} \le q \tag{1}$$
Raising both sides to the $n$-th power yields
$$\vert a_n \vert \le q^n \quad \text{for all } n > N \tag{2}$$
The series $\sum q^n$ is a fundamental geometric series. Because $0 < q < 1$, the geometric series $\sum q^n$ strictly converges. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Standard Comparison Test\|comparison theorem]], since the absolute terms $\vert a_n \vert$ are bounded above by the terms of a convergent geometric series, the series $\sum \vert a_n \vert$ converges. Thus, $\sum a_n$ converges absolutely.

### Divergence
Assume $\alpha > 1$. By the definition of the superior limit, there are infinitely many indices $n$ for which $\sqrt[n]{\vert a_n \vert} \ge 1$. Raising this to the $n$-th power reveals that $\vert a_n \vert \ge 1$ for infinitely many terms. Consequently, the sequence of terms $a_n$ cannot possibly tend to zero ($\lim_{n \to \infty} a_n \neq 0$). By the necessary condition for series convergence, the failure of the terms to diminish to zero guarantees that the series $\sum a_n$ diverges. 
$$
\textbf{Q.E.D}
$$
