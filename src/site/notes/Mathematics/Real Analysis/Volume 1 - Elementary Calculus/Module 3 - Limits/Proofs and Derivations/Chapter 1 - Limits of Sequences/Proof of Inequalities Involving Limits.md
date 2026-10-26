---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-inequalities-involving-limits/","dg-note-properties":{}}
---

# Theorem 1
Let $\{x_n\}$ and $\{y_n\}$ be two convergent sequences of real numbers with $\lim_{n \to \infty} x_n = A$ and $\lim_{n \to \infty} y_n = B$, such that $A < B$. Define the positive quantity $\varepsilon := \frac{B - A}{2} > 0$.

By the definition of convergence, there exists an index $N_1 \in \mathbb{N}$ such that $|x_n - A| < \varepsilon$ for all $n > N_1$, which is equivalent to $A - \varepsilon < x_n < A + \varepsilon$. Similarly, there exists an index $N_2 \in \mathbb{N}$ such that $|y_n - B| < \varepsilon$ for all $n > N_2$, which is equivalent to $B - \varepsilon < y_n < B + \varepsilon$.

Set $N := \max(N_1, N_2) \in \mathbb{N}$. For all $n > N$, both bounds hold simultaneously:
$$
\begin{gather}
x_n < A + \varepsilon = A + \frac{B - A}{2} = \frac{A + B}{2} \\[2mm]
y_n > B - \varepsilon = B - \frac{B - A}{2} = \frac{A + B}{2} \tag{1}
\end{gather}
$$
By the transitivity of strict inequalities, step 1 implies that for all $n > N$:
$$
\begin{gather}
x_n < \frac{A + B}{2} < y_n \implies x_n < y_n \tag{2}
\end{gather}
$$

---
# Theorem 2
Suppose the sequences $\{x_n\}$, $\{y_n\}$, and $\{z_n\}$ satisfy $x_n \le y_n \le z_n$ for all $n > N_0$ for some threshold index $N_0 \in \mathbb{N}$, and assume that $\lim_{n \to \infty} x_n = \lim_{n \to \infty} z_n = L$.

Let $\varepsilon > 0$ be arbitrary. Because $\lim_{n \to \infty} x_n = L$, there exists an index $N_1 \in \mathbb{N}$ such that $L - \varepsilon < x_n < L + \varepsilon$ for all $n > N_1$. Similarly, because $\lim_{n \to \infty} z_n = L$, there exists an index $N_2 \in \mathbb{N}$ such that $L - \varepsilon < z_n < L + \varepsilon$ for all $n > N_2$.

Set $N := \max(N_0, N_1, N_2) \in \mathbb{N}$. For all $n > N$, combining the ordering hypothesis with the convergence bounds yields
$$
\begin{gather}
L - \varepsilon < x_n \le y_n \le z_n < L + \varepsilon \tag{3}
\end{gather}
$$
Extracting the outer and middle terms from step 3 gives
$$
\begin{gather}
L - \varepsilon < y_n < L + \varepsilon \iff |y_n - L| < \varepsilon \quad \forall n > N \tag{4}
\end{gather}
$$
Because $\varepsilon > 0$ is arbitrary, the sequence $\{y_n\}$ converges to $L$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
