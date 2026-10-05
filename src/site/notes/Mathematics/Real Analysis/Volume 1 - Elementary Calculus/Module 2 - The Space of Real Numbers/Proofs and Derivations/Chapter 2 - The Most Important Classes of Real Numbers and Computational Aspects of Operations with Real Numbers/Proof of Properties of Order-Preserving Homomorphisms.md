---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-properties-of-order-preserving-homomorphisms/","dg-note-properties":{}}
---

Assume the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|Axiom of Completeness]] holds. Let $X$ and $Y$ be non-empty subsets of $\mathbb{R}$ such that $X \cup Y = \mathbb{R}$, and for all $x \in X$ and $y \in Y$, the inequality $x \le y$ is satisfied.

By the Axiom of Completeness, there exists a separating real number $c \in \mathbb{R}$ such that
$$x \le c \le y \quad \forall x \in X, \forall y \in Y \tag{1}$$
Since the union of the two sets encompasses the entire real line ($X \cup Y = \mathbb{R}$), the element $c$ must belong to either $X$ or $Y$. This leads to two cases
1.  Assume $c \in X$. Since $x \le c$ for all $x \in X$, the element $c$ is by definition the maximal element of $X$ (denoted as $\max X = c$).
2. Assume $c \in Y$. Since $c \le y$ for all $y \in Y$, the element $c$ is by definition the minimal element of $Y$ (denoted as $\min Y = c$).

It is impossible for both a maximal element of $X$ and a minimal element of $Y$ to exist simultaneously without intersecting in a single point, but the theorem only requires that _either_ one or the other condition is met. Thus, the forward implication is established.

Secondly, assume [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Dedekind's Cut Theorem and Complete Equivalence\|Proof of Dedekind's Cut Theorem and Complete Equivalence]] holds.
A Dedekind cut $(X, Y)$ on the real line is constructed as follows. Let $Y$ be the set of all strict upper bounds of $A$:  
$$Y = \{ y \in \mathbb{R} \mid \forall a \in A \ (a < y) \} \tag{2}$$
Let $X$ be the complement of $Y$ in $\mathbb{R}$:  

$$X = \mathbb{R} \setminus Y = \{ x \in \mathbb{R} \mid \exists a \in A \text{ such that } x \le a \} \tag{3}$$
The properties of the cut $(X, Y)$ are verified below:
1. **Non-empty:** Since $A$ is non-empty, choosing any $a_0 \in A$ gives $a_0 \in X$, so $X \neq \emptyset$. Furthermore, any element $b \in B$ acts as an upper bound for $A$. If $b \notin Y$, then there exists some $a' \in A$ such that $b \le a'$. Given the initial hypothesis that $a \le b$ for all $a \in A$, it must be true that $b = a'$. In this boundary case, $b+1$ is strictly greater than all elements in $A$, ensuring $Y$ is never empty.
2. **Exhaustive and Ordered:** By construction, $X \cup Y = \mathbb{R}$ and $X \cap Y = \emptyset$. For any $x \in X$ and $y \in Y$, there exists an $a \in A$ such that $x \le a$. By the definition of $Y$, $a < y$. By transitivity, $x < y$.

The sets $X$ and $Y$ satisfy the hypotheses of Dedekind's Theorem. Therefore, either $X$ has a maximal element or $Y$ has a minimal element. Let this distinguished element be denoted as $c$. In either scenario, $c$ separates the sets such that $x \le c \le y$ for all $x \in X$ and $y \in Y$.

Because $A \subset X$, it naturally follows that $a \le c$ for all $a \in A$. For any element $b \in B$, $b$ is an upper bound for $A$. If $b \in Y$, then $c \le b$. If $b \notin Y$, then $b \in X$, which requires $b = \max A$, in which case $c = b$ and $c \le b$ still holds.

Therefore, $a \le c \le b$ for all $a \in A$ and $b \in B$, which perfectly satisfies the Axiom of Completeness.
$$
\textbf{Q.E.D}
$$