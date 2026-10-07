---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-squeeze-theorem/","dg-note-properties":{}}
---

Let $\varepsilon > 0$. Because $\lim_{ n \to \infty } a_{n} = x$, there has to be a $N_{0} \in \mathbb{N}$ such that for all $n \ge N_{0}$, 
$$
|a_{n} - x| < \varepsilon \implies x - \varepsilon < a_{n} \tag{1}
$$
Since $\lim_{ n \to \infty } b_{n} = x$, there's a $N_{1}$ such that for all $n \ge N_{1}$, 
$$
|b_{n} - x| < \varepsilon \implies b_{n} < x + \varepsilon \tag{2}
$$
Choose $M = \text{max}(N_{0}, N_{1})$. Then, if $n \ge M$, then 
$$
x - \varepsilon < a_{n} \le x_{n} \le b_{n} < x - \varepsilon \implies |x_{n} - x| < \varepsilon \tag{3}
$$
Therefore, $\{ x_{n} \}$ is convergent and $\lim_{ n \to \infty } x_{n} = x$. 
$$
\textbf{Q.E.D}
$$
