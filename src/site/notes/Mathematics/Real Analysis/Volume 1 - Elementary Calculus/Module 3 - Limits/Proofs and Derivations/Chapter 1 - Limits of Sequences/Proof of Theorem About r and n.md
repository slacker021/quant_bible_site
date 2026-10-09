---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-theorem-about-r-and-n/","dg-note-properties":{}}
---

# Case 1
### Sub-Case 1
For $0 < r < 1$, the sequence $\{ r_{n} \}$ is strictly decreasing and bounded below by $0$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Monotone Convergence]] principle, it converges to some limit $A$. For contradiction, a if $\lim_{ n \to \infty } r^n = A$, then $\lim_{ n \to \infty } r^{n+1} = rA$. However, the Monotone Convergence principle shows that if $\lim_{ n \to \infty } r^{n+1} = AA$, then $A = rA$. Solving $A = rA$ gives $A(1 - r) = 0$. Since $r \neq 1$, the value of $A$ must be zero. 

### Sub-Case 2
For $-1 < r < 0$, the sequence $\{ r_{n} \}$ oscillates between positive and negative values. The absolute value $|r^n| = |r|^n$ satisfies 
$$
0 < |r| < 1, \text{ so } |r^n| \rightarrow 0 \text{ as } n \rightarrow \infty \tag{1}
$$
Since the sequence has an upper bound of $1$ and its absolute value converges to zero, then $r^n$ converges to zero. 

### Sub-Case 3
If $r=0$, then $r^n = 0$ for all $n \ge 1$, and since all [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|terms are zero]], the limit is zero. 

---
# Case 2
For $r=1$, $r^n = 1$ for all $n$, so $\lim_{ n \to \infty } r^n = 1$. 

---
# Case 3
If $r > 1$, then $r^n$ grows without bound as $n$ gets arbitrarily larger. Thus, the sequence converges to $+\infty$. 

---
# Case 4
If $r < -1$, then $r^n$ oscillates between positive and negative values with increasing magnitude. This implies that the sequence doesn't approach any finite limit, and is therefore a divergent sequence. 

---
# Case 5
For $r = -1$, the sequence alternates between $-1$ and $1$, resulting in the sequence of 
$$
\{-1, 1, -1, 1 \dots  \} \tag{2}
$$
This sequence is divergent because it doesn't approach any single value. 
$$
\textbf{Q.E.D}
$$
