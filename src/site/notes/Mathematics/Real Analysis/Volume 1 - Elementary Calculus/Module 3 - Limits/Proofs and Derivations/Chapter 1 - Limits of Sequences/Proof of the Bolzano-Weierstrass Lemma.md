---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-bolzano-weierstrass-lemma/","dg-note-properties":{}}
---

Let $\{x_n\}$ be an arbitrary bounded sequence of real numbers. To systematically extract a monotonic subsequence from $\{x_n\}$, an index $m \in \mathbb{N}$ is defined to be a _peak_ of the sequence if the term $x_m$ is greater than or equal to every subsequent term:
$$
\begin{gather}
\forall n \in \mathbb{N}, \quad (n > m) \implies (x_m \ge x_n) \tag{1}
\end{gather}
$$
The proof divides into two exhaustive cases depending on whether the set of peak indices of $\{x_n\}$ is infinite or finite.

### Case 1
Suppose the sequence $\{x_n\}$ possesses infinitely many peaks. Arrange the infinite set of peak indices in strictly increasing order as $m_1 < m_2 < m_3 < \dots < m_k < \dots$. For each $k \in \mathbb{N}$, because $m_k$ is a peak and $m_{k+1} > m_k$, the defining condition in step 1 guarantees that $x_{m_k} \ge x_{m_{k+1}}$. Consequently, the subsequence $\{x_{m_k}\}$ satisfies
$$
\begin{gather}
x_{m_1} \ge x_{m_2} \ge x_{m_3} \ge \dots \ge x_{m_k} \ge x_{m_{k+1}} \ge \dots \tag{2}
\end{gather}
$$
Thus, $\{x_{m_k}\}$ is a nonincreasing subsequence. Because the parent sequence $\{x_n\}$ is bounded, $\{x_{m_k}\}$ is bounded below. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], the nonincreasing, bounded-below subsequence $\{x_{m_k}\}$ converges to a finite real limit.

### Case 2
Suppose instead that the sequence $\{x_n\}$ possesses only finitely many peaks. Let $N \in \mathbb{N} \cup \{0\}$ denote the largest peak index (setting $N := 0$ if $\{x_n\}$ has no peaks at all). Then no index $n > N$ is a peak.

Select the first index $n_1 := N + 1 > N$. Because $n_1 > N$ is not a peak, the negation of step 1 implies that there exists at least one index $n_2 > n_1$ such that $x_{n_2} > x_{n_1}$. Because $n_2 > n_1 > N$, the index $n_2$ is also not a peak, so there exists an index $n_3 > n_2$ such that $x_{n_3} > x_{n_2}$. Proceeding inductively, given $n_k > N$, the fact that $n_k$ is not a peak guarantees the existence of an index $n_{k+1} > n_k$ with $x_{n_{k+1}} > x_{n_k}$. This inductive construction produces a subsequence $\{x_{n_k}\}$ with $n_1 < n_2 < n_3 < \dots$ satisfying
$$
\begin{gather}
x_{n_1} < x_{n_2} < x_{n_3} < \dots < x_{n_k} < x_{n_{k+1}} < \dots \tag{3}
\end{gather}
$$
Thus, $\{x_{n_k}\}$ is a strictly increasing (and hence nondecreasing) subsequence. Because the parent sequence $\{x_n\}$ is bounded, $\{x_{n_k}\}$ is bounded above. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], the nondecreasing, bounded-above subsequence $\{x_{n_k}\}$ converges to a finite real limit.

In both cases, $\{x_n\}$ contains a convergent subsequence.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
