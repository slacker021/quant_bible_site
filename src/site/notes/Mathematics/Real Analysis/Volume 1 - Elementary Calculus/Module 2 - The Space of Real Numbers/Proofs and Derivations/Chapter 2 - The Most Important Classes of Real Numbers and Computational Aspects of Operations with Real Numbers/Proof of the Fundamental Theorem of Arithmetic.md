---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-fundamental-theorem-of-arithmetic/","dg-note-properties":{}}
---

To show that the fundamental theorem of arithmetic holds true, two lemmas are required:

# Proof of Lemma 1

### Lemma Statement
$$
\begin{gather}
\textbf{Lemma: } \\[5mm]
\text{If } m \mid pq \text{ and } (m,p) = 1, \text{ then } m \mid q.   
\end{gather}
$$
>[!info]+ Remark: Greatest Common Divisor (GCD)
In the context of this lemma, $(a,b) = 1$ means that the *greatest common divisor* of $a$ and $b$ is $1$. Additionally, $m \mid q$ means that $q$ divides $m$ into a whole number. These notations are most commonly used in *Number Theory*, which is not explored in these notes.

### Proof Statement

Let 
$$
1 = (m,p) = am + bp \text{ for some } a,b \in \mathbb{Z} \tag{1}
$$
then 
$$
q = amq + bpq \tag{2}
$$
Now
$$
m \mid amq \text{ and } m \mid bpq \text{ (since m \ | \ pq)}, \tag{3} 
$$
so $m \mid (amq + bpq) = q$. 

---
# Proof of Lemma 2

### Lemma Statement
$$
\begin{gather}
\text{Lemma: Euclid} \\[5mm]
\text{If } p \text{ is prime and } p \mid a_{1} a_{2} \dots a_{n}, \text{ then } \\
p \mid a_{i} \text{ for some } i.
\end{gather}
$$
If $n = 2$, then the result says that if $p$ is prime and $p | ab$, then $p | a$ or $p | b$. This is often called *Euclid’s lemma*.

### Proof Statement
Begin with the case of $n = 2$. Suppose $p \mid a_{1} a_{2}$, and suppose $p \nmid a_{1}$. $(p, a_{1}) \mid p$ and $p$ is prime, so $(p, a_{1}) = 1$ or $(p, a_{1}) = p$, then $p = (p, a_{1}) \mid a_{1}$, which contradicts the premise that $p \nmid a_{1}$. Therefore, $(p,m_{1}) = 1$. By the preceding lemma, $p \mid a_{2}$. This establishes the case $n = 2$. 

Now, assume $n > 2$, and assume the result is true when $p$ divides a product of with less than $n$ factors. Suppose that $p \mid a_{1} a_{2} \dots a_{n}$. Grouping the terms yields
$$
p \mid (a_{1} a_{2} \dots a_{n-1})a_{n}. \tag{4} 
$$
By the case $n = 2$, either $p \mid a_{1} a_{2} \dots a_{n-1}$ or $p \mid a_{n}$. If $p \mid a_{n}$, then nothing else has to be done. Otherwise, if $p \mid a_{1} a_{2} \dots a_{n-1}$, then $p$ divides one of $a_{1}, a_{2}, \dots, a_{n-1}$, by induction. In either case, it's shown that $p$ divides one of the $a_{i}$s, which completes the inductive step. 

---
# Proof of the Fundamental Theorem of Arithmetic
Now that both Lemmas have been derived, the fundamental theorem of arithmetic can now be proven. 

The base case $n = 2$ is true because $2$ is prime. Now, suppose $n >2$, and assume every number less than $n$ can be factored into a product of primes. If $n$ is prime, then nothing else has to be done. Otherwise, $n$ is *composite*, so $n$ can be factored as $n = ab$, where $1 < a, b < n$. By induction, $a$ and $b$ can be factored into primes. Then $n = ab$ shows that $n$ can, too. 

Now, suppose that 
$$
p_{1}^{m_{1}} \dots p_{j}^{m_{j}} = q_{1}^{n_{1}} \dots q_{k}^{n_{k}} \tag{5}
$$
Here, the values $p$ and $q$ are distinct primes, and all the exponents are greater than or equal to $1$. Looking at $p_{1}$, it divides both the left and right side. By the second lemma, $p_{1} \mid q_{i}^{n_{i}}$ for some $i$. However, $q_{i}$ is $q_{i} \dots q_{i}$ ($n_{i}$ times), so again by the second lemma, $p_{1} \mid q_{i}$. Since $p_{1}$ and $q_{i}$ are prime, $p_{1} = q_{i}$. This can be renumbered by renumbering the values $q$ so that $q_{i}$ becomes $q_{1}$ and vice versa. Thus, $p_{1} = q_{1}$, where the equation reads
$$
p_{1}^{m_{1}} \dots p_{j}^{m_{j}} = p_{1}^{n_{1}} \dots q_{k}^{n_{k}} \tag{6} 
$$
If $m_{1} > n_{1}$, cancel $p_{1}^{n_{1}}$ from both sides, leaving
$$
p_{1}^{m_{1} - n_{1}} \dots p_{j}^{m_{j}} = q_{2}^{n_{2}} \dots q_{k}^{n_{k}} \tag{7} 
$$
This is a contradiction, since now $p_{1}$ divides the left but not the right side. For the same reason, $m_{1} < n_{1}$ is also a contradiction. Thus, it follows that $m_{1} = n_{1}$. This means that the $p_{1}$ of both sides can be cancelled, leaving
$$
p_{2}^{m_{2}} \dots p_{j}^{m_{j}} = q_{2}^{n_{2}} \dots q_{k}^{n_{k}}. \tag{8} 
$$
This pattern can be kept going, where at each stage, a power of a $p$ can be paired with a power of a $q$, and the preceding argument shows that the powers are equal. This means that no primes can be left over at the end, or this'd result in a product of primes equal to $1$. Therefore, everything must be paired up, and the original factorizations were the same (except possibly for the order of the factors). 
$$
\textbf{Q.E.D}
$$