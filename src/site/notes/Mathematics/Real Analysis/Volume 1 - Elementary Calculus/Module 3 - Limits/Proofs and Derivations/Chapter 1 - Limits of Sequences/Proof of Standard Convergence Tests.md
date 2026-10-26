---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-standard-convergence-tests/","dg-note-properties":{}}
---

# Theorem
Let $\sum_{n=1}^\infty a_n$ be a series of real numbers, and define the non-negative extended real quantity $\alpha := \limsup_{n \to \infty} \sqrt[n]{|a_n|} \ge 0$.

### Convergence
Assume $\alpha < 1$. Because $\alpha \ge 0$, one may choose a real number $q$ satisfying $\alpha < q < 1$ (so that $0 < q < 1$). By the definition of the superior limit $\limsup_{n \to \infty} \sqrt[n]{|a_n|} = \alpha$, there exists a threshold index $N \in \mathbb{N}$ such that for all $n > N$:
$$
\begin{gather}
\sqrt[n]{|a_n|} < q \tag{1}
\end{gather}
$$
Raising both non-negative sides of step 1 to the $n$-th power yields
$$
\begin{gather}
|a_n| < q^n \quad \forall n > N \tag{2}
\end{gather}
$$
Because $0 < q < 1$, the geometric series $\sum_{n=1}^\infty q^n$ converges. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Standard Comparison Test\|Standard Comparison Test]], since the non-negative terms $|a_n|$ are bounded above by the terms of the convergent series $\sum_{n=1}^\infty q^n$ for all $n > N$, the series $\sum_{n=1}^\infty |a_n|$ converges. Thus, $\sum_{n=1}^\infty a_n$ converges absolutely.

### Divergence
Assume $\alpha > 1$. Because $\alpha = \limsup_{n \to \infty} \sqrt[n]{|a_n|} > 1$ is the largest partial limit of the sequence $\left\{\sqrt[n]{|a_n|}\right\}$, there exist infinitely many indices $n \in \mathbb{N}$ for which
$$
\begin{gather}
\sqrt[n]{|a_n|} > 1 \implies |a_n| > 1 \tag{3}
\end{gather}
$$
Consequently, the sequence of terms $\{a_n\}$ cannot converge to zero as $n \to \infty$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|Necessary Condition for Series Convergence]], the failure of $\{a_n\}$ to tend to zero guarantees that the series $\sum_{n=1}^\infty a_n$ diverges.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
