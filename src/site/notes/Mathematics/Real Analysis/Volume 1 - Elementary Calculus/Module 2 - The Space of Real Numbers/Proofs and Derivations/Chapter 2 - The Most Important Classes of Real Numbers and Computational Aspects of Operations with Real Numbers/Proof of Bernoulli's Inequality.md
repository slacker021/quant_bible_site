---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-bernoulli-s-inequality/","dg-note-properties":{}}
---

Let $n \in \mathbb{N}$ and $x > -1$ such that 
$$
(1 + x)^{n} \ge 1 + nx \tag{1}
$$
Beginning with the base case, where $n = 1$, the following evaluating both sides of the expression yields:  $$
\begin{gather}
(1 + x)^1 = 1 + x  \\
1 + (1)x = 1 + x  \tag{2}
\end{gather}
$$Because both sides are identical, equality holds for $n = 1$. Thus, the base case is verified.

Now, assume the inequality holds for an arbitrary natural number $k \in \mathbb{N}$:  
$$(1 + x)^k \ge 1 + kx \tag{4}$$
It must be shown that the inequality holds for $k + 1$:  
$$(1 + x)^{k+1} \ge 1 + (k + 1)x \tag{5}$$

Since $x > -1$, it follows from the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|ordering axioms]] that $1 + x > 0$. Multiplying both sides of the induction hypothesis, as seen in the fourth step, by the positive quantity $(1 + x)$ preserves the inequality direction:  
$$(1 + x)^k (1 + x) \ge (1 + kx)(1 + x) \tag{6}$$
Expanding both expressions gives:
$$
\begin{gather}
(1 + x)^{k+1} \ge 1 + x + kx + kx^2  \\
(1 + x)^{k+1} \ge 1 + (k + 1)x + kx^2 \tag{7}
\end{gather}
$$
Because $k \in \mathbb{N}$ implies $k \ge 1$, and the square of any real number satisfies $x^2 \ge 0$, the product term satisfies:
$$kx^2 \ge 0 \tag{8}$$
Dropping the non-negative term $kx^2$ from the right-hand side of step 8 yields:
$$1 + (k + 1)x + kx^2 \ge 1 + (k + 1)x \tag{9}$$
By the transitivity of the order relation, combining the results from both steps 7 and 9 establishes that
$$(1 + x)^{k+1} \ge 1 + (k + 1)x \tag{10}$$
This completes the inductive step. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|induction]], the inequality holds for all $n \in \mathbb{N}$.

In step 9, the strict inequality occurs if and only if $kx^2 > 0$. Since $k \ge 1$, this condition reduces to $x^2 > 0$, which holds for all $x \ne 0$. Hence, for $n > 1$ and $x \ne 0$, the strict inequality holds:  
$$(1 + x)^n > 1 + nx \tag{11}$$
Consequently, equality holds if and only if $n = 1$ or $x = 0$.
$$\textbf{Q.E.D}$$