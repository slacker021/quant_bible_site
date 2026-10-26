---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-corollary-for-the-squeeze-theorem-of-limits/","dg-note-properties":{}}
---

Let $\{x_n\}$ be a sequence of real numbers.

# Necessity
Assume that $\lim_{n \to \infty} |x_n| = 0$. By the definition of the absolute value on $\mathbb{R}$, every term $x_n$ is bounded below by $-|x_n|$ and bounded above by $|x_n|$:
$$
\begin{gather}
-|x_{n}| \le x_{n} \le |x_{n}| \quad \forall n \in \mathbb{N} \tag{1}
\end{gather}
$$
By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|scalar multiplication property of limits]], multiplying the convergent sequence $\{|x_n|\}$ by $c = -1$ yields
$$
\begin{gather}
\lim_{n \to \infty} (-|x_{n}|) = -\lim_{n \to \infty} |x_{n}| = -0 = 0 \tag{2}
\end{gather}
$$
Consequently, both bounding sequences $\{-|x_n|\}$ and $\{|x_n|\}$ converge to the same limit $0$:
$$
\begin{gather}
\lim_{n \to \infty} (-|x_{n}|) = \lim_{n \to \infty} |x_{n}| = 0 \tag{3}
\end{gather}
$$
Applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Squeeze Theorem\|Squeeze Theorem]] to step 1 and step 3 establishes that $\lim_{n \to \infty} x_n = 0$.

---
# Sufficiency
Conversely, assume that $\lim_{n \to \infty} x_n = 0$, and let $\varepsilon > 0$ be arbitrary. By the definition of convergence, there exists an index $N \in \mathbb{N}$ such that $|x_n - 0| < \varepsilon$ for all $n > N$. Because $||x_n| - 0| = |x_n| = |x_n - 0|$, it follows that
$$
\begin{gather}
||x_n| - 0| = |x_n - 0| < \varepsilon \quad \forall n > N \tag{4}
\end{gather}
$$
Therefore, $\lim_{n \to \infty} |x_n| = 0$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
