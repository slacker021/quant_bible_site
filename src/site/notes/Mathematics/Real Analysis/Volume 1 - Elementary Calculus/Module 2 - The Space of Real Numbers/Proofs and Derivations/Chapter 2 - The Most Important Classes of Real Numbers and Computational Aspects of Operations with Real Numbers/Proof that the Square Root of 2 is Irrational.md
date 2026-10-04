---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-the-square-root-of-2-is-irrational/","dg-note-properties":{}}
---

Let $X$ and $Y$ be the sets of positive real numbers such that $\forall x \in X (x^{2} <2), \forall y \in Y (2 < y^{2})$. Since $1 \in X$ and $2 \in Y$, it follows that $X$ and $Y$ are nonempty sets. Furthermore, since 
$$
(x < y) \iff (x^2 < y^2) \tag{1}
$$
for positive numbers $x$ and $y$, every element of $X$ is less than every element of $Y$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|completeness axiom]] there's a $s \in \mathbb{R}$ such that $x \le s \le y$ for all $x \in X$ and $y \in Y$. 

If $s^2 < 2$, then, for example, the number $s + \frac{2 - s^2}{3s}$, which is larger than $s$, would have a square that's less than $2$. Indeed, it's known that $1 \in X$, so that $1^2 \le s^2 < 2$, and $0 < \Delta := 2 - s^2 \le 1$. Therefore, it follows that 
$$
\left(s - \frac{\Delta}{3s} \right)^2 = s^2 - 2 \cdot \frac{\Delta}{3s} + \left( \frac{\Delta}{3s}\right)^2 < s^2 + 3 \cdot \frac{\Delta}{3s} < s^2 + 3 \cdot \frac{\Delta}{3s} = s^2 + \Delta = 2. \tag{2}
$$
Consequently, $\left( s + \frac{\Delta}{3s} \right) \in X$, which is inconsistent with the inequality $x \ne s$ for all $x \in X$. 

If $2 < s^2$, then the number $s - \frac{s^2 - 2}{3s}$, which is smaller than $s$, would have a square larger than $2$. It's already known that $2 \in Y$, so that $2 < s^2 \le 2^2$ or $0 < \Delta:= s^2 - 2 < 3$ and $0 < \frac{\Delta}{3} < 1$. Hence, 
$$
\left(s - \frac{\Delta}{3s} \right)^2 = s^2 - 2 \cdot \frac{\Delta}{3s} + \left( \frac{\Delta}{3s}\right)^2 > s^2 - 3 \cdot \frac{\Delta}{3s} = s^2 - \Delta = 2 \tag{3}
$$
and has now contradicted the fact that $s$ is a lower bound of $Y$. Therefore, the only remaining possibility is that $s^2 = 2$. 

Lastly, assume that $s \in \mathbb{Q}$ and let $m/n$ be an irreducible representation of $s$. Then, $m^2 = 2 \cdot n^2$, so that $m^2$ is divisible by $2$ and therefore, $m$ also is divisible by $2$. But, if $m=2k$, then $2k^2 = n^2$, and for the same reason, $n$ must be divisible by $2$. However, this contradicts the assumed irreducibility of the fraction $m/n$. 