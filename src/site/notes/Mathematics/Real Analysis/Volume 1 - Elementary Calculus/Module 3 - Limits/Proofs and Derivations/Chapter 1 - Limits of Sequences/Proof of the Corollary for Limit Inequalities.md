---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-corollary-for-limit-inequalities/","dg-note-properties":{}}
---

Let $\{x_n\}$ and $\{y_n\}$ be two convergent sequences of real numbers with $\lim_{n \to \infty} x_n = A$ and $\lim_{n \to \infty} y_n = B$, and let $b \in \mathbb{R}$ be a real constant.

# Corollary 1
Assume there exists an index $N \in \mathbb{N}$ such that $x_n > y_n$ for all $n > N$. By definition of the order relation on $\mathbb{R}$, the strict inequality $x_n > y_n$ implies the non-strict inequality
$$
\begin{gather}
x_n \ge y_n \quad \forall n > N \tag{1}
\end{gather}
$$
By Corollary 2 established immediately below, step 1 implies $A \ge B$.

---
# Corollary 2
Assume there exists an index $N \in \mathbb{N}$ such that $x_n \ge y_n$ for all $n > N$. Suppose, for the sake of contradiction, that $A < B$. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Inequalities Involving Limits\|Theorem 1 of Inequalities Involving Limits]], the strict inequality $A < B$ guarantees the existence of an index $N^* \in \mathbb{N}$ such that
$$
\begin{gather}
x_n < y_n \quad \forall n > N^* \tag{2}
\end{gather}
$$
Define the index $M := \max(N, N^*) + 1 \in \mathbb{N}$. Because $M > N$, the initial hypothesis requires $x_M \ge y_M$; simultaneously, because $M > N^*$, step 2 requires $x_M < y_M$:
$$
\begin{gather}
(x_M \ge y_M) \wedge (x_M < y_M) \tag{3}
\end{gather}
$$
Step 3 violates the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Order Axioms\|Law of Trichotomy]]. Therefore, the assumption $A < B$ is false, and trichotomy forces $A \ge B$.

---
# Corollary 3
Assume there exists an index $N \in \mathbb{N}$ such that $x_n > b$ for all $n > N$. Define the constant sequence $\{y_n\}$ by setting $y_n := b$ for all $n \in \mathbb{N}$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|basic properties of limits]], $\lim_{n \to \infty} y_n = b$. Applying Corollary 1 to $\{x_n\}$ and $\{y_n\}$ yields $A \ge b$.

---
# Corollary 4
Assume there exists an index $N \in \mathbb{N}$ such that $x_n \ge b$ for all $n > N$. Defining the constant sequence $y_n := b$ for all $n \in \mathbb{N}$ (so that $\lim_{n \to \infty} y_n = b$) and applying Corollary 2 to $\{x_n\}$ and $\{y_n\}$ directly yields $A \ge b$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
