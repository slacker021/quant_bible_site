---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-properties-of-natural-numbers/","dg-note-properties":{}}
---

# Proposition 1
Let $m$ and $n$ be natural numbers, and let $E$ be the set of natural numbers $n$ for which $(m + n) \in \mathbb{N}$ for all $m \in \mathbb{N}$. Then by definition, $1$ is in $E$ since 
$$
(m \in \mathbb{N}) \implies ((m + 1) \in \mathbb{N}) \ \forall m \in N. \tag{1}
$$
If $n \in E$, that is $(m + n) \in \mathbb{N}$, then $(n + 1) \in E$ also, since 
$$
(m + (n + 1)) = ((m + n) + 1) ∈ N. \tag{2}
$$
By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|principle of induction]], $E = \mathbb{N}$. Therefore, the addition of two or more natural numbers doesn't lead to a sum that isn't a natural number. 

Similarly, taking $E$ to be the set of natural numbers $n$ for which $(m \cdot n) \in \mathbb{N}$ for all $m \in \mathbb{N}$, it can be found that $1 \in E$, since $m \cdot 1 = m$, and if $n \in E$, that is, $m \cdot n \in \mathbb{N}$, then $(m \cdot (n + 1)) = mn + m$ is the sum of two natural numbers, which belongs to $\mathbb{N}$ by what was just proved above. Thus, 
$$
(n \in E) \implies ((n + 1) \in E) \tag{3}
$$
and so by the principle of induction, $E = \mathbb{N}$. 

---
# Proposition 2
Let $E$ be the set consisting of all real numbers of the form $n - 1$, where $n$ is a natural number different from $1$. Since $1$'s a natural number, it follows that 
$$
2:= (1 + 1) \in \mathbb{N} \text{ and hence } 1 = (2 -1) \in E. \tag{4}
$$
If $m \in E$, then $m = n - 1$, where $n \in \mathbb{N}$; then $m + 1 = (n + 1) -1$, and since $n + 1 \in \mathbb{N}$, it can be inferred that $(m + 1) \in E$. By the principle of induction, it can be concluded that $E = \mathbb{N}$. 

---
# Proposition 3
Let
$$
M = \{x ∈ \mathbb{N} \ | \  (x = 1) ∨ (2 ≤ x) \}.\tag{5}
$$
By definition of $M$, $1 \in M$. Then if $x \in M$, either $x = 1$, in which case $x + 1 = 2 \in M$, or else $2 \leq x$, and then $2 \le (x + 1)$, and once again $(x + 1) \in M$. Thus, $M = \mathbb{N}$, and hence if $(x = 1) ∧ (x ∈ \mathbb{N})$, then $2 \le x$, that is, $\text{min}\{ x \in \mathbb{N} \ | \ 1 < x\} = 2$.  

Now, if 
$$
x \in \{x \in \mathbb{N} \ | \ n + 1 < x  \} \tag{6}
$$
then
$$
(x - 1) = y \in \{ y \in \mathbb{N} \ | \ n < y \}. \tag{7}
$$
For, by what's already been proven, every natural number is at least as large as $1$; therefore
$$
(n + 1 < x) \implies (1 < x) \implies (x \ne 1) \tag{8}
$$
and consequently, 
$$
\text{min}\{ y \in \mathbb{N} \ | \ n < y \} = n + 1. \tag{9}
$$
Then, $x - 1 \ge y \ge n + 1$ and $x \ge n + 1$. Hence, 
$$
(x ∈ \{x ∈ \mathbb{N} \  | \  n + 1 < x \}) \implies (x ≥ n + 2) \tag{10}
$$
and consequently,
$$
\text{min}\{ x \in \mathbb{N} \ | \ n + 1 < x \} = n + 2, \tag{11}
$$
that is, $n + 1 \in E$. By the principle of induction $E = \mathbb{N}$ and this proposition has been proven. 

---
# Proposition 4
Let $m$ and $n$ be natural numbers, where $n$ is less than $m$.  

### Direct Proof
By definition of [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|"less than"]], the statement $n < m$ is equivalent to stating that $m - n$ is a positive integer. By definition, definition of the natural numbers, the smallest positive integer is $1$. Therefore, $m - n \ge 1$. Adding $n$ to both sides of this inequality yields
$$
(m - n) + n \ge 1 + n \implies m \ge n + 1 \tag{12}
$$
The terms can be rearranged such that $n + 1 \le m$. 

