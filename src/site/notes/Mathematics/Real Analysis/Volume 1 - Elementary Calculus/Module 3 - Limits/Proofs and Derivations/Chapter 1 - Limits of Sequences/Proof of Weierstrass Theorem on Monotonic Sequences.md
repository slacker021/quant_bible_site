---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-weierstrass-theorem-on-monotonic-sequences/","dg-note-properties":{}}
---

# Theorem 1
Let $\{x_n\}$ be a nondecreasing sequence, meaning $x_1 \le x_2 \le \dots \le x_n \le \dots$. Further assume the sequence is bounded above. By the completeness axiom of the real numbers, any non-empty set of real numbers that's bounded above possesses a definitive supremum (least upper bound). Now, let $S = \{x_n : n \in \mathbb{N}\}$ be the set of all terms in the sequence and $L = \sup(S)$.

Let $\varepsilon > 0$. Because $L$ is the least upper bound of $S$, the value $L - \varepsilon$ cannot be an upper bound. Consequently, there must exist at least one term in the sequence, denoted as $x_N$, such that
$$x_N > L - \varepsilon \tag{1}$$
Because the sequence is nondecreasing, it is guaranteed that for all $n > N$, $x_n \ge x_N$. By transitivity, this yields
$$x_n > L - \varepsilon \quad \text{for all } n > N \tag{2}$$
Simultaneously, $L$ being an upper bound for the entire sequence makes it such that it strictly holds that $x_n \le L < L + \varepsilon$ for all $n \in \mathbb{N}$.

Combining these inequalities provides
$$L - \varepsilon < x_n < L + \varepsilon \quad \text{for all } n > N \tag{3}$$

This is mathematically equivalent to $\vert x_n - L \vert < \varepsilon$ for all $n > N$. Thus, the sequence perfectly converges to its supremum $L$. 

---
# Theorem 2
Let $\{y_n\}$ be a nonincreasing sequence bounded below and $\{z_n\}$ be a new sequence such that $z_n = -y_n$. Because $\{y_n\}$ is nonincreasing and bounded below, $\{z_n\}$ is definitively nondecreasing and bounded above. By the previously proven theorem, $\{z_n\}$ converges to its supremum, $\sup(-y_n)$. By the arithmetic properties of limits, $\lim_{n \to \infty} y_n = -\lim_{n \to \infty} (-y_n)$. Thus, the sequence $\{y_n\}$ converges to $\inf(y_n)$. 
$$
\textbf{Q.E.D}
$$
