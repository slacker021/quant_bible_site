---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-q-ary-representation-theorem/","dg-note-properties":{}}
---

# Necessity
Let $x$ be a rational number, where $x = a/b$ such that $a$ and $b$ are both integers but $b > 0$. Furthermore, let $x$ be in base-$q$. This requires the algorithm of *long division*, which allows the digits $d_{1}, d_{2}, d_{3}, \dots$ to be found such that 
$$
x = d_{1}q^{-1} + d_{2}q^{-2} + d_{3}q^{-3} + \dots \tag{1}
$$

### Prelude: Proof of the Division Algorithm
The algorithm of long division posits that if $a$ and $b$ are two integers, where $a > 0$, then there's unique integers $q$ and $r$ such that $b = qa + r$ with $0 \le r < a$. 

Now, let 
$$
S = \{b - xa \ | b - xa \ge 0, x \in \mathbb{Z} \} \tag{2}
$$
One of the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|properties of natural numbers]], which may be referred to as the *well-ordering principle*, states that every non-empty set of positive integers contains a last element. This splits this proof into multiple cases:
- **Case 1:** If $b \ge 0$ and $x = 0$, then $b \in S$. 
- **Case 2:** If $b < 0$ and $x = b$, then $b - ba = b(1-a) \implies b - ba \in S$. 
Now, let $r$ be the least element in the set, where 
$$
r = b - qa \text{ and } r \ge 0 \tag{3}
$$
Now, with the intention of contradiction, assume that $r \ge a$. It then follows that
$$
\begin{gather}
b - qa \ge a \implies b - qa - a \ge 0 \implies b - a(q + 1) \ge 0 \tag{4}
\end{gather}
$$
However, 
$$
b - a(q + 1) < b - aq = r \tag{5}
$$
This is a contradiction, and it must be that $r < a$. This completes the demonstration of the existence of the integers $q$ and $r$. 

Now, suppose that $b = qa + r$ and $b = q'a + r'$, where $0 \le r < a$ and $0 \le r' < a$. It 
then follows that
$$
\begin{gather}
r = b - qa  \\
r' = b - q'a \tag{6}
\end{gather}
$$
and both equations can be manipulated such that
$$
r' - r = a(q - q') \tag{7}
$$
Now, the two inequalities mentioned earlier can be rearranged into
$$
-a < -r \le 0 \text{ and } 0 \le r' < a \implies -a < r' - r < a \implies |r' - r| < a\tag{8}
$$
It then follows that, after taking account of the eighth step, 
$$
|r' - r| = |a||q - q'| < a \implies |r' - r| = a|q - q'| < a\tag{9}
$$
and can then be simplified to
$$
|q - q'| < 1 \implies 0 \le |q - q'| < 1 \tag{10}
$$
In conclusion, $|q - q'| = 0 \implies q = q'$ and $r = r'$. This means that the two integers $q$ and $r$ are unique. 

### Applying Long Division
The algorithm of long division posits that the remainder $r_{n}$ be an integer such that $0 \le r_{n} < b$. Because there're only $b$ possible values for the remainder, which is represented by the set $\{ 0,1,2,\dots, b-1 \}$. Now, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Pigeonhole Principle\|Pigeonhole Principle]] dictates that after at most $b$ divisions, a remainder must repeat. Let $r_{j}$ be the first remainder that repeats at step $k$, where $k > j$, such that $r_{j} = k_{j}$. Since the next digit $d_{n+1}$ and next remainder $r_{n+1}$ are determined solely by the current remainder $r_{n}$ and the base $q$ by via the following relations: 
$$
d_{n+1} = l\lfloor \frac{q \cdot r_{n}}{b} \rfloor \text{ and } r_{n+1} = (q \cdot r_{n}) \tag{11}
$$
The repetition of $r_j$ implies that $d_{j+1} = d_{k+1}, r_{j+1} = r_{k+1}$, and so on. This results in a repeating sequence of digits, proving that the expansion is eventually period. 

---
# Sufficiency
Assuming the $q$-ary expansion of $x$ is eventually periodic, this means that after some rank $k$, the digits repeat $p$ places. The expression $x$ can be written as the sum of a terminating part and a repeating part: 
$$
x = \frac{A}{q^k} + \frac{1}{q^k} \sum_{i = 1}^\infty \frac{D}{q^{ip}} \tag{12}
$$
where $A$ is the integer value of the non-repeating prefix and $D$ is the integer value of the repeating block of length $p$. Now, the infinite sum is a geometric sequence: 
$$
\sum_{i = 1}^\infty \left( \frac{1}{q^p} \right)^i \tag{13}
$$
and the sum of a geometric series is
$$
\sum_{i=1}^\infty r^i \text{ is } \ \frac{r}{1-r} \ \text{ for } |r| < 1. 
$$
Here, $\frac{1}{q^p}$. Substituting this back into step 12 shows that
$$
x = \frac{A}{q^k} + \frac{1}{q^k} \left(\frac{1/q^p}{1 - 1/^p} \right) = \frac{A}{q^k} + \frac{1}{q^k}\left( \frac{1}{q^p - 1} \right) \tag{14}
$$
Combining these over a common denominator shows that
$$
x = \frac{A(q^p - 1) + 1}{q^k(q^p - 1)} \tag{15}
$$
Since $A, q, p,$ and $k$ are all integers, $x$ is expressed as a ratio of two integers. By definition, $x$ is a rational number. 
$$
\textbf{Q.E.D}
$$





