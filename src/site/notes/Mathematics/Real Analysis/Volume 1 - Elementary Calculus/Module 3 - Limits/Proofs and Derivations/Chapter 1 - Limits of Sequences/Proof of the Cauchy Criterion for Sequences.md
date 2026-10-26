---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-cauchy-criterion-for-sequences/","dg-note-properties":{}}
---

# Necessity
Assume the sequence $\{x_n\}$ converges to a finite limit $A \in \mathbb{R}$, and let $\varepsilon > 0$ be arbitrary. By the definition of convergence applied to the tolerance $\frac{\varepsilon}{2} > 0$, there exists an index $N \in \mathbb{N}$ such that $|x_n - A| < \frac{\varepsilon}{2}$ for all $n > N$.

For any two indices $n > N$ and $m > N$, applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] by inserting and subtracting $A$ yields
$$
\begin{gather}
|x_n - x_m| = |(x_n - A) + (A - x_m)| \le |x_n - A| + |x_m - A| \\[2mm]
|x_n - x_m| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{1}
\end{gather}
$$
Thus, $\{x_n\}$ is a Cauchy sequence.

---
# Sufficiency
Conversely, assume $\{x_n\}$ is a Cauchy sequence. First, verify that $\{x_n\}$ is bounded. Instantiating the Cauchy definition with $\varepsilon = 1 > 0$ yields an index $N_0 \in \mathbb{N}$ such that $|x_n - x_m| < 1$ for all $m, n > N_0$. Fixing $m = N_0 + 1 > N_0$, the Triangle Inequality implies that for all $n > N_0$:
$$
\begin{gather}
|x_n| = |(x_n - x_{N_0+1}) + x_{N_0+1}| \le |x_n - x_{N_0+1}| + |x_{N_0+1}| < 1 + |x_{N_0+1}| \tag{2}
\end{gather}
$$
Defining $M := \max(|x_1|, |x_2|, \dots, |x_{N_0}|, |x_{N_0+1}| + 1) + 1$, it follows that $|x_n| < M$ for all $n \in \mathbb{N}$, so $\{x_n\}$ is bounded.

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Bolzano-Weierstrass Lemma\|Bolzano-Weierstrass Lemma]], the bounded real sequence $\{x_n\}$ contains a convergent subsequence $\{x_{n_k}\}$ that converges to some finite real limit $L \in \mathbb{R}$.

To demonstrate that the entire sequence $\{x_n\}$ converges to $L$, let $\varepsilon > 0$ be arbitrary. Because $\{x_n\}$ is a Cauchy sequence, there exists an index $N \in \mathbb{N}$ such that $|x_n - x_m| < \frac{\varepsilon}{2}$ for all $m, n > N$. Furthermore, because $\lim_{k \to \infty} x_{n_k} = L$, there exists an index $K \in \mathbb{N}$ such that $|x_{n_k} - L| < \frac{\varepsilon}{2}$ for all $k > K$.

Select a fixed index $k > \max(K, N)$. Because $n_1 < n_2 < \dots < n_k$ is a strictly increasing sequence of natural numbers, $n_k \ge k > N$. For any index $n > N$, applying the Triangle Inequality with the anchor term $x_{n_k}$ gives
$$
\begin{gather}
|x_n - L| = |(x_n - x_{n_k}) + (x_{n_k} - L)| \le |x_n - x_{n_k}| + |x_{n_k} - L| \tag{3}
\end{gather}
$$
Because both $n > N$ and $n_k > N$, the Cauchy bound gives $|x_n - x_{n_k}| < \frac{\varepsilon}{2}$; because $k > K$, the subsequence convergence bound gives $|x_{n_k} - L| < \frac{\varepsilon}{2}$. Substituting both bounds into step 3 yields
$$
\begin{gather}
|x_n - L| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \quad \forall n > N \tag{4}
\end{gather}
$$
Therefore, the sequence $\{x_n\}$ converges to $L$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
