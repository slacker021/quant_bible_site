---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-series-rearrangement-proposition/","dg-note-properties":{}}
---

# Proposition 1
Let $\sum_{n=1}^\infty x_n$ be an absolutely convergent series with sum $x := \sum_{n=1}^\infty x_n = \lim_{n \to \infty} s_n$, where $s_n := \sum_{k=1}^n x_k$ denotes the $n$-th partial sum, and let $\sigma : \mathbb{N} \to \mathbb{N}$ be a [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 1 - General Mathematical Concepts and Notation/Chapter 4 - Functions and Cardinality\|bijection]]. Denote the $m$-th partial sum of the rearranged series $\sum_{k=1}^\infty x_{\sigma(k)}$ by $s'_m := \sum_{k=1}^m x_{\sigma(k)}$.

First, to verify that $\sum_{k=1}^\infty x_{\sigma(k)}$ converges absolutely, let $S := \sum_{n=1}^\infty |x_n| < +\infty$. For any $m \in \mathbb{N}$, define $M := \max\{\sigma(1), \sigma(2), \dots, \sigma(m)\} \in \mathbb{N}$. Because $\sigma$ is injective and $|x_n| \ge 0$, the finite sum of $m$ non-negative terms is bounded above by the partial sum of the first $M$ absolute terms:
$$
\begin{gather}
\sum_{k=1}^m |x_{\sigma(k)}| \le \sum_{n=1}^M |x_n| \le S < +\infty \quad \forall m \in \mathbb{N} \tag{1}
\end{gather}
$$
Because the partial sums of $\sum_{k=1}^\infty |x_{\sigma(k)}|$ are nondecreasing and bounded above by $S$, the rearranged series $\sum_{k=1}^\infty x_{\sigma(k)}$ converges absolutely (and therefore converges in $\mathbb{R}$).

Second, to prove that $\lim_{m \to \infty} s'_m = x$, let $\varepsilon > 0$ be arbitrary. Because $\lim_{n \to \infty} s_n = x$ and $\sum_{n=1}^\infty |x_n|$ satisfies the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|Cauchy Convergence Criterion for a Series]], there exists an index $N \in \mathbb{N}$ such that
$$
\begin{gather}
|s_N - x| < \frac{\varepsilon}{2} \quad \text{and} \quad \sum_{n=N+1}^P |x_n| < \frac{\varepsilon}{2} \quad \forall P > N \tag{2}
\end{gather}
$$
Because $\sigma : \mathbb{N} \to \mathbb{N}$ is surjective, every natural number $n \in \{1, 2, \dots, N\}$ possesses a preimage $\sigma^{-1}(n) \in \mathbb{N}$. Define the threshold index
$$
\begin{gather}
K := \max\left\{\sigma^{-1}(1), \sigma^{-1}(2), \dots, \sigma^{-1}(N)\right\} \in \mathbb{N} \tag{3}
\end{gather}
$$
For every $m > K$, the set of indices $\{\sigma(1), \sigma(2), \dots, \sigma(m)\}$ contains $\{1, 2, \dots, N\}$. Consequently, in the difference $s'_m - s_N = \sum_{k=1}^m x_{\sigma(k)} - \sum_{n=1}^N x_n$, the terms $x_1, x_2, \dots, x_N$ cancel completely, leaving only terms $x_{\sigma(k)}$ with $\sigma(k) > N$. Setting $P := \max\{\sigma(1), \dots, \sigma(m)\} > N$ and applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] bersama step 2 yields
$$
\begin{gather}
|s'_m - s_N| = \left| \sum_{\substack{1 \le k \le m \\ \sigma(k) > N}} x_{\sigma(k)} \right| \le \sum_{\substack{1 \le k \le m \\ \sigma(k) > N}} |x_{\sigma(k)}| \le \sum_{n=N+1}^P |x_n| < \frac{\varepsilon}{2} \quad \forall m > K \tag{4}
\end{gather}
$$
Combining step 2 and step 4 via the Triangle Inequality shows that for all $m > K$:
$$
\begin{gather}
|s'_m - x| \le |s'_m - s_N| + |s_N - x| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{5}
\end{gather}
$$
Therefore, $\lim_{m \to \infty} s'_m = x$, and the rearranged series $\sum_{k=1}^\infty x_{\sigma(k)}$ converges to $x$.

