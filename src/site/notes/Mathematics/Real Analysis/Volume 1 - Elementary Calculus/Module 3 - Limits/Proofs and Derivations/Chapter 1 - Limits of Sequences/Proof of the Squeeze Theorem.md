---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-squeeze-theorem/","dg-note-properties":{}}
---

Let $\{a_n\}$, $\{b_n\}$, and $\{x_n\}$ be sequences of real numbers satisfying $a_n \le x_n \le b_n$ for all $n > N_0$ (for some threshold index $N_0 \in \mathbb{N}$, or for all $n \in \mathbb{N}$), and assume that $\{a_n\}$ and $\{b_n\}$ converge to the common limit $\lim_{n \to \infty} a_n = \lim_{n \to \infty} b_n = x \in \mathbb{R}$.

Let $\varepsilon > 0$ be arbitrary. Because $\lim_{n \to \infty} a_{n} = x$, by the definition of sequence convergence there exists an index $N_{1} \in \mathbb{N}$ such that for all $n > N_{1}$:
$$
\begin{gather}
|a_{n} - x| < \varepsilon \implies x - \varepsilon < a_{n} < x + \varepsilon \tag{1}
\end{gather}
$$
Similarly, because $\lim_{n \to \infty} b_{n} = x$, there exists an index $N_{2} \in \mathbb{N}$ such that for all $n > N_{2}$:
$$
\begin{gather}
|b_{n} - x| < \varepsilon \implies x - \varepsilon < b_{n} < x + \varepsilon \tag{2}
\end{gather}
$$
Define the threshold index $N := \max(N_0, N_{1}, N_{2}) \in \mathbb{N}$. For every index $n > N$, the ordering hypothesis $a_n \le x_n \le b_n$ and the bounds from steps 1 and 2 hold simultaneously:
$$
\begin{gather}
x - \varepsilon < a_{n} \le x_{n} \le b_{n} < x + \varepsilon \implies x - \varepsilon < x_n < x + \varepsilon \iff |x_{n} - x| < \varepsilon \tag{3}
\end{gather}
$$
Because $\varepsilon > 0$ is arbitrary, $\{x_{n}\}$ converges and $\lim_{n \to \infty} x_{n} = x$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
