---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-corollary-of-partial-limits-proposition/","dg-note-properties":{}}
---

# Corollary 1
Let $\{x_n\}$ be a sequence with inferior limit $l$ and superior limit $L$. Let $i_n = \inf_{k \ge n} x_k$ and $s_n = \sup_{k \ge n} x_k$.

### Necessity
Assume $\lim_{n \to \infty} x_n = A$, where $A \in \mathbb{R} \cup \{-\infty, +\infty\}$. By the fundamental properties of limits, every subsequence must identically converge to $A$. Since $l$ and $L$ are proven to be partial limits (limits of specific subsequences), they must both equal $A$. Thus, $l = L = A$.

### Sufficiency
Assume $l = L = A$. By the construction of sequence bounds, it is strictly true that for all $n \in \mathbb{N}$:  
$$i_n \le x_n \le s_n \tag{1}$$
Because $\lim_{n \to \infty} i_n = A$ and $\lim_{n \to \infty} s_n = A$, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Squeeze Theorem\|Proof of the Squeeze Theorem]] dictates that the parent sequence must conform to the identical bound, yielding $\lim_{n \to \infty} x_n = A$.

---
# Corollary 2

### Necessity
Assume the sequence $\{x_n\}$ converges to a finite real number $A$. Let $\{x_{n_k}\}$ be any arbitrary subsequence. By the definition of convergence, for any $\varepsilon > 0$, there is an $N$ such that $\vert x_n - A \vert < \varepsilon$ for all $n > N$. Because $n_k \ge k$, there exists an index $K$ such that $n_k > N$ for all $k > K$. Thus, $\vert x_{n_k} - A \vert < \varepsilon$ for all $k > K$. Every subsequence definitively converges to $A$.

### Sufficiency
Assume every subsequence of $\{x_n\}$ converges. If subsequences converged to distinct limits, the sequence would possess multiple differing partial limits. However, because all subsequences converge, they must converge to a single, finite limit. Consequently, the smallest partial limit ($l$) and the largest partial limit ($L$) must be equal and finite. By the proven result of corollary 1, the equality $l = L$ strictly guarantees that the parent sequence $\{x_n\}$ converges.

---
# Corollary 3
The restricted [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Bolzano-Weierstrass Lemma\|Bolzano-Weierstrass Lemma]] asserts that every bounded sequence contains a convergent subsequence. Let $\{x_n\}$ be an arbitrary bounded sequence. Because the sequence is bounded, its absolute supremum and absolute infimum exist as finite real numbers. Consequently, its superior limit $L = \limsup_{n \to \infty} x_n$ and inferior limit $l = \liminf_{n \to \infty} x_n$ must exist as definitive, finite real numbers.

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that the Inferior (Superior) Limit is the Smallest (Largest) of its Partial Limits\|Partial Limits Proposition]], $L$ and $l$ are mathematically classified as partial limits of the sequence. A partial limit is defined as a point to which at least one subsequence converges. Because $L$ (and $l$) exists as a finite scalar, there is mathematically guaranteed to exist at least one subsequence converging to it. Thus, a convergent subsequence has been successfully identified, proving the lemma directly from partial limit properties.
$$
\textbf{Q.E.D}
$$
