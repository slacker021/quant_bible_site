---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-bounds-in-the-natural-numbers-and-integers/","dg-note-properties":{}}
---

# Proposition 1
Let $E \subset \mathbb{N}$ be a nonempty subset of the natural numbers that is bounded above in $\mathbb{R}$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|Least Upper Bound Principle]], $E$ possesses a unique supremum $s := \sup E \in \mathbb{R}$. 

Because $s$ is the *least* upper bound of $E$, the smaller quantity $s - 1 < s$ cannot be an upper bound for $E$. Consequently, there exists at least one element $n \in E$ satisfying
$$
\begin{gather}
s - 1 < n \le s \tag{1}
\end{gather}
$$

Adding $1$ to the left-hand inequality of step 1 gives $s < n + 1$. If there existed any element $m \in E$ strictly greater than $n$, then [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Proposition 4 of the Properties of Natural Numbers]] would require $m \ge n + 1 > s$, contradicting the fact that $s$ is an upper bound for $E$. Thus, $m \le n$ for all $m \in E$, confirming that $n = \max E$.

---
# Proposition 2
Suppose, for the sake of contradiction, that $\mathbb{N}$ were bounded above in $\mathbb{R}$. Since $\mathbb{N} \subset \mathbb{N}$ is nonempty, Proposition 1 would guarantee the existence of a maximal natural number $n = \max \mathbb{N}$. However, because $\mathbb{N}$ is an inductive set, $n + 1 \in \mathbb{N}$ and $n + 1 > n$, contradicting the maximality of $n$. Therefore, $\mathbb{N}$ is not bounded above in $\mathbb{R}$.

---
# Proposition 3
First, observe that for any two integers $m, n \in \mathbb{Z}$, the implication $n < m \implies n + 1 \le m$ holds: indeed, $n < m \iff m - n > 0$, and since $\mathbb{Z}$ is closed under subtraction ([[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Integer Operations Yield Integers\|Algebraic Closure of the Integers]]), the positive integer $m - n$ must belong to $\mathbb{N}$, which satisfies $m - n \ge 1 \iff n + 1 \le m$.

Now let $E \subset \mathbb{Z}$ be a nonempty subset of integers bounded above in $\mathbb{R}$, and let $s := \sup E \in \mathbb{R}$. Because $s - 1$ is not an upper bound for $E$, there exists an integer $n \in E$ such that
$$
\begin{gather}
s - 1 < n \le s \implies n + 1 > s \tag{2}
\end{gather}
$$

Any integer $m \in E$ satisfies $m \le s < n + 1$; by the discrete spacing of $\mathbb{Z}$ established above, $m < n + 1$ implies $m \le n$. Thus, $n = \max E$.

---
# Proposition 4
Let $E \subset \mathbb{Z}$ be a nonempty subset of integers that is bounded below in $\mathbb{R}$ by some lower bound $b \in \mathbb{R}$ ($b \le x$ for all $x \in E$). Consider the reflected set of additive inverses:
$$
\begin{gather}
-E := \{-x \mid x \in E\} \subset \mathbb{Z} \tag{3}
\end{gather}
$$

Because $E$ is nonempty, $-E$ is nonempty, and because $b \le x$ for all $x \in E$, the inequality $-x \le -b$ holds for all $-x \in -E$. Thus, $-E$ is a nonempty subset of $\mathbb{Z}$ bounded above by $-b$. By Proposition 3, $-E$ possesses a maximal element $m^* = \max(-E) \in -E$. Setting $n^* := -m^* \in E$, shows that
$$
\begin{gather}
\forall x \in E \ (-x \le m^* = -n^*) \implies \forall x \in E \ (n^* \le x) \tag{4}
\end{gather}
$$

Therefore, $n^* = \min E$ is the minimal element of $E$.

---
# Proposition 5
Because $\mathbb{N} \subset \mathbb{Z}$ and $\mathbb{N}$ is not bounded above in $\mathbb{R}$ (Proposition 2), the superset $\mathbb{Z}$ cannot be bounded above in $\mathbb{R}$. Similarly, if $\mathbb{Z}$ were bounded below in $\mathbb{R}$, then Proposition 4 would guarantee a minimal integer $n_{\min} = \min \mathbb{Z}$; however, $n_{\min} - 1 \in \mathbb{Z}$ satisfies $n_{\min} - 1 < n_{\min}$, a contradiction. Thus, $\mathbb{Z}$ is unbounded both above and below in $\mathbb{R}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$