---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-cauchy-condensation-test/","dg-note-properties":{}}
---

# Proposition
Let $\{a_n\}$ be a nonincreasing sequence of non-negative real numbers ($a_1 \ge a_2 \ge \dots \ge a_n \ge \dots \ge 0$). Denote the $n$-th partial sum of the original series $\sum_{n=1}^\infty a_n$ by $S_n := \sum_{j=1}^n a_j$, and the $k$-th partial sum of the condensed series $\sum_{k=0}^\infty 2^k a_{2^k}$ by $T_k := \sum_{j=0}^k 2^j a_{2^j}$. Because $a_n \ge 0$ and $2^j a_{2^j} \ge 0$, both $\{S_n\}$ and $\{T_k\}$ are nondecreasing sequences of partial sums. By the convergence criterion for series with non-negative terms, each series converges if and only if its sequence of partial sums is bounded above.

### Sufficiency
Assume the condensed series $\sum_{k=0}^\infty 2^k a_{2^k}$ converges, so there exists a finite constant $M > 0$ such that $T_k \le M$ for all $k \in \mathbb{N} \cup \{0\}$. For any $n \in \mathbb{N}$, choose $k \in \mathbb{N}$ large enough that $n \le 2^{k+1} - 1$. Because $a_j \ge 0$, the monotonicity of $\{S_n\}$ implies $S_n \le S_{2^{k+1}-1}$. Grouping the terms of $S_{2^{k+1}-1}$ into dyadic blocks of length $2^m$ (for $m = 0, 1, \dots, k$) yields
$$
\begin{gather}
S_{2^{k+1}-1} = a_1 + (a_2 + a_3) + (a_4 + a_5 + a_6 + a_7) + \dots + \left(a_{2^k} + a_{2^k + 1} + \dots + a_{2^{k+1}-1}\right) \tag{1}
\end{gather}
$$
Because $\{a_n\}$ is nonincreasing ($a_j \le a_{2^m}$ for all $j \ge 2^m$), each of the $2^m$ terms inside the $m$-th dyadic block is bounded above by its leading term $a_{2^m}$:
$$
\begin{gather}
a_2 + a_3 \le a_2 + a_2 = 2a_2 \\[2mm]
a_4 + a_5 + a_6 + a_7 \le a_4 + a_4 + a_4 + a_4 = 4a_4 \\[2mm]
a_{2^m} + a_{2^m + 1} + \dots + a_{2^{m+1}-1} \le 2^m a_{2^m} \tag{2}
\end{gather}
$$
Substituting the dyadic block bounds from step 2 into step 1 yields
$$
\begin{gather}
S_n \le S_{2^{k+1}-1} \le a_1 + 2a_2 + 4a_4 + \dots + 2^k a_{2^k} = T_k \le M \tag{3}
\end{gather}
$$
Because $S_n \le M$ for all $n \in \mathbb{N}$, the sequence $\{S_n\}$ is bounded above, and the series $\sum_{n=1}^\infty a_n$ converges.

### Necessity
Conversely, assume the original series $\sum_{n=1}^\infty a_n$ converges, so there exists a finite constant $L > 0$ such that $S_n \le L$ for all $n \in \mathbb{N}$. For any $k \in \mathbb{N}$, decompose the partial sum $S_{2^k}$ into dyadic blocks of length $2^{m-1}$ (for $m = 1, 2, \dots, k$) terminating at powers of $2$:
$$
\begin{gather}
S_{2^k} = a_1 + a_2 + (a_3 + a_4) + (a_5 + a_6 + a_7 + a_8) + \dots + \left(a_{2^{k-1}+1} + \dots + a_{2^k}\right) \tag{4}
\end{gather}
$$
Because $\{a_n\}$ is nonincreasing ($a_j \ge a_{2^m}$ for all $j \le 2^m$), each of the $2^{m-1}$ terms inside the $m$-th block is bounded below by its terminal element $a_{2^m}$:
$$
\begin{gather}
a_3 + a_4 \ge a_4 + a_4 = 2a_4 \\[2mm]
a_5 + a_6 + a_7 + a_8 \ge a_8 + a_8 + a_8 + a_8 = 4a_8 \\[2mm]
a_{2^{m-1}+1} + \dots + a_{2^m} \ge 2^{m-1} a_{2^m} \tag{5}
\end{gather}
$$
Applying the lower bounds of step 5 to step 4 gives
$$
\begin{gather}
S_{2^k} \ge a_1 + a_2 + 2a_4 + 4a_8 + \dots + 2^{k-1} a_{2^k} \\[2mm]
S_{2^k} \ge a_1 + \frac{1}{2} \left(2a_2 + 4a_4 + 8a_8 + \dots + 2^k a_{2^k}\right) \tag{6}
\end{gather}
$$
Observing that the parenthetical sum in step 6 equals $T_k - a_1$, step 6 simplifies to
$$
\begin{gather}
S_{2^k} \ge a_1 + \frac{1}{2} (T_k - a_1) = \frac{1}{2} a_1 + \frac{1}{2} T_k \tag{7}
\end{gather}
$$
Solving step 7 for $T_k$ and using the upper bound $S_{2^k} \le L$ yields
$$
\begin{gather}
T_k \le 2 S_{2^k} - a_1 \le 2L - a_1 \quad \forall k \in \mathbb{N} \tag{8}
\end{gather}
$$
Thus, $\{T_k\}$ is bounded above, proving that the condensed series $\sum_{k=0}^\infty 2^k a_{2^k}$ converges.

---
# Corollary
Consider the $p$-series $\sum_{n=1}^\infty \frac{1}{n^p}$ for $p \in \mathbb{R}$. If $p \le 0$, then $\frac{1}{n^p} = n^{-p} \ge 1$ for all $n \in \mathbb{N}$, so the terms fail to tend to zero and the series diverges by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|Necessary Condition for Series Convergence]].

Suppose $p > 0$. Then for every $n \in \mathbb{N}$, the strict inequality $1 \le n < n + 1$ implies $0 < n^p < (n + 1)^p$, so that
$$
\begin{gather}
\frac{1}{n^p} > \frac{1}{(n + 1)^p} > 0 \quad \forall n \in \mathbb{N} \tag{9}
\end{gather}
$$
Because the sequence $a_n := \frac{1}{n^p}$ is nonincreasing and non-negative, the Cauchy Condensation Test applies. Forming the condensed series $\sum_{k=0}^\infty 2^k a_{2^k}$ yields
$$
\begin{gather}
\sum_{k=0}^\infty 2^k \left( \frac{1}{(2^k)^p} \right) = \sum_{k=0}^\infty 2^k \cdot 2^{-kp} = \sum_{k=0}^\infty \left(2^{1-p}\right)^k \tag{10}
\end{gather}
$$
The series in step 10 is a geometric series with positive common ratio $r := 2^{1-p} > 0$. By the convergence theorem for geometric series, $\sum_{k=0}^\infty r^k$ converges if and only if $r < 1$:
$$
\begin{gather}
2^{1-p} < 1 = 2^0 \iff 1 - p < 0 \iff p > 1 \tag{11}
\end{gather}
$$
By the Cauchy Condensation Test, the $p$-series $\sum_{n=1}^\infty \frac{1}{n^p}$ converges for $p > 1$ and diverges for $p \le 1$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
