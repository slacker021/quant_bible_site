---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-theorem-involving-odd-and-even-indexed-sequences/","dg-note-properties":{}}
---

Let $\{x_n\}$ be a sequence of real numbers, and let $A \in \mathbb{R}$.

# Necessity
Assume the sequence $\{x_n\}$ converges to $A$, so $\lim_{n \to \infty} x_n = A$. Let $\varepsilon > 0$ be arbitrary. By the definition of convergence, there exists an index $N \in \mathbb{N}$ such that $|x_m - A| < \varepsilon$ for all $m > N$.

For every index $n > N$, because $n \in \mathbb{N}$ satisfies $n \ge 1$, the even index $m = 2n$ and the odd index $m = 2n + 1$ satisfy $2n + 1 > 2n \ge n + 1 > n > N$. Consequently, for all $n > N$:
$$
\begin{gather}
|x_{2n} - A| < \varepsilon \quad \text{and} \quad |x_{2n+1} - A| < \varepsilon \tag{1}
\end{gather}
$$
Thus, $\lim_{n \to \infty} x_{2n} = A$ and $\lim_{n \to \infty} x_{2n+1} = A$.

---
# Sufficiency
Conversely, assume that both $\lim_{n \to \infty} x_{2n} = A$ and $\lim_{n \to \infty} x_{2n+1} = A$. Let $\varepsilon > 0$ be arbitrary. Because $\lim_{n \to \infty} x_{2n} = A$, there exists an index $N_{1} \in \mathbb{N}$ such that for all $k > N_{1}$:
$$
\begin{gather}
|x_{2k} - A| < \varepsilon \tag{2}
\end{gather}
$$
Similarly, because $\lim_{n \to \infty} x_{2n + 1} = A$, there exists an index $N_{2} \in \mathbb{N}$ such that for all $k > N_{2}$:
$$
\begin{gather}
|x_{2k+1} - A| < \varepsilon \tag{3}
\end{gather}
$$
Define the threshold index $N := \max(2N_{1}, \, 2N_{2} + 1) \in \mathbb{N}$, and let $n > N$ be an arbitrary natural number. Every integer $n$ is either even or odd:
- **If $n$ is even:** Then $n = 2k$ for some $k \in \mathbb{N}$. Because $2k = n > N \ge 2N_1$, dividing by $2$ yields $k > N_1$, so step 2 guarantees $|x_n - A| = |x_{2k} - A| < \varepsilon$.
- **If $n$ is odd:** Then $n = 2k + 1$ for some $k \in \mathbb{N} \cup \{0\}$. Because $2k + 1 = n > N \ge 2N_2 + 1$, subtracting $1$ and dividing by $2$ yields $k > N_2$, so step 3 guarantees $|x_n - A| = |x_{2k+1} - A| < \varepsilon$.

In either case, for all $n > N$:
$$
\begin{gather}
|x_{n} - A| < \varepsilon \tag{4}
\end{gather}
$$
Therefore, $\{x_{n}\}$ is convergent and $\lim_{n \to \infty} x_{n} = A$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
