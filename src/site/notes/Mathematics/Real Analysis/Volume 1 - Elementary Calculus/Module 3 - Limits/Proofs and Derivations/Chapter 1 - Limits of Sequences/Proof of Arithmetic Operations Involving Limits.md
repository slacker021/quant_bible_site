---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-arithmetic-operations-involving-limits/","dg-note-properties":{}}
---

Let $\{x_n\}$ and $\{y_n\}$ be two convergent sequences such that $\lim_{n \to \infty} x_n = A$ and $\lim_{n \to \infty} y_n = B$.
# Theorem 1
Let $\varepsilon > 0$. By the definition of convergence, there exists an index $N_1 \in \mathbb{N}$ such that for all $n > N_1$, $\vert x_n - A \vert < \frac{\varepsilon}{2}$. Similarly, there exists an index $N_2 \in \mathbb{N}$ such that for all $n > N_2$, $\vert y_n - B \vert < \frac{\varepsilon}{2}$. Let $N = \max(N_1, N_2)$. For all $n > N$, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] gives:  

$$\vert (x_n + y_n) - (A + B) \vert = \vert (x_n - A) + (y_n - B) \vert \le \vert x_n - A \vert + \vert y_n - B \vert \tag{1}$$
Substituting the bounds yields
$$\vert (x_n + y_n) - (A + B) \vert < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{2}$$
Thus, the sum of the sequences converges to $A + B$.

---
# Theorem 2
Because $\{x_n\}$ is convergent, it is bounded. Therefore, there's a real number $M > 0$ such that $\vert x_n \vert \le M$ for all $n \in \mathbb{N}$. Let $\varepsilon > 0$. Through algebraic manipulation, the distance between the terms and the target limit can be expressed as:  
$$\vert x_n y_n - A B \vert = \vert x_n y_n - x_n B + x_n B - A B \vert \le \vert x_n \vert \vert y_n - B \vert + \vert B \vert \vert x_n - A \vert \tag{3}$$
Using the bound $M$, this becomes
$$\vert x_n y_n - A B \vert \le M \vert y_n - B \vert + \vert B \vert \vert x_n - A \vert \tag{4}$$
By convergence, there's an index $N_1$ such that $\vert y_n - B \vert < \frac{\varepsilon}{2M}$ for all $n > N_1$. Additionally, there's an index $N_2$ such that $\vert x_n - A \vert < \frac{\varepsilon}{2(\vert B \vert + 1)}$ for all $n > N_2$. (The term $\vert B \vert + 1$ is used to prevent division by zero in the event that $B = 0$). Let $N = \max(N_1, N_2)$. For all $n > N$, 
$$\vert x_n y_n - A B \vert < M \left( \frac{\varepsilon}{2M} \right) + \vert B \vert \left( \frac{\varepsilon}{2(\vert B \vert + 1)} \right) < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{5}$$
Thus, the product of the sequences converges to $A \cdot B$. 

---
# Theorem 3
It suffices to prove that $\lim_{n \to \infty} \frac{1}{y_n} = \frac{1}{B}$, as the full quotient rule follows directly by combining this result with the product rule. Let $\varepsilon > 0$. Because $\lim_{n \to \infty} y_n = B \neq 0$, there's an index $N_1 \in \mathbb{N}$ such that $\vert y_n - B \vert < \frac{\vert B \vert}{2}$ for all $n > N_1$. Applying the reverse triangle inequality reveals that $\vert y_n \vert > \frac{\vert B \vert}{2}$ for all $n > N_1$. Furthermore, there's an index $N_2 \in \mathbb{N}$ such that for all $n > N_2$, $\vert y_n - B \vert < \varepsilon \frac{\vert B \vert^2}{2}$. Let $N = \max(N_1, N_2)$. For all $n > N$, the absolute difference evaluates to
$$\left\vert \frac{1}{y_n} - \frac{1}{B} \right\vert = \frac{\vert B - y_n \vert}{\vert y_n \vert \vert B \vert} < \frac{\varepsilon \frac{\vert B \vert^2}{2}}{\frac{\vert B \vert}{2} \vert B \vert} = \varepsilon \tag{6}$$
Thus, $\{\frac{1}{y_n}\}$ converges to $\frac{1}{B}$. Applying the product rule gives $\lim_{n \to \infty} \left(x_n \cdot \frac{1}{y_n}\right) = \frac{A}{B}$.

---
# Theorem 4

### Case 1
If $\varepsilon = 0$, then every term of the sequence $x_{n}$ is also equal to zero. This results in a constant sequence, which is [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|ultimately convergent]] to $0$. 

### Case 2
Let $\varepsilon > 0$ and $c \neq 0$. By definition of the limit of a sequence, 
$$
|c \cdot x_{n} -  c A | < \varepsilon \implies |c||x_{n} - A| < \varepsilon \tag{7}
$$
Multiplying both sides by $\frac{1}{|c|}$ and by virtue of there being an $N \in \mathbb{N}$ for all values of $n > N$, 
$$
|x_{n} - A| < \frac{\varepsilon}{|c|} \tag{8}
$$
Multiplying both sides of the inequality by $|c|$, 
$$
|c||x_{n} - A| < |c| \left(\frac{\varepsilon}{|c|} \right) = \varepsilon \tag{9}
$$
Therefore, for any $\varepsilon > 0$, there's a $N \in \mathbb{N}$ such that for all $n \ge N$, 
$$
|c x_{n} - c A| < \varepsilon \tag{10}
$$
Thus demonstrating that $\lim_{ n \to \infty } c x_{n} = c \cdot A$. 

---
# Theorem 5
Let $\varepsilon > 0$. Since $x_{n} = A$ there's a $N_{1}$ such that
$$
n > N_{1} \implies |x_{n}| \le |x_{n} - A| + |A| < 1 + |A| \tag{11}
$$
If $|x|$ and $|y|$ are both less than or equal to $M$, then 
$$
|x^p - y^p| = |x-y| \left| \ \sum_{k=0}^{p = 1} \ x^k y^{p-1-k} \right| \le |x-y| p M^{p-1} \tag{12}
$$
Replacing $x$ with $x_{n}$,  $y$ with $A$, and $M$ with $1 + |A|$ shows that
$$
|x_{n}^p - A^p | \le |x_{n} - A| p(1 + |A|)^{p-1} \ \text{ when } n > N_{1} \tag{13}
$$
Now, let $N_{2}$ be such that
$$
n > N_{2} \implies |x_{n} - A| < \frac{\varepsilon}{p(1 + |A|)^{p-1}} \tag{14}
$$
Then, 
$$
N > \text{max}(N_{1}, N_{2}) \implies |x_{n}^p - A^p | < \varepsilon \tag{15}
$$
$$
\textbf{Q.E.D}
$$
