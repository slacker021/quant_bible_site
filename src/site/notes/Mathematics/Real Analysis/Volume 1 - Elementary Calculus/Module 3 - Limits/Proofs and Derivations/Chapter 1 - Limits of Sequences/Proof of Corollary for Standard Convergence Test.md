---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-corollary-for-standard-convergence-test/","dg-note-properties":{}}
---

# Corollary 1
Suppose there exists an index $N_0 \in \mathbb{N}$ such that $|x_n| \le y_n$ for all $n > N_0$, and assume that $\sum_{n=1}^\infty y_n$ converges to a finite sum $B := \sum_{n=1}^\infty y_n$. Because $y_n \ge |x_n| \ge 0$ for all $n > N_0$, the partial sums $Y_m := \sum_{n=1}^m y_n$ satisfy $\sum_{n=N_0+1}^m y_n = Y_m - Y_{N_0} \le B - Y_{N_0}$ for all $m > N_0$.

Consequently, for any $m > N_0$, the $m$-th partial sum $X_m := \sum_{n=1}^m |x_n|$ of the series of absolute values satisfies
$$
\begin{gather}
X_{m} = X_{N_0} + \sum_{n=N_0+1}^m |x_{n}| \le X_{N_0} + \sum_{n=N_0+1}^m y_{n} \le X_{N_0} + (B - Y_{N_0}) \tag{1}
\end{gather}
$$
Because $|x_n| \ge 0$ for all $n \in \mathbb{N}$, the sequence of partial sums $\{X_m\}$ is nondecreasing and bounded above by the constant $M := X_{N_0} + B - Y_{N_0}$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], $\{X_m\}$ converges to a finite limit $X \le M$. Therefore, $\sum_{n=1}^\infty |x_n|$ converges, establishing that $\sum_{n=1}^\infty x_n$ converges absolutely.

---
# Corollary 2
Let $\alpha := \limsup_{n \to \infty} \sqrt[n]{|x_n|} \ge 0$.

### Case 1
Suppose $\alpha < 1$. Because $\alpha \ge 0$, there exists a real constant $r$ satisfying $0 \le \alpha < r < 1$. By the definition of the superior limit, there exists an index $N \in \mathbb{N}$ such that for all $n > N$:
$$
\begin{gather}
\sqrt[n]{|x_{n}|} < r \implies |x_{n}| < r^n \tag{2}
\end{gather}
$$
Because $0 < r < 1$, the geometric series $\sum_{n=1}^\infty r^n$ converges. By Corollary 1 (or the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Standard Comparison Test\|Standard Comparison Test]]), the bound $|x_n| < r^n$ for all $n > N$ guarantees that $\sum_{n=1}^\infty x_n$ converges absolutely.

### Case 2
Suppose $\alpha > 1$. Because $\alpha = \limsup_{n \to \infty} \sqrt[n]{|x_n|} > 1$ is the largest partial limit of $\left\{\sqrt[n]{|x_n|}\right\}$, there exists a subsequence $\left\{x_{n_k}\right\}$ such that $\sqrt[n_k]{|x_{n_k}|} > 1$, and thus $|x_{n_k}| > 1$, for all $k \in \mathbb{N}$. Consequently, $x_n$ does not converge to $0$ as $n \to \infty$. By Corollary 4 below, the series $\sum_{n=1}^\infty x_n$ diverges.

---
# Corollary 3
Suppose $x_n \neq 0$ for all sufficiently large $n$, and let $\alpha := \lim_{n \to \infty} \left| \frac{x_{n+1}}{x_n} \right| \ge 0$.

### Case 1
Suppose $\alpha < 1$. Choose a real number $r$ such that $0 \le \alpha < r < 1$. By the definition of the limit, there exists an index $N \in \mathbb{N}$ such that for all $n \ge N$:
$$
\begin{gather}
\left| \frac{x_{n+1}}{x_n} \right| < r \implies |x_{n+1}| < r|x_{n}| \tag{3}
\end{gather}
$$
Applying step 3 inductively for $n > N$ yields
$$
\begin{gather}
|x_n| < r |x_{n-1}| < r^2 |x_{n-2}| < \dots < r^{n-N} |x_N| = \left(\frac{|x_N|}{r^N}\right) r^n \tag{4}
\end{gather}
$$
Setting the positive constant $C := \frac{|x_N|}{r^N} > 0$, the geometric series $\sum_{n=1}^\infty C r^n = C \sum_{n=1}^\infty r^n$ converges because $0 < r < 1$. By Corollary 1, since $|x_n| < C r^n$ for all $n > N$, the series $\sum_{n=1}^\infty x_n$ converges absolutely.

### Case 2
Suppose $\alpha > 1$. By the definition of the limit $\lim_{n \to \infty} \left|\frac{x_{n+1}}{x_n}\right| = \alpha > 1$, there exists an index $N \in \mathbb{N}$ such that for all $n \ge N$:
$$
\begin{gather}
\left| \frac{x_{n+1}}{x_n} \right| > 1 \implies |x_{n+1}| > |x_n| > 0 \tag{5}
\end{gather}
$$
By induction, $|x_n| > |x_N| > 0$ for all $n > N$, which prevents $\{x_n\}$ from converging to $0$. By Corollary 4 below, the series $\sum_{n=1}^\infty x_n$ diverges.

---
# Corollary 4
Assume that $\lim_{n \to \infty} x_n$ either does not exist or satisfies $\lim_{n \to \infty} x_n \neq 0$. Suppose, for the sake of contradiction, that the series $\sum_{n=1}^\infty x_n$ converges. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|Necessary Condition for Series Convergence]] (since the partial sums $s_n = \sum_{k=1}^n x_k$ converge to a finite sum $s$, forcing $\lim_{n \to \infty} x_n = \lim_{n \to \infty} (s_n - s_{n-1}) = s - s = 0$), the convergence of $\sum_{n=1}^\infty x_n$ requires that
$$
\begin{gather}
\lim_{n \to \infty} x_n = 0 \tag{6}
\end{gather}
$$
Step 6 directly contradicts the hypothesis that $\lim_{n \to \infty} x_n \neq 0$ (or does not exist). Therefore, the series $\sum_{n=1}^\infty x_n$ must diverge.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
