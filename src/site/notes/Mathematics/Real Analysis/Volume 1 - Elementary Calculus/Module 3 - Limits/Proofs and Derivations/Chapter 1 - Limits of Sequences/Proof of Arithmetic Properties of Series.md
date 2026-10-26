---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-arithmetic-properties-of-series/","dg-note-properties":{}}
---

Let $\sum_{n=k}^\infty x_n$ and $\sum_{n=k}^\infty y_n$ be two convergent series with sums $A = \sum_{n=k}^\infty x_n$ and $B = \sum_{n=k}^\infty y_n$, and let $c \in \mathbb{R}$ be a real constant.

# Proposition 1
Because the series $\sum_{n=k}^\infty x_n$ converges to $A$, its sequence of partial sums
$$
\begin{gather}
S_{N} := \sum_{n=k}^N x_{n} \tag{1}
\end{gather}
$$
converges to $A$ as $N \rightarrow \infty$. By the distributive axiom of $\mathbb{R}$, the $N$-th partial sum $S_{c,N}$ of the scaled series $\sum_{n=k}^\infty (c x_n)$ satisfies
$$
\begin{gather}
S_{c,N} := \sum_{n=k}^N (c x_{n}) = c \sum_{n=k}^N x_{n} = c S_{N} \tag{2}
\end{gather}
$$
Passing to the limit as $N \rightarrow \infty$ and applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|scalar multiplication property of sequence limits]] yields
$$
\begin{gather}
\lim_{N \to \infty} S_{c,N} = \lim_{N \to \infty} (c S_{N}) = c \lim_{N \to \infty} S_{N} = c A \tag{3}
\end{gather}
$$
Thus, the series $\sum_{n=k}^\infty (c x_n)$ converges and $\sum_{n=k}^\infty (c x_n) = c \sum_{n=k}^\infty x_n$.

---
# Proposition 2
Let $S_{x,N} := \sum_{n=k}^N x_n$ and $S_{y,N} := \sum_{n=k}^N y_n$ denote the $N$-th partial sums of $\sum_{n=k}^\infty x_n$ and $\sum_{n=k}^\infty y_n$, which converge to $A$ and $B$, respectively, as $N \to \infty$. By the commutativity and associativity of finite addition in $\mathbb{R}$, the $N$-th partial sum $S_{x \pm y, N}$ of the series $\sum_{n=k}^\infty (x_n \pm y_n)$ is given by
$$
\begin{gather}
S_{x \pm y, N} := \sum_{n=k}^N (x_{n} \pm y_{n}) = \sum_{n=k}^N x_{n} \pm \sum_{n=k}^N y_{n} = S_{x,N} \pm S_{y,N} \tag{4}
\end{gather}
$$
Taking the limit as $N \rightarrow \infty$ and applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|linearity of sequence limits]] yields
$$
\begin{gather}
\lim_{N \to \infty} S_{x \pm y, N} = \lim_{N \to \infty} (S_{x,N} \pm S_{y,N}) = \lim_{N \to \infty} S_{x,N} \pm \lim_{N \to \infty} S_{y,N} = A \pm B \tag{5}
\end{gather}
$$
Thus, $\sum_{n=k}^\infty (x_{n} \pm y_{n})$ converges to $A \pm B = \sum_{n=k}^\infty x_n \pm \sum_{n=k}^\infty y_n$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