---
# Proposition 2
Assume the series $\sum_{n=1}^\infty x_n$ is conditionally convergent: $\sum_{n=1}^\infty x_n$ converges to a finite sum, whereas $\sum_{n=1}^\infty |x_n| = +\infty$. By the Necessary Condition for Series Convergence, $\lim_{n \to \infty} x_n = 0$.

For each $n \in \mathbb{N}$, define the non-negative positive and negative parts of $x_n$:
$$
\begin{gather}
x_n^+ := \frac{|x_n| + x_n}{2} \ge 0 \quad \text{and} \quad x_n^- := \frac{|x_n| - x_n}{2} \ge 0 \tag{6}
\end{gather}
$$
so that $x_n = x_n^+ - x_n^-$ and $|x_n| = x_n^+ + x_n^-$. If both $\sum_{n=1}^\infty x_n^+$ and $\sum_{n=1}^\infty x_n^-$ converged, then $\sum_{n=1}^\infty |x_n| = \sum_{n=1}^\infty (x_n^+ + x_n^-)$ would converge; if one converged and the other diverged, then $\sum_{n=1}^\infty x_n = \sum_{n=1}^\infty (x_n^+ - x_n^-)$ would diverge by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Properties of Series\|linearity of convergent series]]. Because $\sum_{n=1}^\infty x_n$ converges while $\sum_{n=1}^\infty |x_n|$ diverges, both subseries must diverge to $+\infty$:
$$
\begin{gather}
\sum_{n=1}^\infty x_n^+ = +\infty \quad \text{and} \quad \sum_{n=1}^\infty x_n^- = +\infty \tag{7}
\end{gather}
$$
Partition the terms of $\{x_n\}$ in their original order into the subsequence of non-negative terms $P = \{p_1, p_2, p_3, \dots\}$ (where $p_i \ge 0$) and the subsequence of strictly negative terms $Q = \{q_1, q_2, q_3, \dots\}$ (where $q_j < 0$). By step 7, $\sum_{i=1}^\infty p_i = +\infty$ and $\sum_{j=1}^\infty q_j = -\infty$, and $\lim_{i \to \infty} p_i = \lim_{j \to \infty} q_j = 0$.

Let $y \in \mathbb{R}$ be any prescribed real number. Construct a rearranged series $\sum_{k=1}^\infty z_k$ inductively in alternating blocks of terms from $P$ and $Q$:
1. **First Positive Block:** Because $\sum_{i=1}^\infty p_i = +\infty$, let $i_1 \in \mathbb{N}$ be the minimal index such that $S^{(1)} := \sum_{i=1}^{i_1} p_i > y$. By minimality of $i_1$, if $i_1 > 1$, then $\sum_{i=1}^{i_1 - 1} p_i \le y$, so $y < S^{(1)} \le y + p_{i_1}$.
2. **First Negative Block:** Because $\sum_{j=1}^\infty q_j = -\infty$, let $j_1 \in \mathbb{N}$ be the minimal index such that $T^{(1)} := S^{(1)} + \sum_{j=1}^{j_1} q_j < y$. By minimality of $j_1$, the partial sum immediately prior to adding $q_{j_1}$ is $\ge y$, so $y + q_{j_1} \le T^{(1)} < y$.
3. **Inductive Continuation:** Proceeding inductively for each stage $r \ge 2$, append consecutive unused terms $p_{i_{r-1}+1}, \dots, p_{i_r}$ from $P$ until the first index $i_r$ where the cumulative sum $S^{(r)} > y$, and then append consecutive unused terms $q_{j_{r-1}+1}, \dots, q_{j_r}$ from $Q$ until the first index $j_r$ where the cumulative sum $T^{(r)} < y$.

At every step $m$ during the $r$-th positive block or $r$-th negative block (for $r \ge 2$), the partial sum $s'_m := \sum_{k=1}^m z_k$ of the rearranged series lies between the overshoot bounds of the preceding and current turnarounds:
$$
\begin{gather}
|s'_m - y| \le \max\left(p_{i_r}, \, |q_{j_{r-1}}|, \, |q_{j_r}|\right) \tag{8}
\end{gather}
$$
Because $i_r \ge r$ and $j_r \ge r$, and $\lim_{i \to \infty} p_i = \lim_{j \to \infty} |q_j| = 0$, the right-hand side of step 8 tends to $0$ as $m \to \infty$ (and hence $r \to \infty$):
$$
\begin{gather}
\lim_{m \to \infty} \sum_{k=1}^m z_k = y \tag{9}
\end{gather}
$$
Thus, there exists a rearrangement of $\sum_{n=1}^\infty x_n$ converging to $y$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
