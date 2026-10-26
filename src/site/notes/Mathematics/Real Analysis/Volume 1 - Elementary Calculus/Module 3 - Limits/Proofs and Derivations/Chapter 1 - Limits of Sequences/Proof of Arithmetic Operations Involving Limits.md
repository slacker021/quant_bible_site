---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-arithmetic-operations-involving-limits/","dg-note-properties":{}}
---

Let $\{x_n\}$ and $\{y_n\}$ be two convergent sequences of real numbers such that $\lim_{n \to \infty} x_n = A$ and $\lim_{n \to \infty} y_n = B$.

# Theorem 1
Let $\varepsilon > 0$ be arbitrary. By the definition of sequence convergence applied to the positive tolerance $\frac{\varepsilon}{2} > 0$, there exists an index $N_1 \in \mathbb{N}$ such that $|x_n - A| < \frac{\varepsilon}{2}$ for all $n > N_1$, and there exists an index $N_2 \in \mathbb{N}$ such that $|y_n - B| < \frac{\varepsilon}{2}$ for all $n > N_2$.

Set $N := \max(N_1, N_2) \in \mathbb{N}$. For all $n > N$, applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] yields
$$
\begin{gather}
|(x_n + y_n) - (A + B)| = |(x_n - A) + (y_n - B)| \le |x_n - A| + |y_n - B| \tag{1}
\end{gather}
$$
Substituting the error bounds for $n > N$ into step 1 gives
$$
\begin{gather}
|(x_n + y_n) - (A + B)| < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{2}
\end{gather}
$$
Thus, $\lim_{n \to \infty} (x_n + y_n) = A + B$.

---
# Theorem 2
Because $\{x_n\}$ is convergent, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|basic properties of limits]] guarantee that $\{x_n\}$ is bounded: there exists a real number $M > 0$ such that $|x_n| \le M$ for all $n \in \mathbb{N}$. Let $\varepsilon > 0$ be arbitrary. Adding and subtracting the intermediate term $x_n B$ and applying the Triangle Inequality gives
$$
\begin{gather}
|x_n y_n - A B| = |x_n(y_n - B) + B(x_n - A)| \le |x_n||y_n - B| + |B||x_n - A| \tag{3}
\end{gather}
$$
Using the bound $|x_n| \le M$, step 3 becomes
$$
\begin{gather}
|x_n y_n - A B| \le M |y_n - B| + |B| |x_n - A| \tag{4}
\end{gather}
$$
By the convergence of $\{y_n\}$ and $\{x_n\}$, there exists an index $N_1 \in \mathbb{N}$ such that $|y_n - B| < \frac{\varepsilon}{2M}$ for all $n > N_1$, and there exists an index $N_2 \in \mathbb{N}$ such that $|x_n - A| < \frac{\varepsilon}{2(|B| + 1)}$ for all $n > N_2$ (where $|B| + 1 > 0$ prevents division by zero when $B = 0$). Setting $N := \max(N_1, N_2) \in \mathbb{N}$, it holds for all $n > N$ that
$$
\begin{gather}
|x_n y_n - A B| < M \left( \frac{\varepsilon}{2M} \right) + |B| \left( \frac{\varepsilon}{2(|B| + 1)} \right) < \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon \tag{5}
\end{gather}
$$
Thus, $\lim_{n \to \infty} (x_n \cdot y_n) = A \cdot B$.

---
# Theorem 3
Assume $B \neq 0$ and $y_n \neq 0$ for all $n \in \mathbb{N}$. It suffices to prove that $\lim_{n \to \infty} \frac{1}{y_n} = \frac{1}{B}$, as the quotient rule then follows immediately by applying Theorem 2 to the product $x_n \cdot \frac{1}{y_n}$.

Because $|B| > 0$, applying the definition of $\lim_{n \to \infty} y_n = B$ to the tolerance $\frac{|B|}{2} > 0$ yields an index $N_1 \in \mathbb{N}$ such that $|y_n - B| < \frac{|B|}{2}$ for all $n > N_1$. By the reverse triangle inequality, for all $n > N_1$:
$$
\begin{gather}
|y_n| = |B - (B - y_n)| \ge |B| - |y_n - B| > |B| - \frac{|B|}{2} = \frac{|B|}{2} \implies \frac{1}{|y_n|} < \frac{2}{|B|} \tag{6}
\end{gather}
$$
Now let $\varepsilon > 0$ be arbitrary. There exists an index $N_2 \in \mathbb{N}$ such that $|y_n - B| < \frac{\varepsilon |B|^2}{2}$ for all $n > N_2$. Setting $N := \max(N_1, N_2) \in \mathbb{N}$, it follows from step 6 that for all $n > N$:
$$
\begin{gather}
\left| \frac{1}{y_n} - \frac{1}{B} \right| = \frac{|B - y_n|}{|y_n| |B|} < \frac{2}{|B|^2} |y_n - B| < \frac{2}{|B|^2} \left( \frac{\varepsilon |B|^2}{2} \right) = \varepsilon \tag{7}
\end{gather}
$$
Thus, $\lim_{n \to \infty} \frac{1}{y_n} = \frac{1}{B}$, and applying Theorem 2 yields $\lim_{n \to \infty} \frac{x_n}{y_n} = \frac{A}{B}$.

