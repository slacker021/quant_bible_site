---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-theorem-of-absolute-convergence/","dg-note-properties":{}}
---

Let $\sum_{n=1}^\infty a_n$ be an infinite series of real numbers that is absolutely convergent, meaning that the series of absolute values $\sum_{n=1}^\infty |a_n|$ converges to a finite real sum.

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|Cauchy Convergence Criterion for a Series]], the series of absolute values $\sum_{n=1}^\infty |a_n|$ converges if and only if for every $\varepsilon > 0$, there exists an index $N \in \mathbb{N}$ such that for all integers $m \ge n > N$:
$$
\begin{gather}
\sum_{k=n}^m |a_k| = \left| \sum_{k=n}^m |a_k| \right| < \varepsilon \tag{1}
\end{gather}
$$
Now consider the original series $\sum_{n=1}^\infty a_n$. For any integers $m \ge n > N$, applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] to the tail sum yields:
$$
\begin{gather}
\left| \sum_{k=n}^m a_k \right| \le \sum_{k=n}^m |a_k| \tag{2}
\end{gather}
$$
Combining step 1 and step 2 demonstrates that for all $m \ge n > N$:
$$
\begin{gather}
\left| \sum_{k=n}^m a_k \right| < \varepsilon \tag{3}
\end{gather}
$$
Step 3 establishes that the original series $\sum_{n=1}^\infty a_n$ satisfies the Cauchy Convergence Criterion. Therefore, the series $\sum_{n=1}^\infty a_n$ converges.
$$
\begin{gather}
\textbf{Q.E.D.}
\end{gather}
$$
