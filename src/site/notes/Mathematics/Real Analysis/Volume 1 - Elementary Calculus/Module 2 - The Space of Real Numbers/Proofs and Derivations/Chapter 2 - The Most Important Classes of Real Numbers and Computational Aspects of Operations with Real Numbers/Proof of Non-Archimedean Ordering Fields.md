---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-non-archimedean-ordering-fields/","dg-note-properties":{}}
---

Let $\mathbb{Q}(x)$ denote the field of fractions of the polynomial ring $\mathbb{Q}[x]$. Any non-zero rational function $R(x) \in \mathbb{Q}(x)$ can be uniquely written in reduced form as:  
$$R(x) = \frac{P(x)}{Q(x)} = \frac{a_m x^m + a_{m-1}x^{m-1} + \dots + a_0}{b_n x^n + b_{n-1}x^{n-1} + \dots + b_0} \tag{1}$$
where $a_m \ne 0$, $b_n \ne 0$, and $Q(x)$ is monic ($b_n > 0$).

The positivity cone $P \subset \mathbb{Q}(x)$ is defined by the sign of the leading coefficient of $P(x)$:  
$$R(x) > 0 \iff a_m \cdot b_n > 0 \tag{2}$$
For two arbitrary elements $R_1, R_2 \in \mathbb{Q}(x)$, the ordering is defined by $R_1 < R_2 \iff R_2 - R_1 > 0$.

Now, it's critical to verify the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Order Axioms\|ordered field axioms]]: 
1. **Trichotomy:** For any $R(x) = P(x)/Q(x)$, either $P(x) = 0$ (so $R = 0$), the leading coefficient product $a_m b_n > 0$ (so $R > 0$), or $a_m b_n < 0$ (so $-R > 0$). Exactly one condition holds.
2. **Closure under Addition:** Let $R_1 = P_1/Q_1 > 0$ and $R_2 = P_2/Q_2 > 0$ with positive leading coefficients. The sum is: $$R_1 + R_2 = \frac{P_1 Q_2 + P_2 Q_1}{Q_1 Q_2} \tag{3}$$The leading coefficient of the numerator is a sum of positive products or dominated by the higher-degree term, ensuring the leading coefficient of the sum remains positive.
3. **Closure under Multiplication:** The product is:  $$R_1 \cdot R_2 = \frac{P_1 P_2}{Q_1 Q_2} \tag{4}$$The leading coefficient of $P_1 P_2$ is the product of the leading coefficients of $P_1$ and $P_2$. Since both are positive, their product is positive. Hence, $R_1 \cdot R_2 > 0$.

Thus, $(\mathbb{Q}(x), +, \cdot, <)$ is a linearly ordered field.

Lastly, the Archimedean property asserts that for any positive elements $A, B$ in an ordered field, there exists $k \in \mathbb{N}$ such that $k \cdot A > B$. With that specified, let $A = 1$ and $B = x$. Under the order definition: 
- The element $1 = \frac{1}{1}$ has leading coefficients $1$ and $1$, so $1 \cdot 1 = 1 > 0$, meaning $1 > 0$.
- The element $x = \frac{1 \cdot x + 0}{1}$ has leading coefficients $1$ and $1$, so $x > 0$.
Furthermore, let $k \in \mathbb{N}$ be an arbitrary natural number. The standard natural number embedding is represented by the constant rational function $k = \frac{k}{1}$. Consider the difference
$$x - k \cdot 1 = \frac{x - k}{1} \tag{5}$$
The numerator polynomial $P(x) = x - k$ has degree $1$ with leading coefficient $a_1 = 1$. The denominator $Q(x) = 1$ has degree $0$ with leading coefficient $b_0 = 1$. Evaluating the positivity condition:  
$$a_1 \cdot b_0 = 1 \cdot 1 = 1 > 0 \tag{6}$$
By definition of the ordering:  
$$x - k > 0 \implies k \cdot 1 < x \tag{7}$$
Because the inequality in step 7 holds for every natural number $k \in \mathbb{N}$, no natural multiple of the unit element $1$ can ever exceed $x$.

Therefore, the field $\mathbb{Q}(x)$ is non-Archimedean.
$$\textbf{Q.E.D}$$