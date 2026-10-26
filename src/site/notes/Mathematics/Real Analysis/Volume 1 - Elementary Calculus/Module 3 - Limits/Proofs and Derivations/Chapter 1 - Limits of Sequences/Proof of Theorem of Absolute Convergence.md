---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-theorem-of-absolute-convergence/","dg-note-properties":{}}
---

Assume the series $\sum_{n=1}^{\infty} x_n$ is absolutely convergent. By definition of absolute convergence, the corresponding series of absolute values $\sum_{n=1}^{\infty} |x_n|$ converges to a finite real sum.

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|Cauchy Convergence Criterion for a Series]], a series $\sum_{n=1}^{\infty} a_n$ converges if and only if for every $\varepsilon > 0$, there exists an index $N \in \mathbb{N}$ such that for all $m \ge n > N$, the finite block sum satisfies
$$
\begin{gather}
\left| \sum_{k=n}^{m} a_k \right| < \varepsilon \tag{1}
\end{gather}
$$
Let $\varepsilon > 0$ be arbitrary. Because the series $\sum_{n=1}^{\infty} |x_n|$ converges, applying the Cauchy Convergence Criterion from step 1 to $\sum_{n=1}^{\infty} |x_n|$ guarantees the existence of an index $N \in \mathbb{N}$ such that for all $m \ge n > N$:
$$
\begin{gather}
\sum_{k=n}^{m} |x_k| = \left| \sum_{k=n}^{m} |x_k| \right| < \varepsilon \tag{2}
\end{gather}
$$
Now consider the original series $\sum_{n=1}^{\infty} x_n$. For any indices $m \ge n > N$, applying the generalized [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] to the finite sum $\sum_{k=n}^m x_k$ yields
$$
\begin{gather}
\left| \sum_{k=n}^{m} x_k \right| \le \sum_{k=n}^{m} |x_k| \tag{3}
\end{gather}
$$
Combining step 2 and step 3 by transitivity shows that for all $m \ge n > N$:
$$
\begin{gather}
\left| \sum_{k=n}^{m} x_k \right| \le \sum_{k=n}^{m} |x_k| < \varepsilon \tag{4}
\end{gather}
$$
Because step 4 holds for every $\varepsilon > 0$, the series $\sum_{n=1}^{\infty} x_n$ satisfies the Cauchy Convergence Criterion for a Series and is therefore convergent.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
