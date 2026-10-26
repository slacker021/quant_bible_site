---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-binomial-theorem/","dg-note-properties":{}}
---

# Prelude: Pascal's Rule
Before proving the Binomial Theorem by induction, it is necessary to establish *Pascal's Rule*, a fundamental combinatorial identity governing binomial coefficients. For any non-negative integers $n, k \in \mathbb{N} \cup \{0\}$ with $0 \le k \le n$, the binomial coefficient is defined by
$$
\begin{gather}
\binom{n}{k} := \frac{n!}{k!(n - k)!}, \quad \text{where } 0! := 1 \text{ and } m! := \prod_{i=1}^m i \text{ for } m \in \mathbb{N}. \tag{1}
\end{gather}
$$
For any $n, k \in \mathbb{N}$ satisfying $1 \le k \le n$, expanding the sum $\binom{n}{k} + \binom{n}{k-1}$ via step 1 yields
$$
\begin{gather}
\binom{n}{k} + \binom{n}{k-1} = \frac{n!}{k!(n-k)!} + \frac{n!}{(k-1)!(n-k+1)!} \tag{2}
\end{gather}
$$
Using the factorial recurrence relations $k! = k \cdot (k - 1)!$ and $(n - k + 1)! = (n - k + 1)(n - k)!$, both fractions in step 2 can be placed over the common denominator $k!(n - k + 1)!$ by multiplying the first fraction by $\frac{n - k + 1}{n - k + 1}$ and the second fraction by $\frac{k}{k}$:
$$
\begin{gather}
\frac{n!(n-k+1)}{k!(n-k+1)!} + \frac{n! \cdot k}{k!(n-k+1)!} = \frac{n!(n - k + 1 + k)}{k!(n - k + 1)!} \tag{3}
\end{gather}
$$
Simplifying the numerator $n!(n + 1) = (n + 1)!$ in step 3 produces Pascal's Rule:
$$
\begin{gather}
\binom{n}{k} + \binom{n}{k-1} = \frac{n!(n+1)}{k!(n + 1 - k)!} = \frac{(n+1)!}{k!((n + 1) - k)!} = \binom{n+1}{k} \tag{4}
\end{gather}
$$

---
# Binomial Theorem
Let $x, y \in \mathbb{R}$ be arbitrary real numbers, and proceed by mathematical induction on the exponent $n \in \mathbb{N} \cup \{0\}$.

### Base Case
For $n = 0$, $(x + y)^0 = 1 = \binom{0}{0} x^0 y^0$. For $n = 1$, the left-hand side of the identity evaluates to
$$
\begin{gather}
(x + y)^1 = x + y \tag{5}
\end{gather}
$$
Meanwhile, expanding the summation on the right-hand side for $n = 1$ gives
$$
\begin{gather}
\sum_{k=0}^1 \binom{1}{k} x^{1-k} y^k = \binom{1}{0} x^1 y^0 + \binom{1}{1} x^0 y^1 = 1 \cdot x \cdot 1 + 1 \cdot 1 \cdot y = x + y \tag{6}
\end{gather}
$$
Because step 5 and step 6 are equal, the base case holds.

### Inductive Step
Assume as the inductive hypothesis that the identity holds for a fixed natural number $n = m \in \mathbb{N}$:
$$
\begin{gather}
(x + y)^m = \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k \tag{7}
\end{gather}
$$
To evaluate $(x + y)^{m+1}$, factor out $(x + y)$ and substitute the inductive hypothesis from step 7:
$$
\begin{gather}
(x + y)^{m+1} = (x + y)(x + y)^m = (x + y) \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k \tag{8}
\end{gather}
$$
By the distributive axiom of $\mathbb{R}$, distributing $x$ and $y$ across the finite summation in step 8 yields
$$
\begin{gather}
(x + y)^{m+1} = x \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k + y \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k \\[2mm]
(x + y)^{m+1} = \sum_{k=0}^m \binom{m}{k} x^{m-k+1} y^k + \sum_{k=0}^m \binom{m}{k} x^{m-k} y^{k+1} \tag{9}
\end{gather}
$$
To align the powers of $x$ and $y$ in the two sums of step 9, re-index the second summation by setting $j := k + 1$ (so $k = j - 1$). As $k$ ranges from $0$ to $m$, the new index $j$ ranges from $1$ to $m + 1$:
$$
\begin{gather}
\sum_{k=0}^m \binom{m}{k} x^{m-k} y^{k+1} = \sum_{j=1}^{m+1} \binom{m}{j-1} x^{m-(j-1)} y^j = \sum_{j=1}^{m+1} \binom{m}{j-1} x^{m-j+1} y^j \tag{10}
\end{gather}
$$
Relabeling the dummy summation index $j$ back to $k$ in step 10 and substituting the result into step 9 produces
$$
\begin{gather}
(x + y)^{m+1} = \sum_{k=0}^m \binom{m}{k} x^{m-k+1} y^k + \sum_{k=1}^{m+1} \binom{m}{k-1} x^{m-k+1} y^k \tag{11}
\end{gather}
$$
Separating the $k = 0$ term from the first summation and the $k = m + 1$ term from the second summation allows the overlapping terms for $1 \le k \le m$ to be combined into a single sum:
$$
\begin{gather}
(x + y)^{m+1} = \binom{m}{0} x^{m+1} y^0 + \sum_{k=1}^m \left[ \binom{m}{k} + \binom{m}{k-1} \right] x^{m-k+1} y^k + \binom{m}{m} x^0 y^{m+1} \tag{12}
\end{gather}
$$
Applying Pascal's Rule from step 4 to the bracketed coefficient in step 12, and noting that $\binom{m}{0} = 1 = \binom{m+1}{0}$ and $\binom{m}{m} = 1 = \binom{m+1}{m+1}$, transforms step 12 into
$$
\begin{gather}
(x + y)^{m+1} = \binom{m+1}{0} x^{m+1} y^0 + \sum_{k=1}^m \binom{m+1}{k} x^{(m+1)-k} y^k + \binom{m+1}{m+1} x^0 y^{m+1} \tag{13}
\end{gather}
$$
Absorbing the boundary terms $k = 0$ and $k = m + 1$ back into the summation in step 13 yields
$$
\begin{gather}
(x + y)^{m+1} = \sum_{k=0}^{m+1} \binom{m+1}{k} x^{(m+1)-k} y^k \tag{14}
\end{gather}
$$
This completes the inductive step. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|Principle of Mathematical Induction]], the Binomial Theorem holds for all $n \in \mathbb{N} \cup \{0\}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
