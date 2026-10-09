---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-theorem-involving-odd-and-even-indexed-sequences/","dg-note-properties":{}}
---

Let $\varepsilon > 0$. Since $\lim_{ n \to \infty } x_{2n} = A$, there's an $N_{1} > 0$ such that if $n > N_{1}$, then 
$$
|x_{2n} - A| < \varepsilon \tag{1}
$$
Likewise, because $\lim_{ n \to \infty } x_{2n + 1} = A$, there's an $N_{2} > 0$ such that if $n > N_{2}$, then 
$$
|x_{2n+1} - A| < \varepsilon \tag{2} 
$$
Now, let $N = \text{max}\{2N_{1}, 2N_{2+1}\}$ and let $n > N$. Then either $x_{n} = x_{2k}$ for some $k > N_{1}$ or $x_{n} = x_{2k+1}$ for some $k > N_{2}$ and so in either case, 
$$
|a_{n} - A| < \varepsilon \tag{3}
$$
Therefore, $\lim_{ n \to \infty } x_{n} = A$ and $\{x_{n}  \}$ is convergent. 
$$
\textbf{Q.E.D}
$$
