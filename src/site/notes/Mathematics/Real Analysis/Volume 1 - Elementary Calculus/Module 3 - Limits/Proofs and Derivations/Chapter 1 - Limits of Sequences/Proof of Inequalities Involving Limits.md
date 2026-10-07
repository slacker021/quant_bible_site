---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-inequalities-involving-limits/","dg-note-properties":{}}
---

# Theorem 1
Let $\varepsilon = \frac{B - A}{2}$. Since $A < B$, it follows that $\varepsilon > 0$. By the definition of convergence, there's an index $N_1$ such that $\vert x_n - A \vert < \varepsilon$ for all $n > N_1$. This is equivalent to $A - \varepsilon < x_n < A + \varepsilon$. Similarly, there's also an index $N_2$ such that $\vert y_n - B \vert < \varepsilon$ for all $n > N_2$. This is equivalent to $B - \varepsilon < y_n < B + \varepsilon$.

Let $N = \max(N_1, N_2)$. For all $n > N$, both bounds hold simultaneously. Thus, 
$$
\begin{gather}
x_n < A + \varepsilon = A + \frac{B - A}{2} = \frac{A + B}{2} \\
y_n > B - \varepsilon = B - \frac{B - A}{2} = \frac{A + B}{2} \tag{1}
\end{gather}$$

By transitivity, for all $n > N$, $x_n < \frac{A + B}{2} < y_n$, yielding $x_n < y_n$. 

---
# Theorem 2
**Proof:** Let $\varepsilon > 0$. Because $\lim_{n \to \infty} x_n = L$, there's an index $N_1$ such that $L - \varepsilon < x_n < L + \varepsilon$ for all $n > N_1$. Because $\lim_{n \to \infty} z_n = L$, there's an index $N_2$ such that $L - \varepsilon < z_n < L + \varepsilon$ for all $n > N_2$.

Let $N = \max(N_0, N_1, N_2)$. For all $n > N$, the premises guarantee that
$$L - \varepsilon < x_n \le y_n \le z_n < L + \varepsilon \tag{2}$$
Extracting the relevant terms provides $L - \varepsilon < y_n < L + \varepsilon$, which is mathematically equivalent to $\vert y_n - L \vert < \varepsilon$. Since this holds for any $\varepsilon > 0$, the sequence $\{y_n\}$ must converge to the definitive limit $L$. 
$$
\textbf{Q.E.D}
$$
