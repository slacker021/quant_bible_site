---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-rules-of-rational-expressions/","dg-note-properties":{}}
---

# Existence and Uniqueness of Positive $n$-th Roots
Let $a \in \mathbb{R}$ with $a > 0$, and let $n \in \mathbb{N}$. Define the subset $E \subset \mathbb{R}$ by

$$
\begin{gather}
E := \{t \in \mathbb{R} \mid t > 0 \ \wedge \ t^n < a\} \tag{1}
\end{gather}
$$

Verify that $E$ is nonempty and bounded above:
1. **Non-emptiness:** Set $t_0 := \frac{a}{1 + a}$. Because $a > 0$, there are $0 < t_0 < 1$ and $t_0 < a$. Since $0 < t_0 < 1$, induction on $n$ gives $t_0^n \le t_0 < a$, confirming that $t_0 \in E$ and $E \ne \emptyset$.
2. **Boundedness Above:** Set $M := 1 + a > 1$. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Bernoulli's Inequality\|Bernoulli's Inequality]], $(1 + a)^n \ge 1 + na > a$. For any $t \ge 1 + a$, monotonicity of $t \mapsto t^n$ on $\mathbb{R}_+$ implies $t^n \ge (1 + a)^n > a$, so $t \notin E$. Thus, $1 + a$ is an upper bound for $E$.

By the Least Upper Bound Axiom, $E$ possesses a supremum $s := \sup E > 0$ (since $s \ge t_0 > 0$). Note that for any $0 < u < v$, factoring $v^n - u^n$ gives
$$
\begin{gather}
v^n - u^n = (v - u)\left(v^{n-1} + v^{n-2}u + \dots + u^{n-1}\right) \le (v - u) n v^{n-1} \tag{2}
\end{gather}
$$

Evaluate $s^n$ relative to $a$ via trichotomy:
* **Suppose $s^n < a$:** Set $\Delta := a - s^n > 0$, and choose $\varepsilon \in \left]0, \min\left(1, \frac{\Delta}{n(s + 1)^{n-1}}\right)\right[$. Applying step 2 with $v = s + \varepsilon < s + 1$ and $u = s$ yields
  $$
  \begin{gather}
  (s + \varepsilon)^n - s^n \le \varepsilon n (s + \varepsilon)^{n-1} \le \varepsilon n (s + 1)^{n-1} < \Delta = a - s^n \implies (s + \varepsilon)^n < a \tag{3}
  \end{gather}
  $$
  Thus, $(s + \varepsilon) \in E$, contradicting $s = \sup E$.
* **Suppose $s^n > a$:** Set $\Delta := s^n - a > 0$, and choose $\varepsilon \in \left]0, \min\left(\frac{s}{2}, \frac{\Delta}{n s^{n-1}}\right)\right[$. Applying step 2 with $v = s$ and $u = s - \varepsilon > 0$ yields
  $$
  \begin{gather}
  s^n - (s - \varepsilon)^n \le \varepsilon n s^{n-1} < \Delta = s^n - a \implies (s - \varepsilon)^n > a \tag{4}
  \end{gather}
  $$
  For every $t \in E$, there is $t^n < a < (s - \varepsilon)^n \implies t < s - \varepsilon$, meaning $s - \varepsilon$ is an upper bound for $E$ strictly smaller than $s = \sup E$, a contradiction.

By trichotomy, $s^n = a$. Uniqueness in $\mathbb{R}_+$ follows from $0 < s_1 < s_2 \implies s_1^n < s_2^n$. This unique positive root is denoted $\sqrt[n]{a}$ or $a^{1/n}$.

---
# Algebraic Laws of Radicals and Rational Exponents
Let $a, b > 0$ and $m, n \in \mathbb{N}$:
1. **Product and Nested Radical Rules:** Set $x := a^{1/n}$ and $y := b^{1/n}$, so $x^n = a$ and $y^n = b$. By commutativity and associativity of multiplication in $\mathbb{R}$, $(xy)^n = x^n y^n = ab$. By uniqueness of the positive $n$-th root of $ab$,
   $$
   \begin{gather}
   \sqrt[n]{ab} = (ab)^{1/n} = xy = a^{1/n} b^{1/n} = \sqrt[n]{a} \cdot \sqrt[n]{b} \tag{5}
   \end{gather}
   $$
   Similarly, setting $z := (a^{1/m})^{1/n} > 0$ gives $z^{nm} = (z^n)^m = a^{1/m \cdot m} = a$, which by uniqueness of the $(nm)$-th root yields $\sqrt[n]{\sqrt[m]{a}} = \sqrt[nm]{a}$.
2. **Consistency of Rational Exponents:** For $m \in \mathbb{Z}$ and $n \in \mathbb{N}$, raising $x = a^{1/n}$ to the $m$-th power gives $((a^{1/n})^m)^n = ((a^{1/n})^n)^m = a^m$, so $(a^{1/n})^m = (a^m)^{1/n} =: a^{m/n}$. Moreover, for any $k \in \mathbb{N}$,
   $$
   \begin{gather}
   a^{(km)/(kn)} = \left(a^{1/(kn)}\right)^{km} = \left(\left(a^{1/n}\right)^{1/k}\right)^{km} = \left(\left(\left(a^{1/n}\right)^{1/k}\right)^k\right)^m = \left(a^{1/n}\right)^m = a^{m/n} \tag{6}
   \end{gather}
   $$
   confirming that $a^r$ is well-defined for any $r \in \mathbb{Q}$ independent of the fraction representation.
3. **Laws of Rational Exponents:** Given $r_1, r_2 \in \mathbb{Q}$, express them over a common positive denominator $n \in \mathbb{N}$ as $r_1 = m_1/n$ and $r_2 = m_2/n$ with $m_1, m_2 \in \mathbb{Z}$. Using the integer exponent laws on base $c := a^{1/n}$ yields
   $$
   \begin{gather}
   a^{r_1} \cdot a^{r_2} = c^{m_1} \cdot c^{m_2} = c^{m_1 + m_2} = a^{(m_1 + m_2)/n} = a^{r_1 + r_2} \tag{7}
   \end{gather}
   $$
   Furthermore, writing $r_1 = m_1/n_1$ and $r_2 = m_2/n_2$ gives
   $$
   \begin{gather}
   \left(a^{r_1}\right)^{r_2} = \left(\left(a^{m_1}\right)^{1/n_1}\right)^{m_2/n_2} = \left(\left(a^{m_1 m_2}\right)^{1/n_1}\right)^{1/n_2} = \left(a^{m_1 m_2}\right)^{1/(n_1 n_2)} = a^{r_1 r_2} \tag{8}
   \end{gather}
   $$
   and by step 5, $(ab)^{r_1} = \left((ab)^{1/n_1}\right)^{m_1} = \left(a^{1/n_1} b^{1/n_1}\right)^{m_1} = a^{r_1} b^{r_1}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$