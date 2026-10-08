---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-cauchy-condensation-test/","dg-note-properties":{}}
---

# Proposition
Let $S_n = \sum_{j=1}^n a_j$ be the partial sums of the original series, and $T_k = \sum_{j=0}^k 2^j a_{2^j}$ be the partial sums of the condensed series. Because all terms are non-negative, both $\{S_n\}$ and $\{T_k\}$ are nondecreasing sequences. Convergence is entirely dependent upon establishing a finite upper bound for these sums.

### Sufficiency
Assume the condensed series converges, meaning its sequence of partial sums $T_k$ is bounded by some constant $M$. The terms of the original series can be grouped into blocks terminating at powers of 2. For an arbitrary index $n$, select $k$ such that $n < 2^{k+1}$. Because the terms are non-negative, the partial sum $S_n$ is strictly bounded by $S_{2^{k+1}-1}$. Expanding this bounded sum yields
$$S_{2^{k+1}-1} = a_1 + (a_2 + a_3) + (a_4 + a_5 + a_6 + a_7) + \dots + (a_{2^k} + \dots + a_{2^{k+1}-1}) \tag{1}$$
Because the sequence $\{a_n\}$ is monotonically decreasing ($a_j \le a_i$ for $j > i$), every term in a given bracket can be bounded upward by the first term in that bracket 
$$\begin{gather}
(a_2 + a_3) \le a_2 + a_2 = 2a_2 \tag{2}
(a_4 + a_5 + a_6 + a_7) \le a_4 + a_4 + a_4 + a_4 = 4a_4
\end{gather}$$

Generalizing this structure constructs the formal inequality
$$S_n \le S_{2^{k+1}-1} \le a_1 + 2a_2 + 4a_4 + \dots + 2^k a_{2^k} = T_k \tag{3}$$

Because $T_k$ is bounded by $M$, transitivity guarantees that $S_n \le M$ for all $n$. Thus, the original series $\sum a_n$ converges.

### Necessity
 Assume the original series $\sum a_n$ converges, meaning its sequence of partial sums $S_n$ is bounded by some constant $L$. To bound the condensed series, the original terms are grouped differently, bounding them from below using the terminal element of each block:  
$$S_{2^k} = a_1 + a_2 + (a_3 + a_4) + (a_5 + a_6 + a_7 + a_8) + \dots + (a_{2^{k-1}+1} + \dots + a_{2^k}) \tag{4}$$
Because the terms are decreasing, each element in a bracket can be bounded downward by the last term in that bracket:  
$$\begin{gather}
(a_3 + a_4) \ge a_4 + a_4 = 2a_4 \\
(a_5 + a_6 + a_7 + a_8) \ge a_8 + a_8 + a_8 + a_8 = 4a_8 \tag{5}
\end{gather}$$

Constructing the formal inequality reveals
$$\begin{gather}
S_{2^k} \ge a_1 + a_2 + 2a_4 + 4a_8 + \dots + 2^{k-1} a_{2^k} \\
S_{2^k} \ge a_1 + \frac{1}{2} (2a_2 + 4a_4 + 8a_8 + \dots + 2^k a_{2^k}) \tag{6}
\end{gather}$$

Recognizing the right-hand formulation, this becomes
$$S_{2^k} \ge a_1 + \frac{1}{2} (T_k - a_1) = \frac{1}{2} a_1 + \frac{1}{2} T_k \tag{7}$$

Rearranging to isolate $T_k$ yields
$$T_k \le 2 S_{2^k} - a_1 \tag{8}$$
Because $S_{2^k} \le L$, it follows that $T_k \le 2L - a_1$. The partial sums of the condensed series are strictly bounded, proving that the condensed series converges. 

---
# Corollary
If $p \le 0$, the terms do not tend to zero, so the series immediately diverges. If $p > 0$, the function $f(x) = \frac{1}{x^p}$ is strictly decreasing, satisfying the prerequisite for the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Condensation Test\|Cauchy Condensation Test]]. Applying the condensation operator generates the transformed series:  
$$\sum_{k=0}^\infty 2^k \left( \frac{1}{(2^k)^p} \right) = \sum_{k=0}^\infty 2^k \left( 2^{-kp} \right) = \sum_{k=0}^\infty (2^{1-p})^k \tag{9}$$

This is a standard geometric series with the common ratio $r = 2^{1-p}$. A geometric series converges if and only if $r < 1$: 
$$2^{1-p} < 1 \iff 1 - p < 0 \iff p > 1 \tag{10}$$
Thus, the condensed series converges strictly when $p > 1$. By the proven equivalence of the Cauchy Condensation Test, the original p-series converges if and only if $p > 1$. 
$$
\textbf{Q.E.D}
$$

