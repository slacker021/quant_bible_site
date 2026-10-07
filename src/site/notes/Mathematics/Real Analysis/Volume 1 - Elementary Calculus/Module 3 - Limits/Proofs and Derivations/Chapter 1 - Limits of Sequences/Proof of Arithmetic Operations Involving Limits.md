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
$$
\textbf{Q.E.D}
$$