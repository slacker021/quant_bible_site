---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-rules-of-rational-expressions/","dg-note-properties":{}}
---

Let $a \in \mathbb{R}$ with $a > 0$, and let $n \in \mathbb{N}$. Consider the set
$$E = \{ t \in \mathbb{R} \mid t > 0 \wedge t^n < a \} \tag{1}$$
Two bits of information can be inferred from this:
1. **Non-emptiness:** Let $t_0 = \frac{a}{1 + a}$. Since $0 < t_0 < 1$, it follows that $t_0^n \le t_0 < a$. Thus, $t_0 \in E$, so $E \ne \emptyset$.
2. **Boundedness Above:** Consider $1 + a$. By Bernoulli's inequality, $(1 + a)^n \ge 1 + na > a$. If $t \ge 1 + a$, then $t^n \ge (1 + a)^n > a$, meaning $t \notin E$. Thus, $1 + a$ is an upper bound for $E$.
By the least upper bound principle, the supremum exists:  
$$s = \sup E \tag{2}$$
Now evaluate $s^n$ relative to $a$, which leads to two cases: 
- **Assume** $s^n < a$**:** Let $\Delta = a - s^n > 0$. For any $\epsilon \in (0, 1)$, using the binomial expansion:  $$(s + \epsilon)^n = s^n + \sum_{k=1}^n \binom{n}{k} s^{n-k} \epsilon^k \le s^n + \epsilon \sum_{k=1}^n \binom{n}{k} s^{n-k} = s^n + \epsilon C \tag{3}$$where $C = (s + 1)^n - s^n > 0$. Choosing $\epsilon < \min\left(1, \frac{\Delta}{C}\right)$ yields $(s + \epsilon)^n < s^n + \Delta = a$. This implies $(s + \epsilon) \in E$, contradicting that $s$ is an upper bound.
- **Assume** $s^n > a$**:** Let $\Delta = s^n - a > 0$. By a symmetric expansion, choosing $\epsilon > 0$ sufficiently small yields $(s - \epsilon)^n > a$, implying that $s - \epsilon$ is an upper bound of $E$ smaller than $s$, contradicting that $s = \sup E$.

By trichotomy, the only valid conclusion is
$$s^n = a \tag{4}$$
This real number $s$ is denoted by $\sqrt[n]{a}$ or $a^{1/n}$. Uniqueness follows because $0 < s_1 < s_2 \implies s_1^n < s_2^n$.

Next, let $a, b > 0$ and $m, n \in \mathbb{N}$.
1. **Product Rule:** Let $x = a^{1/n}$ and $y = b^{1/n}$. By definition, $x^n = a$ and $y^n = b$. By the commutativity and associativity of multiplication:  $$(xy)^n = x^n y^n = ab \tag{5}$$By the uniqueness of the $n$-th root of $ab$: $$(ab)^{1/n} = xy = a^{1/n} b^{1/n} \tag{6}$$
2. **Nested Roots:** Let $z = (a^{1/m})^{1/n}$. Then $(z^n)^m = a$. By integer power laws, $z^{mn} = a$. By uniqueness:  $$\sqrt[n]{\sqrt[m]{a}} = \sqrt[mn]{a} \tag{7}$$

For $r = m/n \in \mathbb{Q}$ with $n \in \mathbb{N}$ and $m \in \mathbb{Z}$, define
$$a^{m/n} := (a^{1/n})^m \tag{8}$$
To verify that this definition is independent of the fraction representation, let $m/n = (km)/(kn)$ for $k \in \mathbb{N}$:  
$$(a^{km})^{1/(kn)} = \left(((a^{1/n})^{1/k})^{km}\right) = ((a^{1/n})^m)^{k \cdot (1/k)} = (a^{1/n})^m \tag{9}$$
Let $r_1 = \frac{m_1}{n}$ and $r_2 = \frac{m_2}{n}$ with a common denominator $n \in \mathbb{N}$. Then:  
$$a^{r_1} \cdot a^{r_2} = (a^{1/n})^{m_1} \cdot (a^{1/n})^{m_2} = (a^{1/n})^{m_1 + m_2} = a^{(m_1 + m_2)/n} = a^{r_1 + r_2} \tag{10}$$
Similarly, applying the composition of roots yields:  
$$(a^{r_1})^{r_2} = a^{r_1 r_2} \tag{11}$$$$\textbf{Q.E.D}$$