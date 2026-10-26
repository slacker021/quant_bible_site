---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-corollary-of-partial-limits-proposition/","dg-note-properties":{}}
---

# Corollary 1
Let $\{x_n\}$ be a sequence of real numbers with inferior limit $l := \liminf_{n \to \infty} x_n$ and superior limit $L := \limsup_{n \to \infty} x_n$ in the extended real line $\mathbb{R} \cup \{-\infty, +\infty\}$. For each $n \in \mathbb{N}$, denote the tail infimum and tail supremum by $i_n := \inf_{k \ge n} x_k$ and $s_n := \sup_{k \ge n} x_k$.

### Necessity
Assume $\lim_{n \to \infty} x_n = A$, where $A \in \mathbb{R} \cup \{-\infty, +\infty\}$. By definition of convergence (or divergence to $\pm\infty$), every subsequence $\{x_{n_k}\}$ of $\{x_n\}$ also converges (or tends) to $A$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that the Inferior (Superior) Limit is the Smallest (Largest) of its Partial Limits\|Partial Limits Proposition]], both $l$ and $L$ are partial limits of $\{x_n\}$, meaning there exist subsequences converging (or tending) to $l$ and $L$, respectively. By uniqueness of the limit of those subsequences, it follows that
$$
\begin{gather}
l = L = A \tag{1}
\end{gather}
$$

### Sufficiency
Conversely, assume $l = L = A$ for some $A \in \mathbb{R} \cup \{-\infty, +\infty\}$. By definition of the infimum and supremum over the tail $\{x_k \mid k \ge n\}$, every term $x_n$ satisfies
$$
\begin{gather}
i_n \le x_n \le s_n \quad \forall n \in \mathbb{N} \tag{2}
\end{gather}
$$
Consider the three exhaustive cases for $A$:
- **Case 1 ($A \in \mathbb{R}$ is finite):** Because $\lim_{n \to \infty} i_n = l = A \in \mathbb{R}$ and $\lim_{n \to \infty} s_n = L = A \in \mathbb{R}$, the sequence $\{x_n\}$ is bounded below and above, so $i_n$ and $s_n$ are finite real numbers for all $n \in \mathbb{N}$. Applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Squeeze Theorem\|Squeeze Theorem]] to step 2 yields $\lim_{n \to \infty} x_n = A$.
- **Case 2 ($A = +\infty$):** Because $l = \lim_{n \to \infty} i_n = +\infty$, for every real number $c \in \mathbb{R}$ there exists an index $N \in \mathbb{N}$ such that $i_n > c$ for all $n > N$. By step 2, $x_n \ge i_n > c$ for all $n > N$, which proves that $x_n \to +\infty$.
- **Case 3 ($A = -\infty$):** Because $L = \lim_{n \to \infty} s_n = -\infty$, for every real number $c \in \mathbb{R}$ there exists an index $N \in \mathbb{N}$ such that $s_n < c$ for all $n > N$. By step 2, $x_n \le s_n < c$ for all $n > N$, which proves that $x_n \to -\infty$.

---
# Corollary 2

### Necessity
Assume the sequence $\{x_n\}$ converges to a finite real number $A \in \mathbb{R}$, and let $\{x_{n_k}\}$ be an arbitrary subsequence of $\{x_n\}$. Let $\varepsilon > 0$ be given. By the definition of convergence, there exists an index $N \in \mathbb{N}$ such that $|x_n - A| < \varepsilon$ for all $n > N$. Because $n_1 < n_2 < \dots < n_k < \dots$ is a strictly increasing sequence of natural numbers, induction on $k$ guarantees that $n_k \ge k$ for all $k \in \mathbb{N}$. Consequently, for all $k > N$, it holds that $n_k \ge k > N$, which implies
$$
\begin{gather}
|x_{n_k} - A| < \varepsilon \quad \forall k > N \tag{3}
\end{gather}
$$
Thus, every subsequence $\{x_{n_k}\}$ converges to the same finite limit $A$.

### Sufficiency
Conversely, assume that every subsequence of $\{x_n\}$ converges to a finite real limit. First, observe that $\{x_n\}$ must be bounded; otherwise, by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that a Convergent Subsequence or Subsequence Tending to Infinity Can be Constructed From a Sequence of Real Numbers\|Lemma on Subsequences and Infinity]], one could extract a subsequence tending to $\infty$, which would diverge and contradict the hypothesis. Because $\{x_n\}$ is bounded, its inferior limit $l$ and superior limit $L$ are both finite real partial limits.

Suppose, for the sake of contradiction, that $l \neq L$. By the Partial Limits Proposition, there exist a subsequence $\{x_{n_k}\}$ converging to $l$ and a subsequence $\{x_{m_k}\}$ converging to $L$. Construct a new interleaved subsequence $\{x_{p_j}\}$ inductively by setting $p_1 := n_1$, choosing $p_2 := m_{k_1} > p_1$, choosing $p_3 := n_{k_2} > p_2$, and so forth, so that $p_1 < p_2 < p_3 < \dots$ with $x_{p_{2j-1}} \to l$ and $x_{p_{2j}} \to L$. Because the even-indexed and odd-indexed terms of the subsequence $\{x_{p_j}\}$ converge to distinct values $l \neq L$, the subsequence $\{x_{p_j}\}$ diverges, contradicting the hypothesis that every subsequence of $\{x_n\}$ converges. Therefore, $l = L \in \mathbb{R}$, and by Corollary 1, the parent sequence $\{x_n\}$ converges.

---
# Corollary 3
First, consider the restricted [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Bolzano-Weierstrass Lemma\|Bolzano-Weierstrass Lemma]], which asserts that every bounded sequence $\{x_n\}$ of real numbers contains a convergent subsequence. Because $\{x_n\}$ is bounded, there exist finite real constants $m, M \in \mathbb{R}$ such that $m \le x_n \le M$ for all $n \in \mathbb{N}$. Consequently, the tail bounds satisfy $m \le i_n \le s_n \le M$ for all $n \in \mathbb{N}$, ensuring that both $l = \liminf_{n \to \infty} x_n$ and $L = \limsup_{n \to \infty} x_n$ exist as finite real numbers:
$$
\begin{gather}
m \le l \le L \le M \tag{4}
\end{gather}
$$
By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that the Inferior (Superior) Limit is the Smallest (Largest) of its Partial Limits\|Partial Limits Proposition]], $l$ and $L$ are partial limits of $\{x_n\}$. By definition of a partial limit, there exists at least one subsequence $\{x_{n_k}\}$ converging to the finite real number $L$ (and at least one converging to $l$), establishing the restricted Bolzano-Weierstrass Lemma.

Second, consider the general form (the Lemma on Subsequences and Infinity) for an arbitrary sequence $\{x_n\}$ of real numbers. If $\{x_n\}$ is bounded, it contains a convergent subsequence by the restricted case above. If $\{x_n\}$ is unbounded, then either $\{x_n\}$ is unbounded above (in which case $L = \limsup_{n \to \infty} x_n = +\infty$) or $\{x_n\}$ is unbounded below (in which case $l = \liminf_{n \to \infty} x_n = -\infty$). Because $L$ and $l$ are partial limits of $\{x_n\}$ in $\mathbb{R} \cup \{-\infty, +\infty\}$, there exists a subsequence $\{x_{n_k}\}$ that tends to $+\infty$ or $-\infty$ (and therefore tends to $\infty$), establishing the general lemma.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