---
# Theorem 4
Let $c \in \mathbb{R}$ be a real constant. Note that this property is a special case of Theorem 2 obtained by taking $\{y_n\}$ to be the constant sequence $y_n = c$; it can also be verified directly from the definition of a limit by considering two cases for $c$:

### Case 1
Suppose $c = 0$. Then $c x_n = 0$ for all $n \in \mathbb{N}$ and $c A = 0$. Because the constant sequence $\{0\}$ converges to $0$ by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|basic properties of limits]], $\lim_{n \to \infty} (0 \cdot x_n) = 0 = 0 \cdot A$.

### Case 2
Suppose $c \neq 0$, so that $|c| > 0$, and let $\varepsilon > 0$ be arbitrary. Because $\frac{\varepsilon}{|c|} > 0$ and $\lim_{n \to \infty} x_n = A$, there exists an index $N \in \mathbb{N}$ such that for all $n > N$:
$$
\begin{gather}
|x_{n} - A| < \frac{\varepsilon}{|c|} \tag{8}
\end{gather}
$$
Multiplying both sides of step 8 by $|c| > 0$ yields, for all $n > N$:
$$
\begin{gather}
|c x_{n} - c A| = |c||x_{n} - A| < |c| \left(\frac{\varepsilon}{|c|} \right) = \varepsilon \tag{9}
\end{gather}
$$
Thus, $\lim_{n \to \infty} (c x_n) = c A$.

---
# Theorem 5
First, consider a positive integer exponent $p \in \mathbb{N}$. If $p = 1$, the statement $\lim_{n \to \infty} x_n^1 = A^1$ holds by hypothesis. Suppose $p \ge 2$, and let $\varepsilon > 0$ be arbitrary. Because $\lim_{n \to \infty} x_n = A$, there exists an index $N_1 \in \mathbb{N}$ such that $|x_n - A| < 1$ for all $n > N_1$, which implies
$$
\begin{gather}
|x_{n}| \le |x_{n} - A| + |A| < 1 + |A| =: M \quad \forall n > N_1 \tag{10}
\end{gather}
$$
For any real numbers $x, y \in \mathbb{R}$ satisfying $|x| \le M$ and $|y| \le M$, the algebraic factorization of $x^p - y^p$ and the Triangle Inequality yield
$$
\begin{gather}
|x^p - y^p| = |x - y| \left| \sum_{k=0}^{p - 1} x^k y^{p-1-k} \right| \le |x - y| \sum_{k=0}^{p - 1} |x|^k |y|^{p-1-k} \le |x - y| p M^{p-1} \tag{11}
\end{gather}
$$
Setting $x = x_n$, $y = A$, and $M = 1 + |A| > 0$ in step 11 shows that for all $n > N_1$:
$$
\begin{gather}
|x_{n}^p - A^p| \le |x_{n} - A| p(1 + |A|)^{p-1} \tag{12}
\end{gather}
$$
Choose an index $N_2 \in \mathbb{N}$ such that for all $n > N_2$:
$$
\begin{gather}
|x_{n} - A| < \frac{\varepsilon}{p(1 + |A|)^{p-1}} \tag{13}
\end{gather}
$$
Then for all $n > N := \max(N_1, N_2)$, combining step 12 and step 13 produces
$$
\begin{gather}
|x_{n}^p - A^p| < \varepsilon \tag{14}
\end{gather}
$$
For a general real exponent $p \in \mathbb{R}$ with $x_n > 0$ and $A > 0$, note that if $p = 0$, then $x_n^0 = 1 = A^0$. If $p \neq 0$, let $\varepsilon > 0$ be arbitrary. Because $\lim_{n \to \infty} \frac{x_n}{A} = 1$ by Theorem 3, it suffices to show that $\lim_{n \to \infty} z_n^p = 1$ where $z_n := \frac{x_n}{A} > 0$. By the [[Corollary of the Weierstrass Theorem\|asymptotics of n-th roots]], $\lim_{k \to \infty} 2^{|p|/k} = 1$ and $\lim_{k \to \infty} 2^{-|p|/k} = 1$, so there exists $k \in \mathbb{N}$ such that
$$
\begin{gather}
1 - \frac{\varepsilon}{A^p} < 2^{-\frac{|p|}{k}} < 1 < 2^{\frac{|p|}{k}} < 1 + \frac{\varepsilon}{A^p} \tag{15}
\end{gather}
$$
Since $\lim_{n \to \infty} z_n = 1$ and $2^{-1/k} < 1 < 2^{1/k}$, there exists $N \in \mathbb{N}$ such that $2^{-1/k} < z_n < 2^{1/k}$ for all $n > N$. Raising this inequality to the power $p$ (which either preserves or reverses the outer bounds depending on the sign of $p$) and applying step 15 yields, for all $n > N$:
$$
\begin{gather}
1 - \frac{\varepsilon}{A^p} < z_n^p < 1 + \frac{\varepsilon}{A^p} \implies |x_n^p - A^p| = A^p |z_n^p - 1| < \varepsilon \tag{16}
\end{gather}
$$
Thus, $\lim_{n \to \infty} x_n^p = A^p$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
