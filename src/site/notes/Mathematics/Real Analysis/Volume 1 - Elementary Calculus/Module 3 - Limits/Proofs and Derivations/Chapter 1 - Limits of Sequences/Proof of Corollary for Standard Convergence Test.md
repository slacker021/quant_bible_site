---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-corollary-for-standard-convergence-test/","dg-note-properties":{}}
---

# Corollary 1
Since $\sum_{n=1}^\infty y_{n}$ converges, its partial sums $Y_{N} = \sum_{n=1}^N y_{n}$ converge to some limit $B$. For all $n > N$, $|x_{n}| \le y_{n}$. Thus, the partial sums of $\sum_{n=1}^\infty |x_{n}|$ satisfy the condition of 
$$
X_{N} = \sum_{n=1}^N |x_{n}| \le \sum_{n=1}^N y_{n} = Y_{N} \tag{1}
$$
Since $Y_{N}$ converges to $Y$, and $X_{N}$ is bounded above by $Y_{N}$, the sequence $\{ A_{N} \}$ is monotonically increasing and bounded above by $Y$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Monotone Convergence Theorem]], $\{X_{N}  \}$ converges to some limit $X \le B$. Therefore, $\sum_{n=1}^\infty |x_{n}|$ converges, which means $\sum_{n=1}^\infty x_{n}$ converges absolutely. 

---
# Corollary 2
Let $\alpha = \lim_{ n \to \infty } \sqrt[n]{|x_{n}|}$. If $\alpha < 1$, then the series $\sum_{n = 1}^\infty$ converges absolutely. If $\alpha > 1$, the series diverges. 

### Case 1
Let $\alpha < 1$. Since $\lim \text{sup}_{{ n \to \infty }} \sqrt[n]{|x_{n}|} = \alpha < 1$, then there's a constant $r$ such that $\alpha < r < 1$. For all $n$ sufficiently large $\sqrt[n]{|x_{n}|} < r$, which implies $|x_{n}| < r^n$. The series $\sum_{n=1}^\infty r^n$ is a geometric sequence with ratio $r < 1$, so it converges. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Standard Comparison Test\|comparison test]], since $|x_{n}| < r^n$ for all $n$ sufficiently large, $\sum_{n=1}^\infty |x_{n}|$ also converges. Ergo, the original series converges absolutely. 

### Case 2
Let $\alpha > 1$. Since $\lim \text{sup}_{{ n \to \infty }} \sqrt[n]{|x_{n}|} = \alpha > 1$, there's a subsequence $\{n_{k}  \}$ such that $\sqrt[n_{k}]{|x_{n_{k}}|} > 1$ for all $k$. This implies that $|x_{n_{k}}| > 1$ for all $k$, so the terms of the series don't tend toward zero. By the divergence test of corollary 4, the terms of the series not tending to zero implies series divergence. 

---
# Corollary 3
Since $\lim_{n \to \infty} \left\vert{} \frac{x_{n+1}}{x_n} \right\vert{} = \alpha < 1$, there's a constant $r$ such that $\alpha < r < 1$. For all $n$ sufficiently large, 
$$
\left\vert{} \frac{x_{n+1}}{x_n} \right\vert{} < r \implies |x_{n+1}| < r|x_{n}| \tag{2}
$$
This gives the inequality $|x_{n}| < |x_{0}|r^n$ for some constant $|x_{0}$|. The series $\sum_{n=1}^\infty|x_{0}|r^n$ is a geometric series with ratio $r < 1$, so it converges. By the comparison test, since $|x_{n}| < |x_{0}|r^n$ for all $n$ sufficiently large, $\sum_{n=1}^\infty |x_{n}|$ also converges. Thus, the original series converges absolutely. 

---
# Corollary 4
Let's contradict the conclusion of the corollary statement, with this contradiction assuming that the series does indeed converge. If $\sum_{n=1}^\infty x_{n}$, then by the divergence test, it must be true that $\lim_{ n \to \infty } x_{n} \neq 0$. However, this contradicts the premise that $\lim_{ n \to \infty } x_{n} \neq 0$. Therefore, the claim that the series can't diverge must be true. 
$$
\textbf{Q.E.D}
$$

