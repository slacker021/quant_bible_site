---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-bernoulli-s-inequality/","dg-note-properties":{}}
---

Let $x \in \mathbb{R}$ satisfy $x > -1$, and consider the inequality
$$
\begin{gather}
(1 + x)^n \ge 1 + nx \tag{1}
\end{gather}
$$
for $n \in \mathbb{N}$. Beginning with the base case $n = 1$, evaluating both sides of step 1 yields
$$
\begin{gather}
(1 + x)^1 = 1 + x \quad \text{and} \quad 1 + (1)x = 1 + x \tag{2}
\end{gather}
$$

Because both sides are identical, equality holds for $n = 1$, verifying the base case.

Now assume as the inductive hypothesis that step 1 holds for an arbitrary natural number $k \in \mathbb{N}$:
$$
\begin{gather}
(1 + x)^k \ge 1 + kx \tag{3}
\end{gather}
$$
It must be demonstrated that the inequality holds for $k + 1$:
$$
\begin{gather}
(1 + x)^{k+1} \ge 1 + (k + 1)x \tag{4}
\end{gather}
$$

Because $x > -1$, the order axioms of $\mathbb{R}$ dictate that $1 + x > 0$. Multiplying both sides of step 3 by the strictly positive quantity $(1 + x)$ preserves the direction of the inequality:
$$
\begin{gather}
(1 + x)^{k+1} = (1 + x)^k (1 + x) \ge (1 + kx)(1 + x) \tag{5}
\end{gather}
$$

Expanding the right-hand side of step 5 by the distributive law gives
$$
\begin{gather}
(1 + x)^{k+1} \ge 1 + x + kx + kx^2 = 1 + (k + 1)x + kx^2 \tag{6}
\end{gather}
$$

Because $k \in \mathbb{N}$ satisfies $k \ge 1 > 0$ and the square of any real number satisfies $x^2 \ge 0$, the product term is non-negative:
$$
\begin{gather}
k x^2 \ge 0 \implies 1 + (k + 1)x + kx^2 \ge 1 + (k + 1)x \tag{7}
\end{gather}
$$
By transitivity of the order relation across step 6 and step 7,
$$
\begin{gather}
(1 + x)^{k+1} \ge 1 + (k + 1)x \tag{8}
\end{gather}
$$
By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|Principle of Induction]], Bernoulli's Inequality holds for all $n \in \mathbb{N}$.

Finally, to determine when equality holds, observe that if $x = 0$, then $(1 + 0)^n = 1 = 1 + n(0)$ for all $n \in \mathbb{N}$, and if $n = 1$, equality holds by step 2. Conversely, if $x \ne 0$, then $x^2 > 0$, so in step 7 the strict inequality $1 + (1 + 1)x + 1 \cdot x^2 > 1 + 2x$ holds at $n = 2$, and multiplying by $(1 + x) > 0$ at each subsequent inductive step preserves the strict inequality $(1 + x)^n > 1 + nx$ for all $n \ge 2$. Thus, equality holds if and only if $n = 1$ or $x = 0$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$