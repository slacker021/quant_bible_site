---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-series-rearrangement-proposition/","dg-note-properties":{}}
---

# Proposition 1
If the series $\sum_{n=1}^\infty x_n$ is absolutely convergent, then there's a value $x$ such that $\sum_{n=1}^\infty |x_n| < \infty$. By definition of absolute convergence, the sum of the series is invariant under any permutation of its terms.

Let $\sigma: \mathbb{N} \to \mathbb{N}$ be a [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 1 - General Mathematical Concepts and Notation/Chapter 4 - Functions and Cardinality\|bijection]]. Since the series is absolutely convergent, 
$$
\sum_{n=1}^\infty |x_{\sigma(n)}| = \sum_{n=1}^\infty |x_n| < \infty \tag{1}
$$
Because $\sum |x_{\sigma(n)}|$ converges, the rearranged series $\sum x_{\sigma(n)}$ must also converge. Furthermore, since the sum of an absolutely convergent series is independent of the order of summation, the value of the rearranged series is identically $x$.

---
# Proposition 2
If the series $\sum_{n=1}^\infty x_n$ is conditionally convergent, it means that $\sum_{n=1}^\infty x_n$ converges, but $\sum_{n=1}^\infty |x_n|$ diverges. Let $y$ be any real number. Consider the sub-series of positive terms $P = \{p_1, p_2, \dots\}$ and negative terms $N = \{q_1, q_2, \dots\}$ such that $p_i > 0$ and $q_j < 0$. 

For the original series to converge while $\sum |x_n| = \infty$, it must be that $\sum p_i = \infty$ and $\sum q_j = -\infty$. Additionally, since $\sum x_n$ converges, we must have $\lim_{n \to \infty} x_n = 0$.

Construct the rearranged series $z_k$ by greedily picking terms:
1. Sum the first $k_1$ terms of $P$ until the partial sum exceeds $y$.
2. Sum the next $k_2$ terms of $N$ until the partial sum falls below $y$.
3. Repeat this process indefinitely.

Because $\lim_{n \to \infty} x_n = 0$, the difference between the partial sums and $y$ approaches zero as more terms are added:
$$
\lim_{m \to \infty} \sum_{k=1}^m z_k = y \tag{2}
$$
Thus, by rearranging the terms, the series can be forced to converge to any real value of $y$.
$$
\textbf{Q.E.D}
$$