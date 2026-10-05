---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-euclid-s-algorithm-works/","dg-note-properties":{}}
---

Let $m, n \in \mathbb{N}$ with $m > n$. The Euclidean algorithm performs successive integer divisions with remainders:  
$$\begin{aligned} m &= q_1 n + r_1, \quad &0 < r_1 < n \\ n &= q_2 r_1 + r_2, \quad &0 < r_2 < r_1 \\ r_1 &= q_3 r_2 + r_3, \quad &0 < r_3 < r_2 \\ &\;\;\vdots \\ r_{k-2} &= q_k r_{k-1} + r_k, \quad &0 < r_k < r_{k-1} \\ r_{k-1} &= q_{k+1} r_k + 0 \end{aligned} \tag{1}$$
From the remainder constraints in the division algorithm, the sequence of remainders satisfies:  
$$n > r_1 > r_2 > r_3 > \dots > r_k \ge 0 \tag{2}$$
Because the set $\{ r \in \mathbb{N}_0 \mid r < n \}$ is finite and strictly bounded below by $0$, a strictly decreasing sequence of non-negative integers cannot be infinite. Therefore, the algorithm must terminate in a finite number of steps $k+1$, producing a remainder of zero ($r_{k+1} = 0$). Let $r_k$ be the last non-zero remainder. 

Now, let $\operatorname{CD}(a, b)$ denote the set of common divisors of two integers $a$ and $b$. From the first division equation:  
$$m = q_1 n + r_1 \iff r_1 = m - q_1 n \tag{3}$$
- If $d$ divides both $m$ and $n$, then $d$ divides the linear combination $m - q_1 n = r_1$. Hence, $d \in \operatorname{CD}(n, r_1)$, showing $\operatorname{CD}(m, n) \subset \operatorname{CD}(n, r_1)$.
- Conversely, if $d$ divides both $n$ and $r_1$, then $d$ divides $q_1 n + r_1 = m$. Hence, $d \in \operatorname{CD}(m, n)$, showing $\operatorname{CD}(n, r_1) \subset \operatorname{CD}(m, n)$.
Therefore,

$$\operatorname{CD}(m, n) = \operatorname{CD}(n, r_1) \tag{4}$$
Applying this invariant equality across each step of the algorithm:  
$$\operatorname{CD}(m, n) = \operatorname{CD}(n, r_1) = \operatorname{CD}(r_1, r_2) = \dots = \operatorname{CD}(r_{k-1}, r_k) = \operatorname{CD}(r_k, 0) \tag{5}$$
Since every divisor of $r_k$ divides $0$, the common divisors of $r_k$ and $0$ are simply the divisors of $r_k$. The largest divisor of $r_k$ is $r_k$ itself. Thus,
$$\gcd(m, n) = \max \operatorname{CD}(m, n) = \max \operatorname{CD}(r_k, 0) = r_k \tag{6}$$
This proves that the final non-zero remainder is the greatest common divisor.

And just like that, from the penultimate equation in the system shown in the very first step of this argument, the greatest common divisor $r_k$ can be isolated:  
$$r_k = r_{k-2} - q_k r_{k-1} \tag{7}$$
From the preceding equation, isolate $r_{k-1} = r_{k-3} - q_{k-1} r_{k-2}$ and substitute it into the seventh step: 
$$r_k = r_{k-2} - q_k (r_{k-3} - q_{k-1} r_{k-2}) = (1 + q_k q_{k-1}) r_{k-2} - q_k r_{k-3} \tag{8}$$
The preceding equation expresses $r_k$ as an integer linear combination of $r_{k-2}$ and $r_{k-3}$. By repeating this back-substitution recursively through each division equation:  
$$r_k = A_j r_j + B_j r_{j-1} \quad (A_j, B_j \in \mathbb{Z}) \tag{9}$$
Continuing until $r_1$ and $n$ are replaced by the initial inputs $m$ and $n$ yields integers $p, q \in \mathbb{Z}$ such that
$$r_k = \gcd(m, n) = pm + qn \tag{10}$$
In the special case where $m$ and $n$ are relatively prime, $\gcd(m, n) = 1$, which gives $pm + qn = 1$.
$$
\textbf{Q.E.D}
$$
