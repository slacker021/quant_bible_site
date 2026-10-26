---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-fundamental-theorem-of-arithmetic/","dg-note-properties":{}}
---

Establishing the Fundamental Theorem of Arithmetic requires first proving two foundational divisibility lemmas: 

# Prelude
### Lemma 1
$$\begin{gather} \textbf{Lemma: Coprime Divisibility} \\ \text{For integers } m, a, b \in \mathbb{Z} \text{ with } m \ne 0, \text{ if } m \mid (a \cdot b) \text{ and } \gcd(m, a) = 1, \text{ then } m \mid b. \end{gather}$$

>[!info]+ Remark: Greatest Common Divisor and Divisibility Notation
>The notation $\gcd(m, a) = 1$ (frequently abbreviated as $(m, a) = 1$ in classical number theory) signifies that $m$ and $a$ are relatively prime—their only common divisors in $\mathbb{Z}$ are $1$ and $-1$. The notation $m \mid b$ signifies that $m$ divides $b$, meaning there exists an integer $k \in \mathbb{Z}$ such that $b = k \cdot m$.

By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Euclid's Algorithm Works\|Bézout's Identity]], because $\gcd(m, a) = 1$, there exist integers $u, v \in \mathbb{Z}$ such that
$$\begin{gather} u m + v a = 1 \tag{1} \end{gather}$$
Multiplying both sides of step 1 by $b$ yields
$$\begin{gather} u m b + v (a b) = b \tag{2} \end{gather}$$
By hypothesis, $m \mid (ab)$, so there exists an integer $k \in \mathbb{Z}$ such that $ab = k m$. Substituting $ab = k m$ into step 2 produces
$$\begin{gather} b = u m b + v k m = m(u b + v k) \tag{3} \end{gather}$$
Since $\mathbb{Z}$ is closed under addition and multiplication, $(u b + v k) \in \mathbb{Z}$, which proves that $m \mid b$.

---
### Lemma 2
$$\begin{gather} \textbf{Lemma: Generalized Euclid's Lemma} \\ \text{If } p \text{ is a prime number and } p \mid (a_1 a_2 \cdots a_r) \text{ for integers } a_1, \dots, a_r \in \mathbb{Z}, \\ \text{then } p \mid a_i \text{ for at least one index } i \in \{1, \dots, r\}. \end{gather}$$

Begin with the base case $r = 2$, where $p \mid (a_1 a_2)$. If $p \mid a_1$, the claim holds immediately. Suppose instead that $p \nmid a_1$. Because $p$ is prime, its only positive divisors are $1$ and $p$. Since $p$ does not divide $a_1$, the greatest common divisor of $p$ and $a_1$ cannot be $p$, forcing $\gcd(p, a_1) = 1$. Applying Lemma 1 with $m = p$, $a = a_1$, and $b = a_2$ yields $p \mid a_2$. This establishes the base case $r = 2$.

Now proceed by induction on $r$. Assume the lemma holds for any product of $r - 1$ factors ($r > 2$), and suppose $p \mid (a_1 a_2 \cdots a_r)$. Grouping the first $r - 1$ factors gives
$$\begin{gather} p \mid \left( (a_1 a_2 \cdots a_{r-1}) \cdot a_r \right) \tag{4} \end{gather}$$

By the two-factor base case applied to step 4, either $p \mid a_r$ or $p \mid (a_1 a_2 \cdots a_{r-1})$. If $p \mid a_r$, the claim is satisfied; if $p \mid (a_1 a_2 \cdots a_{r-1})$, the inductive hypothesis guarantees that $p \mid a_i$ for some $i \in \{1, \dots, r - 1\}$. Thus, by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|Principle of Mathematical Induction]], Euclid's Lemma holds for any finite number of factors $r$.

---
# Actual Proof

### Existence of a Prime Factorization
Let $E \subset \mathbb{N}$ be the set of natural numbers $n$ such that either $n = 1$ or every natural number $m$ satisfying $2 \le m \le n$ can be expressed as a product of prime numbers. Clearly $1 \in E$, and since $2$ is prime, $2 \in E$. 

Suppose $n \in E$ for some $n \ge 2$, and consider $n + 1$. If $n + 1$ is prime, it is already a product of a single prime factor. If $n + 1$ is composite, then by definition there exist natural numbers $a, b \in \mathbb{N}$ satisfying
$$\begin{gather} n + 1 = a \cdot b \quad \text{with} \quad 2 \le a \le n \quad \text{and} \quad 2 \le b \le n \tag{5} \end{gather}$$

Because $n \in E$, both $a$ and $b$ can be written as products of primes: $a = p_1 \cdots p_s$ and $b = q_1 \cdots q_t$. Multiplying these representations gives $n + 1 = p_1 \cdots p_s q_1 \cdots q_t$, confirming that $(n + 1) \in E$. By the Principle of Mathematical Induction, every natural number $n > 1$ admits a prime factorization.

### Uniqueness of the Prime Factorization
Suppose a natural number $n > 1$ admits two prime factorizations:
$$\begin{gather} n = p_1 p_2 \cdots p_k = q_1 q_2 \cdots q_l \tag{6} \end{gather}$$

where $p_1 \le p_2 \le \dots \le p_k$ and $q_1 \le q_2 \le \dots \le q_l$ are prime numbers. Because $p_1$ divides the left-hand side of step 6, $p_1$ divides the product $q_1 q_2 \cdots q_l$. By Lemma 2, $p_1 \mid q_i$ for some index $i \in \{1, \dots, l\}$. Since $q_i$ is prime and $p_1 > 1$, the only divisor of $q_i$ greater than $1$ is $q_i$ itself, forcing $p_1 = q_i \ge q_1$.

By a completely symmetric argument, $q_1$ divides $p_1 p_2 \cdots p_k$, so $q_1 = p_j \ge p_1$ for some $j \in \{1, \dots, k\}$. Combining $p_1 \ge q_1$ and $q_1 \ge p_1$ yields
$$\begin{gather} p_1 = q_1 \tag{7} \end{gather}$$

Dividing both sides of step 6 by $p_1 = q_1$ yields
$$\begin{gather} p_2 \cdots p_k = q_2 \cdots q_l \tag{8} \end{gather}$$

Repeating this cancellation inductively pairs each $p_r$ with $q_r$ such that $p_r = q_r$. If $k \ne l$ (say, $k < l$), cancelling all $k$ prime factors would leave $1 = q_{k+1} \cdots q_l$, which is impossible since every prime satisfies $q_i \ge 2 > 1$. Therefore, $k = l$ and $p_r = q_r$ for all $r \in \{1, \dots, k\}$, proving that the prime factorization is unique up to the ordering of the factors.
$$\begin{gather} \textbf{Q.E.D} \end{gather}$$