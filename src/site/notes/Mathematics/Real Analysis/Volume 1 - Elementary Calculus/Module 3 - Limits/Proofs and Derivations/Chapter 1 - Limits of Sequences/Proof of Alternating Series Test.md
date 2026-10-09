---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-alternating-series-test/","dg-note-properties":{}}
---

Let $S_n$ denote the $n$-th partial sum of the series. Without loss of generality, assume the series takes the form $\sum_{n=1}^{\infty} (-1)^{n+1} b_n = b_1 - b_2 + b_3 - b_4 + \dots$. The partial sums can be expressed as
$$
S_1 = b_1 \\
S_2 = b_1 - b_2 \\
S_3 = b_1 - b_2 + b_3 \\
S_4 = b_1 - b_2 + b_3 - b_4 \\ 
\dots \tag{1}
$$
Since $\{b_n\}$ is a decreasing sequence, it follows that $b_n \ge b_{n+1}$ for all $n \ge 1$. This property allows for the following observations regarding the partial sums:
- For any even $k = 2m$, the partial sum can be grouped as
$$
S_{2m} = (b_1 - b_2) + (b_3 - b_4) + \dots + (b_{2m-1} - b_{2m}) \tag{2}
$$
Because each term $(b_{2i-1} - b_{2i}) \ge 0$, it follows that $S_{2m} \ge 0$ for all $m \in \mathbb{N}$. Furthermore, as $m$ increases, more non-negative terms are added, but the magnitude of the subtracted terms decreases.
- For any odd $k = 2m+1$, the partial sum can be expressed as
$$
S_{2m+1} = S_{2m} + b_{2m+1} \tag{3}
$$
Alternatively, $S_{2m+1}$ as $S_{2m-1} - (b_{2m} - b_{2m+1})$ can be viewed. Since $b_{2m} \ge b_{2m+1}$, it follows that $S_{2m+1} \le S_{2m-1}$. 

Now, by examining the subsequences of partial sums, it's demonstrated that
1. The subsequence of even partial sums $\{S_{2m}\}$ is non-decreasing:
$$
S_2 \le S_4 \le S_6 \le \dots \tag{4}
$$
2. The subsequence of odd partial sums $\{S_{2m+1}\}$ is non-increasing:
$$
S_1 \ge S_3 \ge S_5 \ge \dots \tag{5}
$$
Additionally, for any $m$, we have $S_{2m+1} \ge S_{2m}$ because $b_{2m+1} \ge 0$. Combining these, the following chain of inequalities is established:
$$
S_1 \ge S_3 \ge S_5 \ge \dots \ge S_{2m} \ge S_{2m+2} \ge \dots \ge S_2 \tag{6}
$$
This demonstrates that the sequence of partial sums $\{S_n\}$ is bounded:
$$
S_1 \ge S_n \ge S_2
$$
for all $n$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Monotone Convergence Theorem]], every bounded monotonic sequence converges. Therefore, the even subsequence $\{S_{2m}\}$ converges to some limit $L_e$, and the odd subsequence $\{S_{2m+1}\}$ converges to some limit $L_o$.

### Equality of Limits
The difference between consecutive partial sums is given by
$$
|S_{2m+1} - S_{2m}| = b_{2m+1} \tag{7}
$$
Since it is given that $\lim_{n \to \infty} b_n = 0$, it follows that
$$
\lim_{m \to \infty} (S_{2m+1} - S_{2m}) = 0 \implies \lim_{m \to \infty} S_{2m+1} = \lim_{m \to \infty} S_{2m} \tag{8}
$$
Thus, $L_o = L_e = L$. Since both the even and odd subsequences converge to the same limit $L$, the entire sequence of partial sums $\{S_n\}$ converges to $L$.

Therefore, the series $\sum_{n=1}^{\infty} a_n$ is convergent.
$$
\textbf{Q.E.D}
$$
