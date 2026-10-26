---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-standard-comparison-test/","dg-note-properties":{}}
---

Let $\sum_{n=1}^\infty a_n$ and $\sum_{n=1}^\infty b_n$ be two series with non-negative terms ($a_n \ge 0$ and $b_n \ge 0$ for all $n \in \mathbb{N}$), and suppose there exists an index $N \in \mathbb{N}$ such that $a_n \le b_n$ for all $n > N$. Denote the $n$-th partial sums of the two series by $S_n := \sum_{k=1}^n a_k$ and $T_n := \sum_{k=1}^n b_k$. Because $a_n \ge 0$ and $b_n \ge 0$ for all $n \in \mathbb{N}$, both $\{S_n\}$ and $\{T_n\}$ are nondecreasing sequences.

# Theorem 1
Assume the dominating series $\sum_{n=1}^\infty b_n$ converges. By the convergence criterion for series with non-negative terms, its sequence of partial sums $\{T_n\}$ is bounded above by some finite constant $M := \sum_{n=1}^\infty b_n \in \mathbb{R}$, so $T_n \le M$ for all $n \in \mathbb{N}$.

For every index $n > N$, summing the inequality $a_k \le b_k$ from $k = N + 1$ to $n$ and adding $S_N$ yields
$$
\begin{gather}
S_n = S_N + \sum_{k=N+1}^n a_k \le S_N + \sum_{k=N+1}^n b_k = S_N + (T_n - T_N) \le S_N - T_N + M \tag{1}
\end{gather}
$$
Because $\{S_n\}$ is nondecreasing, $S_n \le S_N \le S_N + M$ for $1 \le n \le N$ as well. Consequently, $\{S_n\}$ is nondecreasing and bounded above by the finite real constant $S_N - T_N + M$ (or $S_N + M$). By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], the sequence of partial sums $\{S_n\}$ converges, proving that $\sum_{n=1}^\infty a_n$ converges.

---
# Theorem 2
Assume the minorant series $\sum_{n=1}^\infty a_n$ diverges. Suppose, for the sake of contradiction, that the dominating series $\sum_{n=1}^\infty b_n$ converges. By Theorem 1 established above, the convergence of $\sum_{n=1}^\infty b_n$ implies the convergence of $\sum_{n=1}^\infty a_n$, which directly contradicts the premise that $\sum_{n=1}^\infty a_n$ diverges.

Equivalently, because $a_n \ge 0$ and $\sum_{n=1}^\infty a_n$ diverges, the nondecreasing sequence $\{S_n\}$ is unbounded above ($S_n \to +\infty$). Rearranging step 1 for all $n > N$ gives
$$
\begin{gather}
T_n \ge S_n - (S_N - T_N) \quad \forall n > N \tag{2}
\end{gather}
$$
Because $S_n \to +\infty$, step 2 forces $T_n \to +\infty$. Therefore, $\{T_n\}$ diverges, proving that $\sum_{n=1}^\infty b_n$ diverges.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
