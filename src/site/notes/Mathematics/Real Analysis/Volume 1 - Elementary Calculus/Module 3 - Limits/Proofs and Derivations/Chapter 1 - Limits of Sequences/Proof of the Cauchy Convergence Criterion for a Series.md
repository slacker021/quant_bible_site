---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-cauchy-convergence-criterion-for-a-series/","dg-note-properties":{}}
---

# Theorem
By definition, the infinite series $\sum_{n=1}^\infty a_n$ converges if and only if its sequence of partial sums $\{s_n\}$, defined by $s_n := \sum_{k=1}^n a_k$, converges. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Criterion for Sequences\|Cauchy Criterion for Sequences]], $\{s_n\}$ converges if and only if $\{s_n\}$ is a Cauchy sequence: for every $\varepsilon > 0$, there exists an index $N_0 \in \mathbb{N}$ such that $|s_m - s_p| < \varepsilon$ for all $m, p > N_0$.

For any indices $m \ge n \ge 2$, the difference between the partial sums $s_m$ and $s_{n-1}$ expands as
$$
\begin{gather}
s_m - s_{n-1} = (a_1 + a_2 + \dots + a_m) - (a_1 + a_2 + \dots + a_{n-1}) = a_n + a_{n+1} + \dots + a_m \tag{1}
\end{gather}
$$
which is written compactly in summation notation as
$$
\begin{gather}
s_m - s_{n-1} = \sum_{k=n}^m a_k \tag{2}
\end{gather}
$$
- **Necessity:** Suppose $\sum_{n=1}^\infty a_n$ converges, so $\{s_n\}$ is a Cauchy sequence. Given $\varepsilon > 0$, let $N_0 \in \mathbb{N}$ be such that $|s_m - s_p| < \varepsilon$ for all $m, p > N_0$, and set $N := N_0 + 1 \in \mathbb{N}$. Then for any integers $m, n \in \mathbb{N}$ satisfying $m \ge n > N$, the index $p := n - 1$ satisfies $p > N - 1 = N_0$ and $m \ge n > N_0$. Applying step 2 yields
$$
\begin{gather}
\left| \sum_{k=n}^m a_k \right| = |s_m - s_{n-1}| < \varepsilon \quad \forall m \ge n > N \tag{3}
\end{gather}
$$
- **Sufficiency:** Conversely, suppose that for every $\varepsilon > 0$ there exists $N \in \mathbb{N}$ such that step 3 holds for all $m \ge n > N$. Let $m, p > N$ be arbitrary. If $m = p$, then $|s_m - s_p| = 0 < \varepsilon$. If $m \neq p$, assume without loss of generality that $m > p$, and set $n := p + 1$. Then $m \ge n = p + 1 > N + 1 > N$, so step 2 and step 3 guarantee that $|s_m - s_p| = \left|\sum_{k=n}^m a_k\right| < \varepsilon$. Thus, $\{s_n\}$ is a Cauchy sequence, and $\sum_{n=1}^\infty a_n$ converges.

---
# Corollary
Assume the series $\sum_{n=1}^\infty a_n$ converges, and let $\varepsilon > 0$ be arbitrary. By the Cauchy Convergence Criterion established in the Theorem above, there exists an index $N \in \mathbb{N}$ such that $\left| \sum_{k=n}^m a_k \right| < \varepsilon$ for all $m \ge n > N$. Specializing this inequality to the case $m = n$ collapses the sum to a single term:
$$
\begin{gather}
\left| \sum_{k=n}^n a_k \right| = |a_n - 0| = |a_n| < \varepsilon \quad \forall n > N \tag{4}
\end{gather}
$$
By the definition of the limit of a sequence, step 4 proves that $\lim_{n \to \infty} a_n = 0$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
