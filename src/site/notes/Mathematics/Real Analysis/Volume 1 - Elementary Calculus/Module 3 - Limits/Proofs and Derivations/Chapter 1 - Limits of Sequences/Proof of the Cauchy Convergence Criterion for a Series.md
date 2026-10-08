---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-cauchy-convergence-criterion-for-a-series/","dg-note-properties":{}}
---

# Theorem
By definition, the convergence of an infinite series $\sum_{n=1}^\infty a_n$ is logically synonymous with the convergence of its sequence of partial sums, $\{s_n\}$, where $s_n = \sum_{k=1}^n a_k$. By the Cauchy Criterion for Sequences, the sequence $\{s_n\}$ converges if and only if it is a Cauchy sequence. The definition of a Cauchy sequence dictates that for any $\varepsilon > 0$, there exists an index $N \in \mathbb{N}$ such that for all $m > N$ and $p > N$, the absolute difference is strictly bounded: $\vert s_m - s_p \vert < \varepsilon$.

Without loss of generality, assume $m > p$. Let the lesser index be denoted as $n-1$, meaning $p = n-1$. Thus, the Cauchy condition becomes $\vert s_m - s_{n-1} \vert < \varepsilon$ for all $m \ge n > N$. Expanding the partial sums reveals the internal components:  $$s_m - s_{n-1} = (a_1 + a_2 + \dots + a_m) - (a_1 + a_2 + \dots + a_{n-1}) = a_n + a_{n+1} + \dots + a_m \tag{1}$$
Which can then be condensed into
$$s_m - s_{n-1} = \sum_{k=n}^m a_k \tag{2}$$

Substituting this algebraic simplification back into the sequence constraint yields
$$\left\vert \sum_{k=n}^m a_k \right\vert < \varepsilon \tag{3}$$

This completes the equivalence.

# Corollary
Assume the series converges. By the proven Cauchy Criterion, for any $\varepsilon > 0$, there exists an index $N$ such that $\left\vert \sum_{k=n}^m a_k \right\vert < \varepsilon$ for all $m \ge n > N$. By isolating the evaluation to a single step where $m = n$, the summation collapses to a single term: 
$$\left\vert \sum_{k=n}^n a_k \right\vert = \vert a_n \vert < \varepsilon \quad \text{for all } n > N \tag{4}$$
This inequality is the exact mathematical definition of the sequence $\{a_n\}$ converging to the limit $0$. Thus, terms trending to zero is a strictly necessary condition for series convergence.
$$
\textbf{Q.E.D}
$$