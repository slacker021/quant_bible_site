---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/derivation-of-faulhaber-s-formulae/","dg-note-properties":{}}
---

Let $k \in \mathbb{N} \cup \{0\}$ be a non-negative integer, and let $S_{k}(n) := \sum_{i = 1}^n i^k$ denote the sum of the $k$-th powers of the first $n$ positive integers.

# General Derivation
By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Binomial Theorem\|Binomial Theorem]], the expression $(x + 1)^{k+1}$ expands for any $x \in \mathbb{R}$ as
$$
\begin{gather}
(x + 1)^{k+1} = \sum_{j=0}^{k+1} \binom{k+1}{j} x^j = x^{k+1} + \sum_{j=0}^{k} \binom{k+1}{j} x^j \tag{1}
\end{gather}
$$
Subtracting $x^{k+1}$ from both sides of step 1 yields the algebraic identity
$$
\begin{gather}
(x + 1)^{k+1} - x^{k+1} = \sum_{j=0}^{k} \binom{k+1}{j} x^j \tag{2}
\end{gather}
$$
Summing both sides of step 2 over the integer index $x$ from $1$ to $n$ gives
$$
\begin{gather}
\sum_{x=1}^n \left((x + 1)^{k+1} - x^{k+1}\right) = \sum_{x=1}^n \left( \sum_{j=0}^k \binom{k+1}{j} x^j \right) \tag{3}
\end{gather}
$$
The left-hand side of step 3 is a finite telescoping sum in which all intermediate terms cancel pairwise:
$$
\begin{gather}
(2^{k+1} - 1^{k+1}) + (3^{k+1} - 2^{k+1}) + \dots + \left((n + 1)^{k+1} - n^{k+1}\right) = (n + 1)^{k+1} - 1 \tag{4}
\end{gather}
$$
Meanwhile, interchanging the order of the two finite summations on the right-hand side of step 3 yields
$$
\begin{gather}
\sum_{j = 0}^k \binom{k+1}{j} \left( \sum_{x=1}^n x^j \right) = \sum_{j = 0}^k \binom{k+1}{j} S_{j}(n) \tag{5}
\end{gather}
$$
Equating step 4 and step 5 produces Pascal's identity for power sums:
$$
\begin{gather}
(n + 1)^{k+1} - 1 = \sum_{j = 0}^k \binom{k+1}{j} S_{j}(n) \tag{6}
\end{gather}
$$
Separating the $j = k$ term from the summation in step 6 and noting that $\binom{k+1}{k} = k + 1$ gives
$$
\begin{gather}
(n + 1)^{k+1} - 1 = (k + 1) S_{k}(n) + \sum_{j = 0}^{k-1} \binom{k+1}{j} S_{j}(n) \tag{7}
\end{gather}
$$
Dividing both sides of step 7 by $k + 1$ isolates $S_k(n)$ recursively in terms of $S_0(n), S_1(n), \dots, S_{k-1}(n)$:
$$
\begin{gather}
S_{k}(n) = \frac{1}{k + 1} \left[ (n + 1)^{k+1} - 1 - \sum_{j = 0}^{k-1} \binom{k+1}{j} S_{j}(n) \right] \tag{8}
\end{gather}
$$

---
# Inductive Proof of Polynomial Degree
To prove that $S_k(n)$ is a polynomial in $n$ of degree $k + 1$ with leading coefficient $\frac{1}{k + 1}$, proceed by strong induction on $k \in \mathbb{N} \cup \{0\}$:
- **Base Case ($k = 0$):** Evaluating $S_0(n)$ directly gives $S_0(n) = \sum_{i=1}^n i^0 = \sum_{i=1}^n 1 = n$, which is a polynomial in $n$ of degree $0 + 1 = 1$ with leading coefficient $\frac{1}{0 + 1} = 1$.
- **Inductive Step:** Fix $k \ge 1$, and assume as the strong inductive hypothesis that for every integer $j \in \{0, 1, \dots, k - 1\}$, the power sum $S_j(n)$ is a polynomial in $n$ of degree $j + 1$. Then the finite linear combination $\sum_{j=0}^{k-1} \binom{k+1}{j} S_j(n)$ in step 8 is a polynomial in $n$ of degree at most $(k - 1) + 1 = k$. Meanwhile, expanding $(n + 1)^{k+1} - 1$ via the Binomial Theorem yields
$$
\begin{gather}
(n + 1)^{k+1} - 1 = n^{k+1} + (k + 1)n^k + \dots + (k + 1)n \tag{9}
\end{gather}
$$
which is a polynomial in $n$ of degree $k + 1$ with leading term $n^{k+1}$. Subtracting a polynomial of degree at most $k$ from $(n + 1)^{k+1} - 1$ leaves the leading term $n^{k+1}$ unaltered. Upon dividing by $k + 1$ in step 8, it follows that $S_k(n)$ is a polynomial in $n$ of degree $k + 1$ with leading coefficient $a_{k+1} = \frac{1}{k + 1}$.

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|Principle of Mathematical Induction]], the theorem holds for all $k \in \mathbb{N} \cup \{0\}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
