---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-cauchy-criterion-for-sequences/","dg-note-properties":{}}
---

# Necessity (Convergent $\implies$ Cauchy)
Assume the sequence $\{x_n\}$ converges to a limit $A$ and let $\varepsilon > 0$. By definition, there's  an $N \in \mathbb{N}$ such that for all $n > N$, $\vert x_n - A \vert < \frac{\varepsilon}{2}$. Consider any two indices $n > N$ and $m > N$. By applying the Triangle Inequality through the intermediate point $A$, it's demonstrated that
$$
\begin{gather}
\vert x_n - x_m \vert = \vert x_n - A + A - x_m \vert \le \vert x_n - A \vert + \vert A - x_m \vert \\ 
\vert x_n - x_m \vert < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon\tag{1}
\end{gather}
$$
Thus, the sequence is Cauchy.

---
# Sufficiency (Cauchy $\implies$ Convergence)
Assume $\{x_n\}$ is a Cauchy sequence and let $\varepsilon = 1$. It follows that there's  an index $N$ such that for $m, n > N$, $\vert x_n - x_m \vert < 1$. Fixing $m = N+1$, it follows that $\vert x_n - x_{N+1} \vert < 1$ for all $n > N$. Thus, the tail is bounded by $\vert x_{N+1} \vert + 1$. Because the tail is bounded and there are only finitely many terms before it, the entire sequence is bounded.

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Bolzano-Weierstrass Lemma\|Bolzano-Weierstrass Lemma]], since $\{x_n\}$ is a bounded sequence in $\mathbb{R}$, it contains a convergent subsequence $\{x_{n_k}\}$ that converges to some limit $L$.

It is claimed that the entire sequence $\{x_n\}$ converges to $L$. Let $\varepsilon > 0$. Because the sequence is Cauchy, there's an index $N_1$ such that for all $m, n > N_1$, $\vert x_n - x_m \vert < \frac{\varepsilon}{2}$. Because the subsequence $\{x_{n_k}\}$ converges to $L$, there's a $K \in \mathbb{N}$ such that for all $k > K$, $\vert x_{n_k} - L \vert < \frac{\varepsilon}{2}$.

Let an index $k > K$ such that $n_k > N_1$. (This is always possible since $n_k \ge k$). Now, let $n > N_1$. The distance from $x_n$ to $L$ is calculated using the subsequence term $x_{n_k}$ as an anchor:  
$$\vert x_n - L \vert = \vert x_n - x_{n_k} + x_{n_k} - L \vert \le \vert x_n - x_{n_k} \vert + \vert x_{n_k} - L \vert \tag{2}$$
Since $n > N_1$ and $n_k > N_1$, the Cauchy property gives $\vert x_n - x_{n_k} \vert < \frac{\varepsilon}{2}$. By the subsequence convergence bound, $\vert x_{n_k} - L \vert < \frac{\varepsilon}{2}$.

Thus, 
$$\vert x_n - L \vert < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{3}$$
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
