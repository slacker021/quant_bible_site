---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-monotonicity-and-ordering-of-extrema/","dg-note-properties":{}}
---

Let $A$ and $B$ be non-empty subsets of $\mathbb{R}$ such that $A \subset B$, and suppose $B$ is bounded above. Let $M_B = \sup B$. By the definition of the supremum, 
$$\forall b \in B \ (b \le M_B) \tag{1}$$

Since $A \subset B$, every element $a \in A$ satisfies $a \in B$. Consequently, 

$$\forall a \in A \ (a \le M_B) \tag{2}$$

The equation of step 2 proves that $M_B$ is an upper bound for $A$. Since $\sup A$ is the least upper bound of $A$, it must be less than or equal to any upper bound of $A$:  

$$\sup A \le M_B = \sup B \tag{3}$$

Similarly, if $B$ is bounded below, let $m_B = \inf B$. Then

$$\forall b \in B \ (m_B \le b) \implies \forall a \in A \ (m_B \le a) \tag{4}$$

Thus, $m_B$ is a lower bound for $A$. By the definition of the infimum as the greatest lower bound:  

$$\inf B = m_B \le \inf A \tag{5}$$

Now, let $X,Y \subset \mathbb{R}$ be non-empty sets such that:  

$$\forall x \in X \ \forall y \in Y \ (x \le y) \tag{6}$$

Fix an arbitrary element $y_0 \in Y$. By condition (6), $x \le y_0$ for all $x \in X$. Thus, $y_0$ is an upper bound for $X$. By definition of the least upper bound:  

$$\sup X \le y_0 \tag{7}$$

Because inequality in step 7 holds for every $y_0 \in Y$, the value $\sup X$ serves as a lower bound for the set $Y$. Since $\inf Y$ is the greatest lower bound of $Y$:  

$$\sup X \le \inf Y \tag{8}$$


Lastly, assume additionally that $X \cup Y = \mathbb{R}$. From Part 2, $\sup X \le \inf Y$. Suppose, for the sake of contradiction, that:  
$$\sup X < \inf Y \tag{9}$$
By the density of real numbers (or the midpoint construction), there exists $c \in \mathbb{R}$ such that
$$\sup X < c < \inf Y \tag{10}$$
Because $c > \sup X$, $c$ cannot belong to $X$ (as $\sup X$ is an upper bound for $X$). Simultaneously, because $c < \inf Y$, $c$ cannot belong to $Y$ (as $\inf Y$ is a lower bound for $Y$). This implies
$$c \notin X \cup Y \tag{11}$$

Step 11 contradicts the hypothesis that $X \cup Y = \mathbb{R}$. Therefore, the assumption $\sup X < \inf Y$ is false, which forces:  
$$\sup X = \inf Y \tag{12}$$$$\textbf{Q.E.D}$$