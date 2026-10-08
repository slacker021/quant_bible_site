---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-bolzano-weierstrass-lemma/","dg-note-properties":{}}
---

Let $\{x_n\}$ be an arbitrary bounded sequence in $\mathbb{R}$. To systematically extract a monotonic subsequence, the concept of a "peak point" must be defined. An index $m \in \mathbb{N}$ is defined as a _peak_ of the sequence if it dominates all subsequent terms. Formally, 
$$x_m \ge x_n \quad \text{for all } n > m \tag{1}$$

The proof is bifurcated based on whether the sequence contains infinitely many peaks or finitely many peaks.

### Case 1
Let the infinite set of peak indices be ordered as $m_1 < m_2 < m_3 < \dots < m_k < \dots$. By the very definition of a peak, since $m_1$ is a peak and $m_2 > m_1$, it must hold that $x_{m_1} \ge x_{m_2}$. Extrapolating this logic to the entire set of peaks constructs a subsequence $\{x_{m_k}\}$ such that
$$x_{m_1} \ge x_{m_2} \ge x_{m_3} \ge \dots \ge x_{m_k} \ge \dots \tag{2}$$

This yields a nonincreasing subsequence. Because the parent sequence $\{x_n\}$ is bounded, the subsequence $\{x_{m_k}\}$ is bounded below. By the Weierstrass Theorem on Monotonic Sequences, a nonincreasing sequence bounded below is guaranteed to converge.

### Case 2
Because there are only a finite number of peaks, there must exist a maximum peak index, $N$. (If there are zero peaks, let $N=0$). Choose any index $n_1 > N$. Because $n_1$ is strictly greater than the final peak $N$, $n_1$ itself cannot be a peak. The failure to be a peak implies there must exist some index $n_2 > n_1$ such that $x_{n_2} > x_{n_1}$. Similarly, $n_2 > N$, so $n_2$ is not a peak. There must exist an index $n_3 > n_2$ such that $x_{n_3} > x_{n_2}$. Iterating this logic infinitely constructs a subsequence $\{x_{n_k}\}$ such that: 
$$x_{n_1} < x_{n_2} < x_{n_3} < \dots < x_{n_k} < \dots \tag{3}$$
This yields a strictly increasing subsequence. Because the parent sequence $\{x_n\}$ is bounded, the subsequence $\{x_{n_k}\}$ is bounded above. By the Weierstrass Theorem on Monotonic Sequences, a nondecreasing sequence bounded above is guaranteed to converge.

In all possible cases, a monotonic and bounded subsequence can be successfully extracted, thus proving the lemma.
$$
\textbf{Q.E.D}
$$
