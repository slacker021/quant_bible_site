---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-the-square-root-of-2-is-irrational/","dg-note-properties":{}}
---

# Existence and Uniqueness
Define two subsets $X$ and $Y$ of the positive real numbers $\mathbb{R}_+$ as follows:
$$
\begin{gather}
X := \{x \in \mathbb{R}_+ \mid x^2 < 2\} \quad \text{and} \quad Y := \{y \in \mathbb{R}_+ \mid 2 < y^2\} \tag{1}
\end{gather}
$$

Because $1^2 = 1 < 2$ and $2^2 = 4 > 2$, we have $1 \in X$ and $2 \in Y$, ensuring that both $X$ and $Y$ are nonempty. Furthermore, for any $x, y \in \mathbb{R}_+$, the identity $y^2 - x^2 = (y - x)(y + x)$ with $y + x > 0$ implies
$$
\begin{gather}
(x < y) \iff (x^2 < y^2) \tag{2}
\end{gather}
$$

Consequently, for every $x \in X$ and every $y \in Y$, the inequality $x^2 < 2 < y^2$ forces $x < y$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|Axiom of Completeness]], there exists a separating real number $s \in \mathbb{R}$ such that
$$
\begin{gather}
x \le s \le y \quad \forall x \in X, \ \forall y \in Y \tag{3}
\end{gather}
$$

Since $1 \in X$ and $2 \in Y$, it follows that $1 \le s \le 2$, so $s > 0$. By trichotomy, either $s^2 < 2$, $s^2 > 2$, or $s^2 = 2$:
1. **Suppose $s^2 < 2$:** Define $\Delta := 2 - s^2 > 0$. Since $s \ge 1$,  $3s \ge 3$ and $\Delta = 2 - s^2 \le 1$, which implies $0 < \frac{\Delta}{3s} < 1$. Consider the perturbed value $s + \frac{\Delta}{3s} > s$. Squaring this quantity and using the bounds $\frac{\Delta}{3s} < 1$ and $s \ge 1$ (so $\frac{1}{3s} \le \frac{1}{3}$) yields
   $$
   \begin{gather}
   \left(s + \frac{\Delta}{3s}\right)^2 = s^2 + \frac{2\Delta}{3} + \left(\frac{\Delta}{3s}\right)^2 < s^2 + \frac{2\Delta}{3} + \frac{\Delta}{3s} \le s^2 + \frac{2\Delta}{3} + \frac{\Delta}{3} = s^2 + \Delta = 2 \tag{4}
   \end{gather}
   $$
   Thus, $s + \frac{\Delta}{3s} \in X$, which contradicts step 3 because $s + \frac{\Delta}{3s} > s$ whereas $x \le s$ for all $x \in X$.
2. **Suppose $s^2 > 2$:** Define $\Delta := s^2 - 2 > 0$. Since $1 \le s \le 2$, one should have $0 < \frac{\Delta}{3s} < s$, so $s - \frac{\Delta}{3s} > 0$. Squaring $s - \frac{\Delta}{3s}$ and dropping the positive squared term $\left(\frac{\Delta}{3s}\right)^2 > 0$ yields
   $$
   \begin{gather}
   \left(s - \frac{\Delta}{3s}\right)^2 = s^2 - \frac{2\Delta}{3} + \left(\frac{\Delta}{3s}\right)^2 > s^2 - \frac{2\Delta}{3} > s^2 - \Delta = 2 \tag{5}
   \end{gather}
   $$
   Thus, $s - \frac{\Delta}{3s} \in Y$, which contradicts step 3 because $s - \frac{\Delta}{3s} < s$ whereas $s \le y$ for all $y \in Y$.

By trichotomy, the only remaining possibility is $s^2 = 2$. Uniqueness in $\mathbb{R}_+$ follows immediately from step 2, as $0 < s_1 < s_2 \implies s_1^2 < s_2^2$. This unique positive real number is denoted $\sqrt{2}$.

---
# Irrationality of $\sqrt{2}$
Suppose, for the sake of contradiction, that $s = \sqrt{2} \in \mathbb{Q}$. Then $s$ can be represented as a reduced fraction $s = m/n$, where $m, n \in \mathbb{N}$ are relatively prime ($\gcd(m, n) = 1$). Squaring both sides of $s = m/n$ gives
$$
\begin{gather}
s^2 = \frac{m^2}{n^2} = 2 \implies m^2 = 2 n^2 \tag{6}
\end{gather}
$$
Equation 6 demonstrates that the prime number $2$ divides $m^2 = m \cdot m$. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Fundamental Theorem of Arithmetic\|Euclid's Lemma]], $2$ must divide $m$, so there exists a natural number $k \in \mathbb{N}$ such that $m = 2k$. Substituting $m = 2k$ into step 6 yields
$$
\begin{gather}
(2k)^2 = 4k^2 = 2n^2 \implies n^2 = 2k^2 \tag{7}
\end{gather}
$$
By the same reasoning applied to step 7, the prime $2$ divides $n^2$, which by Euclid's Lemma forces $2 \mid n$. However, having $2 \mid m$ and $2 \mid n$ means $2$ is a common divisor of $m$ and $n$, contradicting the premise that $\gcd(m, n) = 1$. Therefore, $\sqrt{2} \notin \mathbb{Q}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$