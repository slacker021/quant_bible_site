---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-q-ary-representation-theorem/","dg-note-properties":{}}
---

# Necessity
Let $x \in \mathbb{Q}$ be a rational number expressed as $x = \frac{a}{b}$, where $a, b \in \mathbb{Z}$ and $b > 0$, and let $q \in \mathbb{N}$ be an integer base satisfying $q \ge 2$. By decomposing $x = \lfloor x \rfloor + \{x\}$, where the integer part $\lfloor x \rfloor \in \mathbb{Z}$ possesses a finite positional expansion in base $q$, it suffices to analyze the fractional part $\{x\} = \frac{r_0}{b} \in [0, 1[$, where $r_0 \in \{0, 1, \dots, b - 1\}$. Without loss of generality, assume $0 \le x = \frac{r_0}{b} < 1$. Constructing the $q$-ary digits $d_1, d_2, d_3, \dots \in \{0, 1, \dots, q - 1\}$ such that
$$
\begin{gather}
x = d_{1}q^{-1} + d_{2}q^{-2} + d_{3}q^{-3} + \dots = \sum_{n=1}^\infty \frac{d_n}{q^n} \tag{1}
\end{gather}
$$
relies on the integer division algorithm.

### Prelude: Proof of the Division Algorithm
The division algorithm asserts that for any integers $m, n \in \mathbb{Z}$ with $n > 0$, there exist unique integers $u, r \in \mathbb{Z}$ such that $m = u n + r$ with $0 \le r < n$.

To prove existence, define the set of non-negative integer linear combinations:
$$
\begin{gather}
S := \{m - k n \mid k \in \mathbb{Z} \ \wedge \ m - k n \ge 0\} \subset \mathbb{N} \cup \{0\} \tag{2}
\end{gather}
$$
To verify that $S$ is nonempty, consider two exhaustive cases for $m \in \mathbb{Z}$:
- **Case 1 ($m \ge 0$):** Setting $k = 0$ yields $m - 0 \cdot n = m \ge 0$, so $m \in S$.
- **Case 2 ($m < 0$):** Setting $k = m$ yields $m - m n = m(1 - n)$. Because $n \in \mathbb{N}$ satisfies $n \ge 1$, it follows that $1 - n \le 0$. Since $m < 0$ and $1 - n \le 0$, their product satisfies $m(1 - n) \ge 0$, which ensures $m(1 - n) \in S$.

Because $S$ is a nonempty subset of $\mathbb{N} \cup \{0\}$, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Well-Ordering Principle]] guarantees that $S$ possesses a unique minimal element $r := \min S$. By definition of $S$, there exists an integer $u \in \mathbb{Z}$ such that
$$
\begin{gather}
r = m - u n \quad \text{and} \quad r \ge 0 \tag{3}
\end{gather}
$$
Suppose, for the sake of contradiction, that $r \ge n$. Subtracting $n$ from both sides of $r \ge n$ yields
$$
\begin{gather}
m - u n \ge n \implies m - u n - n \ge 0 \implies m - (u + 1)n \ge 0 \tag{4}
\end{gather}
$$
By step 4, the integer $m - (u + 1)n$ belongs to $S$. However, because $n > 0$,
$$
\begin{gather}
m - (u + 1)n = r - n < r \tag{5}
\end{gather}
$$
which contradicts the minimality of $r = \min S$. Thus, $0 \le r < n$, establishing the existence of $u$ and $r$.

To prove uniqueness, suppose $m = u n + r$ and $m = u' n + r'$ with $0 \le r < n$ and $0 \le r' < n$. Expressing both remainders explicitly gives
$$
\begin{gather}
r = m - u n \\[2mm]
r' = m - u' n \tag{6}
\end{gather}
$$
Subtracting the first equation from the second in step 6 yields
$$
\begin{gather}
r' - r = n(u - u') \tag{7}
\end{gather}
$$
Combining the bounds $-n < -r \le 0$ and $0 \le r' < n$ produces
$$
\begin{gather}
-n < r' - r < n \implies |r' - r| < n \tag{8}
\end{gather}
$$
Taking the absolute value of step 7 and applying step 8 with $|n| = n > 0$ gives
$$
\begin{gather}
|r' - r| = |n||u - u'| = n|u - u'| < n \tag{9}
\end{gather}
$$
Dividing step 9 by $n > 0$ yields
$$
\begin{gather}
0 \le |u - u'| < 1 \tag{10}
\end{gather}
$$
Because $u$ and $u'$ are integers, $|u - u'|$ is a non-negative integer strictly less than $1$, forcing $|u - u'| = 0$, so $u = u'$ and consequently $r = r'$. Thus, the quotient and remainder are unique.