### Contradiction
Suppose that $n < m$ is true but the conclusion is false, where the negation of $n+1≤m$ is
$𝑛+1 > m$. In the context of natural numbers, if $n + 1$ is greater than $m$, then it must be that $n + 1$ must be at least $m + 1$. (Note: If it were $m$ or less, then it would contradict the assumption.). Thus, 
$$
n+1≥m+1 \tag{13}
$$
Subtracting $1$ from both sides of the inequality yields 
$$
(n+1)−1≥(m+1)−1 \implies n≥m \tag{14}
$$
This concludes that $n≥m$, which contradicts the premise stated that $n < m$. An integer cannot be simultaneously less than and greater than (or equal to) another integer. Therefore, the original statement that $n + 1 \le m$ must be true. 

---

# Proposition 5
By definition of the natural numbers, every natural number except $1$ is the successor of a natural number. This statement is vacuously true for $1$ and if it holds for $n$, then it holds for $n + 1$. Furthermore, every natural number is greater than or equal to $1$. By the principle of induction, this holds true for $1$ and if $n \ge 1$, then
$$
n + 1 \ge 1 + 2 > 1 \tag{15} 
$$
Now, suppose $q$ is a natural number strictly between $1$ and $2$. Since $q$ isn't $1$, it's the successor of some natural number $q'$ that's greater than or equal to $1$. But $q' \ge 0$ implies that 
$$
q = q' + 1 \ge 1 + 2 = 1 \tag{16}
$$
which contradicts the assumption that $q < 2$. Therefore, there is no natural number between $1$ and $2$. This is the base case of this proof.  

Now that the base case has been completed, the inductive step can now be taken. 
For any natural number $n$, there's no natural number between $n$ and $n + 1$, which was shown in the base case. If there was a natural number $q$ between $n + 1$ and $n + 2$, then it would be the successor of some $q'$, and that $q'$ would have to lie between $n$ and $n + 1$, because if $q' \le n$ then $q = q' + 1 \ge n + 2$. Therefore, if the statement holds for $n$, then it holds for $n + 1$. 

---
# Proposition 6
Let $n$ be a natural number such that $n \ne 1$. Now, assume that there's a natural number $x$ such that 
$$
n - 1 < x < n \tag{17}
$$
Since $x$ and $n$ are natural numbers, the following property can be used:
$$
a < b \implies b - a \ge 1 \tag{18}
$$
This leads to two separate inequalities: 
1. From $n - 1 < x$, it follows that $x - (n + 1)$. Simplifying this yields the inequality $x - n + 1 \ge 1$. 
2. From $x < n$, it follows that $n - x \ge 1$. 
The two inequalities can then be added together:
$$
(x−n+1)+(n−x)≥1+1 \tag{19}
$$
Simplifying the left side, the $x$ and $-x$ terns cancel out, and the $-n$ and $n$ terms also cancel out. This leaves the result that $1 \ge 2$. This is a contradiction because it's impossible for $1 \ge 2$. Therefore, it must be that if $n \ne 1$, then $n - 1$ is the immediate predecessor of $n$.

---
# Proposition 7
Let $M \subset \mathbb{N}$. If $1 \in M$, then $\text{min} M = 1$, since $\forall n \in \mathbb{N} (1 \le n)$. Now, suppose that $1$ isn't an element of $M$, where $1 \in E = \mathbb{N} \setminus M$. The set $E$ must contain a natural number $n$ such that all natural numbers aren't larger than $n \in E$ but $n + 1 \in M$. If there wasn't such an $n$, the set $E \subset \mathbb{N}$, which contains $1$, would contain along with each of its elements $n$, the number $(n + 1)$ also; by the principle of induction, it would therefore equal $\mathbb{N}$. However, the latter is impossible because $\mathbb{N} \setminus E = M \ne \emptyset$. The number $(n + 1)$ so found must be the smallest element of $M$, since there're no natural numbers between $n$ and $n + 1$, which has been proven true by the fifth proposition. 

$$
\textbf{Q.E.D}
$$


