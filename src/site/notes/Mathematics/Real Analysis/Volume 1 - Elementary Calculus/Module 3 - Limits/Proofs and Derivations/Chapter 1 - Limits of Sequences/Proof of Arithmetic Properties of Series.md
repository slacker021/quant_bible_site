---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-arithmetic-properties-of-series/","dg-note-properties":{}}
---

# Proposition 1

Let $S = \sum_{n=k}^\infty x_{n}$ and $S_{c} = s\sum_{n=k}^\infty cx_{n}$. Since $S$ converges, the partial sums
$$
S_{N} = \sum_{n=k}^N x_{n} \tag{1}
$$
converges to $A$ as $N \rightarrow \infty$. The partial sums of $S_{c}$ are given by 
$$
S_{c,N} = \sum_{n=k}^N c x_{n} = c \cdot \sum_{n=k}^N x_{n} = c S_{N} \tag{2}
$$
Taking the limit as $N \rightarrow \infty$:
$$
\lim_{ N \to \infty } S_{c,N} = \lim_{ n \to \infty } c S_{N} = c \lim_{ N \to \infty } S_{N} = c A \tag{3}
$$
Thus, $\sum_{n=k}^\infty$ converges to $c A$. 

---
# Proposition 2
Let $S_{x} = \sum_{n=k}^\infty x_{n}$ and $S_{y} = \sum_{n=k}^\infty y_{n}$, with partial sums $S_{x,N}$ and $S_{y,n}$ converging to $A$ and $B$ respectively. The partial sums of $\sum_{n=k}^\infty (x_{n} + y_{n})$ are given by 
$$
S_{x + y, N} = \sum_{n=k}^N (x_{n} + y_{n}) = S_{x} = \sum_{n=k}^N x_{n} + S_{x} = \sum_{n=k}^N y_{n} = S_{x,N} + S_{y,N} \tag{4}
$$
Taking the limit as $N \rightarrow \infty$: 
$$
\lim_{ N \to \infty } S_{x + y, N} = \lim_{ N \to \infty } (S_{x,N} + S_{y,N}) = \lim_{ N \to \infty }  S_{x,N} + \lim_{ N \to \infty } S_{y,N} = A + B \tag{5}
$$
Thus, $\sum_{n=k}^\infty (x_{n} + y_{n})$ converges to $A + B$. 
$$
\textbf{Q.E.D}
$$