### Applying Long Division
Beginning with the initial remainder $r_0 \in \{0, 1, \dots, b - 1\}$, successive steps of long division in base $q$ define the digit $d_{n+1}$ and the next remainder $r_{n+1}$ for each $n \in \mathbb{N} \cup \{0\}$ by dividing $q \cdot r_n$ by $b$:
$$
\begin{gather}
q \cdot r_n = d_{n+1} b + r_{n+1}, \quad \text{where} \quad d_{n+1} = \left\lfloor \frac{q \cdot r_{n}}{b} \right\rfloor \quad \text{and} \quad r_{n+1} = q \cdot r_{n} - d_{n+1} b \tag{11}
\end{gather}
$$
At every step $n$, the remainder $r_n$ is an integer satisfying $0 \le r_n < b$, meaning $r_n$ can take at most $b$ distinct values from the finite set $\{0, 1, 2, \dots, b - 1\}$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Pigeonhole Principle\|Pigeonhole Principle]], among the first $b + 1$ remainders $r_0, r_1, \dots, r_b$, at least two must be identical. Let $j$ and $k$ with $0 \le j < k \le b$ be the first pair of indices such that $r_j = r_k$, and set $p := k - j \ge 1$. Because $d_{n+1}$ and $r_{n+1}$ are uniquely determined by $r_n$ via step 11, the equality $r_j = r_k$ implies by induction that $d_{n + p} = d_n$ and $r_{n + p} = r_n$ for all $n > j$. Thus, the $q$-ary expansion of $x$ is eventually periodic with period $p$.

---
# Sufficiency
Conversely, suppose that the $q$-ary expansion of a real number $x \ge 0$ is eventually periodic: after $k \ge 0$ non-repeating fractional digits, a block of $p \ge 1$ digits repeats indefinitely. Then $x$ can be decomposed into a terminating prefix and an infinite periodic tail:
$$
\begin{gather}
x = \frac{A}{q^k} + \frac{1}{q^k} \sum_{i = 1}^\infty \frac{D}{q^{i p}} \tag{12}
\end{gather}
$$
where $A \in \mathbb{N} \cup \{0\}$ is the integer formed by the non-repeating prefix shifted by $q^k$, and $D \in \{0, 1, \dots, q^p - 1\}$ is the integer represented by the repeating block of length $p$. Factoring $D$ out of the summation in step 12 isolates a geometric series:
$$
\begin{gather}
\sum_{i = 1}^\infty \frac{D}{q^{i p}} = D \sum_{i = 1}^\infty \left( \frac{1}{q^p} \right)^i \tag{13}
\end{gather}
$$
Because $q \ge 2$ and $p \ge 1$, the common ratio $r := \frac{1}{q^p}$ satisfies $0 < r < 1$, so the geometric series converges to $\frac{r}{1 - r}$. Substituting this closed-form sum into step 12 yields
$$
\begin{gather}
x = \frac{A}{q^k} + \frac{D}{q^k} \left(\frac{1/q^p}{1 - 1/q^p} \right) = \frac{A}{q^k} + \frac{D}{q^k(q^p - 1)} \tag{14}
\end{gather}
$$
Combining both fractions over a common denominator gives
$$
\begin{gather}
x = \frac{A(q^p - 1) + D}{q^k(q^p - 1)} \tag{15}
\end{gather}
$$
Because $A, D, q, p, k \in \mathbb{Z}$ with $q^k(q^p - 1) \in \mathbb{N}$, the numerator and denominator in step 15 are integers with a positive denominator. Therefore, $x \in \mathbb{Q}$ is a rational number.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
