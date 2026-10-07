---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-that-a-convergent-subsequence-or-subsequence-tending-to-infinity-can-be-constructed-from-a-sequence-of-real-numbers/","dg-note-properties":{}}
---

Let $\{x_n\}$ be an arbitrary sequence of real numbers. By the fundamental axioms of real analysis, the sequence is definitively classified as either bounded or unbounded. The proof is partitioned to examine both conditions.

### Case 1
Assume $\{x_n\}$ is bounded. The Bolzano-Weierstrass Lemma strictly guarantees that every bounded sequence of real numbers contains at least one convergent subsequence. Thus, under this condition, a convergent subsequence can always be extracted, satisfying the lemma.

### Case 2
Assume $\{x_n\}$ is unbounded. By definition, it must be unbounded above, unbounded below, or unbounded in both directions.

Assume it is unbounded above. By definition, for any real number $M$, there are infinitely many terms in the sequence such that $x_n > M$. A subsequence $\{x_{n_k}\}$ tending to positive infinity can be recursively constructed as follows:
1. Choose an index $n_1$ such that $x_{n_1} > 1$.
2. Once $n_k$ has been chosen, select an index $n_{k+1} > n_k$ such that $x_{n_{k+1}} > k + 1$. Such an index is guaranteed to exist because the sequence is unbounded above.

This recursive process generates a subsequence $\{x_{n_k}\}$ such that for every index $k$, $x_{n_k} > k$. As $k \to \infty$, the bounding constraint forces $x_{n_k} \to +\infty$.

Conversely, assume the sequence is unbounded below. A strictly symmetric logic is applied to construct a subsequence trending toward negative infinity. Recursively choose indices such that $n_{k+1} > n_k$ and $x_{n_k} < -k$. As $k \to \infty$, this constructs a subsequence where $x_{n_k} \to -\infty$.

### Conclusion
If the parent sequence is bounded, a finite convergent subsequence is extracted via the Bolzano-Weierstrass Lemma. If the parent sequence is unbounded, a subsequence trending toward positive or negative infinity can be systematically constructed. In all possible topological states, the lemma is proven strictly true.
$$
\textbf{Q.E.D}
$$
