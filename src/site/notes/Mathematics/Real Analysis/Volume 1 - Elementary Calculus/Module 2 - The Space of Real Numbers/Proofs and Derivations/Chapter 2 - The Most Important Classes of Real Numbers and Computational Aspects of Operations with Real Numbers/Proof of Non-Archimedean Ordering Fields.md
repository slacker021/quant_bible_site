---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-non-archimedean-ordering-fields/","dg-note-properties":{}}
---

Let $\mathbb{Q}(x)$ denote the field of rational functions (the field of fractions of the polynomial ring $\mathbb{Q}[x]$). Every non-zero rational function $R(x) \in \mathbb{Q}(x)$ can be expressed in reduced form as the quotient of two polynomials $P(x), Q(x) \in \mathbb{Q}[x]$:
$$
\begin{gather}
R(x) = \frac{P(x)}{Q(x)} = \frac{a_m x^m + a_{m-1} x^{m-1} + \dots + a_0}{b_n x^n + b_{n-1} x^{n-1} + \dots + b_0} \tag{1}
\end{gather}
$$

where $a_m \ne 0$ and $b_n \ne 0$ are the leading rational coefficients of $P$ and $Q$, respectively. Define the positivity cone $\mathcal{P} \subset \mathbb{Q}(x)$ by declaring a non-zero element $R(x)$ to be strictly positive ($R(x) > 0$) if and only if the product of its leading coefficients is positive in $\mathbb{Q}$:
$$
\begin{gather}
R(x) > 0 \iff a_m \cdot b_n > 0 \tag{2}
\end{gather}
$$

Note that step 2 is invariant under multiplying $P(x)$ and $Q(x)$ by any non-zero polynomial $H(x) = c_k x^k + \dots + c_0$, because the new leading coefficient product is $(a_m c_k)(b_n c_k) = (a_m b_n) c_k^2$, which has the exact same sign as $a_m b_n$ since $c_k^2 > 0$. Defining the order relation by $R_1 < R_2 \iff R_2 - R_1 > 0$, one verifies the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|ordered field axioms]]:

1. **Trichotomy:** For any $R(x) \in \mathbb{Q}(x)$, either $P(x) = 0$ (so $R(x) = 0$), or $a_m b_n > 0$ (so $R(x) > 0$), or $a_m b_n < 0$ (so $-R(x) > 0$). Exactly one of these three conditions holds.
2. **Closure Under Addition:** Let $R_1 = P_1/Q_1 > 0$ and $R_2 = P_2/Q_2 > 0$. Without loss of generality, scale the fractions so that both denominators have positive leading coefficients ($b_{n_1}^{(1)} > 0$ and $b_{n_2}^{(2)} > 0$), which by step 2 implies both numerators also have positive leading coefficients ($a_{m_1}^{(1)} > 0$ and $a_{m_2}^{(2)} > 0$). In the sum$$
   \begin{gather}
   R_1 + R_2 = \frac{P_1 Q_2 + P_2 Q_1}{Q_1 Q_2} \tag{3}
   \end{gather}
   $$
   the denominator $Q_1 Q_2$ has positive leading coefficient $b_{n_1}^{(1)} b_{n_2}^{(2)} > 0$, and the numerator $P_1 Q_2 + P_2 Q_1$ has leading coefficient equal to $a_{m_1}^{(1)} b_{n_2}^{(2)} > 0$ (if $m_1 + n_2 > m_2 + n_1$), $a_{m_2}^{(2)} b_{n_1}^{(1)} > 0$ (if $m_2 + n_1 > m_1 + n_2$), or their positive sum $a_{m_1}^{(1)} b_{n_2}^{(2)} + a_{m_2}^{(2)} b_{n_1}^{(1)} > 0$ (if $m_1 + n_2 = m_2 + n_1$). Thus, $R_1 + R_2 > 0$.
3. **Closure Under Multiplication:** For $R_1 > 0$ and $R_2 > 0$, the product$$
   \begin{gather}
   R_1 \cdot R_2 = \frac{P_1 P_2}{Q_1 Q_2} \tag{4}
   \end{gather}
   $$
   has leading coefficient product $(a_{m_1}^{(1)} a_{m_2}^{(2)})(b_{n_1}^{(1)} b_{n_2}^{(2)}) = (a_{m_1}^{(1)} b_{n_1}^{(1)})(a_{m_2}^{(2)} b_{n_2}^{(2)}) > 0$, so $R_1 \cdot R_2 > 0$.

Therefore, $(\mathbb{Q}(x), +, \cdot, \le)$ is a linearly ordered field.

To prove that $\mathbb{Q}(x)$ is *non-Archimedean*, compare the multiplicative identity $1 = \frac{1}{1} > 0$ and the indeterminate $x = \frac{1 \cdot x + 0}{1} > 0$. For any natural number $k \in \mathbb{N}$, consider the difference between $x$ and $k \cdot 1 = \frac{k}{1}$:
$$
\begin{gather}
x - k \cdot 1 = \frac{1 \cdot x - k}{1} \tag{5}
\end{gather}
$$

In step 5, the numerator polynomial $P(x) = x - k$ has degree $1$ with leading coefficient $a_1 = 1 > 0$, and the denominator $Q(x) = 1$ has degree $0$ with leading coefficient $b_0 = 1 > 0$. Because $a_1 \cdot b_0 = 1 \cdot 1 = 1 > 0$, step 2 dictates that
$$
\begin{gather}
x - k \cdot 1 > 0 \iff k \cdot 1 < x \quad \forall k \in \mathbb{N} \tag{6}
\end{gather}
$$
Because no integer multiple of the unit $1$ can ever exceed $x$ (and equivalently, $0 < \frac{1}{x} < \frac{1}{k}$ for all $k \in \mathbb{N}$, making $\frac{1}{x}$ a positive infinitesimal), the Principle of Archimedes fails in $\mathbb{Q}(x)$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$