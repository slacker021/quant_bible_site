---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-alternating-series-test/","dg-note-properties":{}}
---

Let $\sum_{n=1}^\infty x_n$ be an alternating series of the form $x_n = (-1)^{n+1} y_n$ (the case $x_n = (-1)^n y_n$ follows identically by multiplying the series by $-1$), where $\{y_n\}$ is a nonincreasing sequence of non-negative real numbers ($y_n \ge y_{n+1} \ge 0$ for all $n \in \mathbb{N}$) satisfying $\lim_{n \to \infty} y_n = 0$. Let $S_n := \sum_{k=1}^n (-1)^{k+1} y_k$ denote the $n$-th partial sum of the series:
$$
\begin{gather}
S_1 = y_1 \\[2mm]
S_2 = y_1 - y_2 \\[2mm]
S_3 = y_1 - y_2 + y_3 \\[2mm]
S_4 = y_1 - y_2 + y_3 - y_4 \\[2mm]
\vdots \tag{1}
\end{gather}
$$
Because $\{y_n\}$ is nonincreasing, the difference $y_{k} - y_{k+1} \ge 0$ is non-negative for every $k \in \mathbb{N}$. This structural property governs the behavior of the even-indexed and odd-indexed subsequences of $\{S_n\}$:
- **Even Partial Sums ($n = 2m$):** Grouping consecutive pairs of terms in $S_{2m}$ yields
$$
\begin{gather}
S_{2m} = (y_1 - y_2) + (y_3 - y_4) + \dots + (y_{2m-1} - y_{2m}) \tag{2}
\end{gather}
$$
Because each grouped difference satisfies $y_{2i-1} - y_{2i} \ge 0$, it follows that $S_{2m} \ge 0$ and $S_{2m+2} - S_{2m} = y_{2m+1} - y_{2m+2} \ge 0$ for all $m \in \mathbb{N}$.
- **Odd Partial Sums ($n = 2m + 1$):** For any $m \in \mathbb{N}$, the $(2m+1)$-th partial sum satisfies both
$$
\begin{gather}
S_{2m+1} = S_{2m} + y_{2m+1} \quad \text{and} \quad S_{2m+1} = S_{2m-1} - (y_{2m} - y_{2m+1}) \tag{3}
\end{gather}
$$
Since $y_{2m} - y_{2m+1} \ge 0$, the second relation in step 3 implies $S_{2m+1} \le S_{2m-1}$ for all $m \in \mathbb{N}$.

Consequently, the two subsequences of partial sums exhibit opposite monotonicity:
1. The subsequence of even partial sums $\{S_{2m}\}$ is nondecreasing:
$$
\begin{gather}
S_2 \le S_4 \le S_6 \le \dots \le S_{2m} \le S_{2m+2} \le \dots \tag{4}
\end{gather}
$$
2. The subsequence of odd partial sums $\{S_{2m-1}\}$ is nonincreasing:
$$
\begin{gather}
S_1 \ge S_3 \ge S_5 \ge \dots \ge S_{2m-1} \ge S_{2m+1} \ge \dots \tag{5}
\end{gather}
$$
Moreover, because $y_{2m+1} \ge 0$, the first relation in step 3 guarantees that $S_{2m} \le S_{2m+1}$ for every $m \in \mathbb{N}$. Combining steps 4 and 5 produces the nested chain of inequalities:
$$
\begin{gather}
S_2 \le S_4 \le \dots \le S_{2m} \le S_{2m+2} \le \dots \le S_{2m+1} \le S_{2m-1} \le \dots \le S_3 \le S_1 \tag{6}
\end{gather}
$$
Step 6 demonstrates that $\{S_{2m}\}$ is nondecreasing and bounded above by $S_1$, while $\{S_{2m+1}\}$ is nonincreasing and bounded below by $S_2$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], both subsequences converge to finite real limits:
$$
\begin{gather}
\lim_{m \to \infty} S_{2m} = L_e \quad \text{and} \quad \lim_{m \to \infty} S_{2m+1} = L_o \tag{7}
\end{gather}
$$

### Equality of Subsequential Limits
From step 3, the difference between consecutive odd and even partial sums is
$$
\begin{gather}
S_{2m+1} - S_{2m} = y_{2m+1} \tag{8}
\end{gather}
$$
Because $\lim_{n \to \infty} y_n = 0$, the subsequence $\{y_{2m+1}\}$ also converges to $0$. Taking the limit as $m \to \infty$ across step 8 yields
$$
\begin{gather}
L_o - L_e = \lim_{m \to \infty} (S_{2m+1} - S_{2m}) = \lim_{m \to \infty} y_{2m+1} = 0 \implies L_o = L_e =: L \tag{9}
\end{gather}
$$
Because both the even-indexed subsequence $\{S_{2m}\}$ and the odd-indexed subsequence $\{S_{2m+1}\}$ converge to the common limit $L$, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Theorem Involving Odd and Even-Indexed Sequences\|theorem on even and odd-indexed sequences]] guarantees that the full sequence of partial sums $\{S_n\}$ converges to $L$. Therefore, the alternating series $\sum_{n=1}^\infty x_n$ converges.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
