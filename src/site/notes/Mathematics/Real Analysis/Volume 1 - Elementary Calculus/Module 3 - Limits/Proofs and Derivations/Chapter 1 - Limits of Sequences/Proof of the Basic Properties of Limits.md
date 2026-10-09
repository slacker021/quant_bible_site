---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-basic-properties-of-limits/","dg-note-properties":{}}
---

# Theorem 1
Let $\{x_n\}$ be an ultimately constant sequence. By definition, there exists a real number $A$ and an index $N \in \mathbb{N}$ such that $x_n = A$ for all $n > N$. Additionally, let $\varepsilon > 0$ be given. The absolute difference is evaluated as $\vert x_n - A \vert = \vert A - A \vert = 0$. Since $0 < \varepsilon$ is strictly true for all $\varepsilon > 0$, the inequality $\vert x_n - A \vert < \varepsilon$ holds for all $n > N$. Therefore, the sequence converges to $A$.

---
# Theorem 2
 Let $\{x_n\}$ be a sequence converging to a limit $A$. Consider an arbitrary neighborhood around $A$, defined by an $\varepsilon$-radius: $(A - \varepsilon, A + \varepsilon)$ for some $\varepsilon > 0$. By the definition of convergence, there exists an index $N \in \mathbb{N}$ such that for all $n > N$, $\vert x_n - A \vert < \varepsilon$. This inequality is equivalent to stating that $x_n \in (A - \varepsilon, A + \varepsilon)$ for all $n > N$. Thus, only the terms $x_1, x_2, \dots, x_N$ may potentially lie outside this neighborhood. Since $N$ is a finite integer, all but a finite number of terms reside within the given neighborhood. 

---
# Theorem 3
Assume for the sake of contradiction that a sequence $\{x_n\}$ converges to two distinct limits, $A$ and $B$, with $A \neq B$. Let $\varepsilon = \frac{\vert A - B \vert}{2}$. Since $A \neq B$, it follows that $\varepsilon > 0$. By the definition of convergence, there exists an index $N_1 \in \mathbb{N}$ such that $\vert x_n - A \vert < \varepsilon$ for all $n > N_1$, and an index $N_2 \in \mathbb{N}$ such that $\vert x_n - B \vert < \varepsilon$ for all $n > N_2$. Let $N = \max(N_1, N_2)$. For any $n > N$, the Triangle Inequality yields:  
$$\vert A - B \vert = \vert A - x_n + x_n - B \vert \le \vert A - x_n \vert + \vert x_n - B \vert \tag{1}$$
Substituting the strict bounds gives
$$\vert A - B \vert < \varepsilon + \varepsilon = 2\varepsilon \tag{2}$$
By  of $\varepsilon$, the second step implies $\vert A - B \vert < \vert A - B \vert$, which is a contradiction. Consequently, the assumption that $A \neq B$ must be false, and the limit is unique. 

---
# Theorem 4
 Let $\{x_n\}$ be a sequence converging to a limit $A$. By setting $\varepsilon = 1$, the definition of convergence guarantees the existence of an index $N \in \mathbb{N}$ such that $\vert x_n - A \vert < 1$ for all $n > N$. Using the reverse Triangle Inequality, it follows that $\vert x_n \vert - \vert A \vert \le \vert x_n - A \vert < 1$, which implies $\vert x_n \vert < \vert A \vert + 1$ for all $n > N$. To bound the entire sequence, a maximum value $M$ must be defined as follows:  
$$M = \max(\vert x_1 \vert, \vert x_2 \vert, \dots, \vert x_N \vert, \vert A \vert + 1) \tag{3}$$
It is clear that $\vert x_n \vert \le M$ for all $n \in \mathbb{N}$. Thus, the sequence $\{x_n\}$ is bounded by the real number $M$. 
$$
\textbf{Q.E.D}
$$
