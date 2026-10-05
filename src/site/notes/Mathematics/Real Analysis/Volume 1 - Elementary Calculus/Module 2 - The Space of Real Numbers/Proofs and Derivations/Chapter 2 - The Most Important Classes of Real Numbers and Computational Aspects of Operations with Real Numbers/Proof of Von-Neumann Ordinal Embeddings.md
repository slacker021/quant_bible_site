---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-von-neumann-ordinal-embeddings/","dg-note-properties":{}}
---

Let $x$ and $y$ be von Neumann ordinals such that
$$x^+ = y^+ \iff x \cup \{x\} = y \cup \{y\} \tag{1}$$

Assume, for the purpose of contradiction, that $x \ne y$. From the identity established in the first step, because $x \in x \cup \{x\}$, it must be that
$$x \in y \cup \{y\} \tag{2}$$
The condition in the preceding step implies that either $x \in y$ or $x \in \{y\}$. Since $x \ne y$ by assumption, $x \in \{y\}$ is impossible ($x \ne y$). Therefore:
$$x \in y \tag{3}$$
By exact symmetric reasoning, because $y \in y \cup \{y\} = x \cup \{x\}$ and $y \ne x$:  
$$y \in x \tag{4}$$

Combining steps 3 and 4 yields the set-membership cycle:  
$$(x \in y) \wedge (y \in x) \tag{5}$$
Now consider the set formed by the pair axiom:  
$$S = \{x, y\} \tag{6}$$
The *Axiom of Regularity* states that every non-empty set $A$ contains an element $z \in A$ such that $A \cap z = \emptyset$. Applying this axiom to $S$:
- If $z = x$, then $y \in x \implies y \in S \cap x \ne \emptyset$.
- If $z = y$, then $x \in y \implies x \in S \cap y \ne \emptyset$.

Thus, $S \cap z \ne \emptyset$ for all $z \in S$, which directly contradicts the Axiom of Regularity. Therefore, the initial assumption $x \ne y$ is false, which proves:  
$$x^+ = y^+ \implies x = y \tag{7}$$

In the von Neumann construction, the ordering relation is defined by set membership:  
$$x < y \iff x \in y \tag{8}$$
Because every element of an ordinal is also an ordinal (transitive set property), $x \in y$ is equivalent to $x \subsetneq y$. For any successor $x^+ = x \cup \{x\}$, $x \subset x^+$ and $x \in x^+$, which guarantees that
$$x < x^+ \tag{9}$$
Furthermore, there is no element $z$ such that $x < z < x^+$, because $z \in x \cup \{x\}$ implies $z \in x$ (so $z < x$) or $z = x$. Thus, $x^+$ is the immediate successor of $x$.

Last but not the least, let $X \subset \mathbb{N}_0$ be any non-empty subset of ordinals. By the Axiom of Regularity, there exists an element $x_m \in X$ such that:  
$$X \cap x_m = \emptyset \tag{10}$$
Suppose there exists an element $x \in X$ such that $x < x_m$. By the ordinal order definition, as seen in step 10, this means that  

$$x \in x_m \tag{11}$$
Since $x \in X$ and $x \in x_m$, it follows that $x \in X \cap x_m$, which contradicts equation (11). Hence, no element of $X$ is strictly smaller than $x_m$:  
$$\forall x \in X \ (x_m \le x) \tag{12}$$
Thus, $x_m$ is the minimal element of $X$, proving that $\mathbb{N}_0$ is well-ordered under inclusion.