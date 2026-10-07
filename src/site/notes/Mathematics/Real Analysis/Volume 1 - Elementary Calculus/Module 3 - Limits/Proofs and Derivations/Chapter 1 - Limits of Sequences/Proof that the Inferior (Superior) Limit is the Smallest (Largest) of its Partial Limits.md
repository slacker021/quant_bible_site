---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-that-the-inferior-superior-limit-is-the-smallest-largest-of-its-partial-limits/","dg-note-properties":{}}
---

# Proposition 1
Let $\{x_n\}$ be an arbitrary sequence of real numbers. Define the sequence of suprema as $s_n = \sup_{k \ge n} x_k$ and the sequence of infima as $i_n = \inf_{k \ge n} x_k$. The superior limit is defined as $L = \lim_{n \to \infty} s_n$, and the inferior limit is defined as $l = \lim_{n \to \infty} i_n$.

If $L$ is finite, then by the definition of the supremum, for any integer $N$ and any $\varepsilon > 0$, there exists an index $k \ge N$ such that $s_N - \varepsilon < x_k \le s_N$. Because $\lim_{N \to \infty} s_N = L$, one can sequentially choose indices $n_1 < n_2 < \dots < n_m < \dots$ such that the absolute difference $\vert x_{n_m} - L \vert < \frac{1}{m}$. The extracted subsequence $\{x_{n_m}\}$ converges exactly to $L$, proving $L$ is a partial limit.

If $L = +\infty$, the sequence $\{s_n\}$ is unbounded above, which mandates that the parent sequence $\{x_n\}$ is unbounded above. By the previously established lemma on subsequences and infinity, a subsequence tending to $+\infty$ can be extracted, making $+\infty$ a partial limit.

If $L = -\infty$, the sequence bounds $s_n \to -\infty$. Because $x_n \le s_n$ for all $n$, the constraint mechanism forces $x_n \to -\infty$. Every possible subsequence tends to $-\infty$, making it a partial limit.

---
# Proposition 2
By definition, there exists a subsequence $\{x_{n_k}\}$ that converges (or tends) to $M$.

By the fundamental definition of the supremum, every term in a sequence is strictly bounded by the supremum of its tail. Therefore, for every index $k$:  
$$x_{n_k} \le \sup_{j \ge n_k} x_j = s_{n_k} \tag{1}$$
Taking the limit as $k \to \infty$ on both sides of the inequality yields
$$\lim_{k \to \infty} x_{n_k} \le \lim_{k \to \infty} s_{n_k} \tag{2}$$
Because the subsequence converges to $M$, and the parent sequence of suprema converges to $L$ (which ensures any extracted subsequence of $s_n$ identically converges to $L$), substitution yields:  
$$M \le L \tag{3}$$
Because $M$ represents any arbitrary partial limit, and $M \le L$ is strictly true in all cases, $L$ is definitively the largest possible partial limit of the sequence. Symmetric calculus applies to the infimum to establish $l$ as the smallest partial limit. 
$$
\textbf{Q.E.D}
$$
