---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-euclid-s-algorithm-works/","dg-note-properties":{}}
---

# Finite Termination of the Algorithm
Let $m, n \in \mathbb{N}$ with $m > n$. By the division property derived from the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Principle of Archimedes\|Principle of Archimedes]], dividing $m$ by $n$ yields a unique quotient $q_1 \in \mathbb{N}$ and remainder $r_1 \in \mathbb{N} \cup \{0\}$ such that $m = q_1 n + r_1$ with $0 \le r_1 < n$. If $r_1 = 0$, the algorithm terminates at the first step with $n \mid m$ and $\gcd(m, n) = n$. Otherwise, iterating the division process while the remainder remains positive produces the system
$$
\begin{align}
m &= q_1 n + r_1, \quad &0 < r_1 < n \\
n &= q_2 r_1 + r_2, \quad &0 < r_2 < r_1 \\
r_1 &= q_3 r_2 + r_3, \quad &0 < r_3 < r_2 \\
&\;\;\vdots \\
r_{k-2} &= q_k r_{k-1} + r_k, \quad &0 < r_k < r_{k-1} \\
r_{k-1} &= q_{k+1} r_k + 0 \tag{1}
\end{align}
$$
The sequence of positive remainders satisfies the strict descending chain
$$
\begin{gather}
n > r_1 > r_2 > r_3 > \dots > r_k > 0 \tag{2}
\end{gather}
$$

Because every nonempty subset of $\mathbb{N}$ possesses a minimal element ([[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Proposition 7 of the Properties of Natural Numbers]]), no infinite strictly decreasing sequence of natural numbers can exist (in fact, at most $n - 1$ positive remainders can occur below $n$). Thus, the division process must terminate after a finite number of steps $k + 1$ with a zero remainder $r_{k+1} = 0$.

---
# Invariance of Common Divisors and Identification of $\gcd(m, n)$

For any two integers $a, b \in \mathbb{Z}$, denote the set of their common divisors by $\operatorname{CD}(a, b) := \{d \in \mathbb{Z} \mid (d \mid a) \wedge (d \mid b)\}$. From the first equation of step 1,
$$
\begin{gather}
m = q_1 n + r_1 \iff r_1 = m - q_1 n \tag{3}
\end{gather}
$$
* If $d \in \operatorname{CD}(m, n)$, then $d$ divides both $m$ and $n$, so $d$ divides the integer linear combination $m - q_1 n = r_1$, which implies $d \in \operatorname{CD}(n, r_1)$.
* Conversely, if $d \in \operatorname{CD}(n, r_1)$, then $d$ divides both $n$ and $r_1$, so $d$ divides $q_1 n + r_1 = m$, which implies $d \in \operatorname{CD}(m, n)$.

Consequently, $\operatorname{CD}(m, n) = \operatorname{CD}(n, r_1)$. Applying this invariance inductively down each row of step 1 yields
$$
\begin{gather}
\operatorname{CD}(m, n) = \operatorname{CD}(n, r_1) = \operatorname{CD}(r_1, r_2) = \dots = \operatorname{CD}(r_{k-1}, r_k) = \operatorname{CD}(r_k, 0) \tag{4}
\end{gather}
$$

Because every non-zero integer divides $0$ ($0 = 0 \cdot d$), the set $\operatorname{CD}(r_k, 0)$ is simply the set of all divisors of $r_k$, whose maximal element is $r_k$ itself. Therefore,
$$
\begin{gather}
\gcd(m, n) = \max \operatorname{CD}(m, n) = \max \operatorname{CD}(r_k, 0) = r_k \tag{5}
\end{gather}
$$

---
# Derivation of Bézout's Identity
From the penultimate equation of step 1, isolate the greatest common divisor $d = r_k$:
$$
\begin{gather}
r_k = r_{k-2} - q_k r_{k-1} \tag{6}
\end{gather}
$$

Substituting $r_{k-1} = r_{k-3} - q_{k-1} r_{k-2}$ from the preceding row of step 1 into step 6 expresses $r_k$ as an integer linear combination of $r_{k-2}$ and $r_{k-3}$:
$$
\begin{gather}
r_k = r_{k-2} - q_k(r_{k-3} - q_{k-1} r_{k-2}) = (1 + q_k q_{k-1})r_{k-2} - q_k r_{k-3} \tag{7}
\end{gather}
$$

Continuing this back-substitution inductively through the $k$ equations of step 1 expresses $r_k$ at each stage as an integer linear combination $r_k = u_j r_j + v_j r_{j-1}$ with $u_j, v_j \in \mathbb{Z}$, terminating at $r_0 := n$ and $r_{-1} := m$ with integers $u, v \in \mathbb{Z}$ such that
$$
\begin{gather}
d = \gcd(m, n) = u m + v n \tag{8}
\end{gather}
$$
In particular, if $m$ and $n$ are relatively prime ($\gcd(m, n) = 1$), then $u m + v n = 1$. Conversely, if $u m + v n = 1$ for some $u, v \in \mathbb{Z}$, any common divisor $d \in \operatorname{CD}(m, n)$ must divide $u m + v n = 1$, forcing $d \in \{1, -1\}$ and $\gcd(m, n) = 1$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$