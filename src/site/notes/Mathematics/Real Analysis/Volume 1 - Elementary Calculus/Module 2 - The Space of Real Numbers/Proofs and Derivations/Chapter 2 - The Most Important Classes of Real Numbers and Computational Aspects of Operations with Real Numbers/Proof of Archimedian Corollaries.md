---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-archimedian-corollaries/","dg-note-properties":{}}
---

# Proposition 1
Let $\varepsilon > 0$ be an arbitrary positive real number. Applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Principle of Archimedes\|Principle of Archimedes]] with step size $h = \varepsilon > 0$ and target value $x = 1$ guarantees the existence of an integer $n \in \mathbb{Z}$ such that
$$
\begin{gather}
(n - 1)\varepsilon \le 1 < n\varepsilon \tag{1}
\end{gather}
$$

Because $1 > 0$ and $\varepsilon > 0$, the inequality $n\varepsilon > 1 > 0$ implies $n > 0$. Since $n \in \mathbb{Z}$ and $n > 0$, it follows that $n \in \mathbb{N}$. Dividing $0 < 1 < n\varepsilon$ by $n > 0$ yields
$$
\begin{gather}
0 < \frac{1}{n} < \varepsilon \tag{2}
\end{gather}
$$

---
# Proposition 2
Let $x \in \mathbb{R}$ satisfy $x \ge 0$ and $x < 1/n$ for all $n \in \mathbb{N}$. Suppose, for the sake of contradiction, that $x > 0$. Applying Proposition 1 with $\varepsilon = x > 0$ guarantees the existence of a natural number $n_0 \in \mathbb{N}$ such that
$$
\begin{gather}
0 < \frac{1}{n_0} < x \tag{3}
\end{gather}
$$

Equation 3 directly contradicts the hypothesis that $x < 1/n$ for all $n \in \mathbb{N}$. Since $x \ge 0$ and $x > 0$ is impossible, it follows that $x = 0$.

---
# Proposition 3
Let $a, b \in \mathbb{R}$ satisfy $a < b$, so that the interval length $b - a > 0$ is strictly positive. By Proposition 1 applied to $\varepsilon = b - a > 0$, there exists a natural number $n \in \mathbb{N}$ such that
$$
\begin{gather}
0 < \frac{1}{n} < b - a \tag{4}
\end{gather}
$$

Next, applying the Principle of Archimedes with step size $h = \frac{1}{n} > 0$ to the real number $a$ yields a unique integer $m \in \mathbb{Z}$ satisfying
$$
\begin{gather}
\frac{m - 1}{n} \le a < \frac{m}{n} \tag{5}
\end{gather}
$$

To verify that the rational number $r := \frac{m}{n} \in \mathbb{Q}$ also satisfies $r < b$, observe from the left-hand inequality of step 5 and the step bound in step 4 that
$$
\begin{gather}
\frac{m}{n} = \frac{m - 1}{n} + \frac{1}{n} \le a + \frac{1}{n} < a + (b - a) = b \tag{6}
\end{gather}
$$
Combining step 5 and step 6 confirms that $r = \frac{m}{n} \in \mathbb{Q}$ satisfies $a < r < b$.

---
# Proposition 4
Let $x \in \mathbb{R}$ be arbitrary. Applying the Principle of Archimedes with unit step size $h = 1 > 0$ yields a unique integer $m \in \mathbb{Z}$ such that
$$
\begin{gather}
m - 1 \le x < m \tag{7}
\end{gather}
$$

Defining $k := m - 1 \in \mathbb{Z}$ transforms step 7 into the unique bracket
$$
\begin{gather}
k \le x < k + 1 \tag{8}
\end{gather}
$$
Denoting this unique integer by $[x] := k$ (the integer part of $x$) and setting $\{x\} := x - [x]$ (the fractional part of $x$), subtracting $k = [x]$ across step 8 yields $0 \le \{x\} < 1$ with $x = [x] + \{x\}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$