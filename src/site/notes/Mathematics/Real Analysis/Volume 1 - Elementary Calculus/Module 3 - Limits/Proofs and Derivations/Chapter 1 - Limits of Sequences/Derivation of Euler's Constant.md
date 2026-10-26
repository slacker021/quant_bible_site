---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/derivation-of-euler-s-constant/","dg-note-properties":{}}
---

To prove that the limit $\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$ exists as a finite real number, it suffices to demonstrate that the sequence $x_n := \left(1 + \frac{1}{n}\right)^n$ is strictly increasing and bounded above, which guarantees convergence by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]].

For $n = 1$, $x_1 = \left(1 + \frac{1}{1}\right)^1 = 2$. For any integer $n \ge 2$, applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Binomial Theorem\|Binomial Theorem]] to expand $x_n$ yields
$$
\begin{gather}
x_n = \sum_{k=0}^n \binom{n}{k} \left(\frac{1}{n}\right)^k = 1 + n\left(\frac{1}{n}\right) + \sum_{k=2}^n \frac{n(n-1)\cdots(n-k+1)}{k! \, n^k} \tag{1}
\end{gather}
$$
Dividing each of the $k$ factors in the numerator of the $k$-th summand by $n$ transforms step 1 into
$$
\begin{gather}
x_n = 2 + \sum_{k=2}^n \frac{1}{k!} \left(1 - \frac{1}{n}\right) \left(1 - \frac{2}{n}\right) \cdots \left(1 - \frac{k-1}{n}\right) \tag{2}
\end{gather}
$$
Similarly, expanding the subsequent term $x_{n+1}$ gives
$$
\begin{gather}
x_{n+1} = 2 + \sum_{k=2}^{n+1} \frac{1}{k!} \left(1 - \frac{1}{n+1}\right) \left(1 - \frac{2}{n+1}\right) \cdots \left(1 - \frac{k-1}{n+1}\right) \tag{3}
\end{gather}
$$
Comparing step 2 and step 3 term by term reveals that for each $k \in \{2, \dots, n\}$ and each $j \in \{1, \dots, k - 1\}$, the inequality $\frac{j}{n} > \frac{j}{n+1}$ implies
$$
\begin{gather}
0 < 1 - \frac{j}{n} < 1 - \frac{j}{n+1} \tag{4}
\end{gather}
$$
Furthermore, $x_{n+1}$ contains an additional strictly positive summand corresponding to $k = n + 1$ (and for $n = 1$, $x_1 = 2 < 2.25 = x_2$). Thus, $x_n < x_{n+1}$ for all $n \in \mathbb{N}$, proving that $\{x_n\}$ is strictly increasing.

To establish an upper bound for $\{x_n\}$, observe from step 2 that for $n \ge 2$, each factor $\left(1 - \frac{j}{n}\right)$ lies strictly between $0$ and $1$. Replacing each such factor with $1$ yields
$$
\begin{gather}
x_n < 2 + \sum_{k=2}^n \frac{1}{k!} \tag{5}
\end{gather}
$$
For every integer $k \ge 2$, the factorial $k! = 1 \cdot 2 \cdot 3 \cdots k$ is the product of $k - 1$ factors each greater than or equal to $2$, which ensures $k! \ge 2^{k-1}$ and hence $\frac{1}{k!} \le \frac{1}{2^{k-1}}$. Substituting this bound into step 5 gives
$$
\begin{gather}
x_n < 2 + \sum_{k=2}^n \frac{1}{2^{k-1}} \tag{6}
\end{gather}
$$
Evaluating the finite geometric sum in step 6 produces
$$
\begin{gather}
\sum_{k=2}^n \frac{1}{2^{k-1}} = \frac{1}{2} + \frac{1}{4} + \dots + \frac{1}{2^{n-1}} = 1 - \frac{1}{2^{n-1}} < 1 \tag{7}
\end{gather}
$$
Combining step 6 and step 7 (along with $x_1 = 2$) shows that for all $n \in \mathbb{N}$,
$$
\begin{gather}
2 \le x_n < 2 + 1 = 3 \tag{8}
\end{gather}
$$
Because $\{x_n\}$ is strictly increasing and bounded above by $3$, the Weierstrass Theorem on Monotonic Sequences guarantees that $\{x_n\}$ converges to a finite real limit $e := \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$ satisfying $2 < e \le 3$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
