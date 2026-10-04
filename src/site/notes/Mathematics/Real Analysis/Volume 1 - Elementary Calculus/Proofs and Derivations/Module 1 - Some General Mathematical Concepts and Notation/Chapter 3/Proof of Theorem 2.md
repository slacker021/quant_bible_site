---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-3/proof-of-theorem-2/","dg-note-properties":{}}
---

Assume $(X = \emptyset) \lor (Y = \emptyset)$. Suppose that, for contradiction, 
$$
X \times Y \neq \emptyset \tag{1}
$$
By definition of the non-empty set, there's at least one element $x$ in $X \times Y$.  By the definition of the Cartesian product, $z$ must be an ordered pair $(x,y)$ such that $x \in X$ and $y \in Y$. The assertion $x \in X$ implies that $X \neq \emptyset$. Similarly, $y \in Y$ implies that $Y \neq \emptyset$. Therefore, it can be inferred that 
$$
(X \neq \emptyset) \wedge (Y \neq \emptyset) \tag{2}
$$
This is the logical negation of the assumption at the start of this proof. This is a contradiction, which means that $X \times Y \neq \emptyset$ must be false. Therefore, it must be that 
$$
(X = \emptyset) \lor (Y = \emptyset) \implies X \times Y = \emptyset \tag{3}
$$

Now, suppose that 
$$\neg \left((X = \emptyset) \lor (Y = \emptyset)\right) \tag{4}$$
By De Morgan's laws of logic, step 4 is logically equivalent to
$$(X \neq \emptyset) \land (Y \neq \emptyset) \tag{5}$$
Since $X \neq \emptyset$ and $Y \neq \emptyset$, 
$$
x \in X \text{ and } y \in Y \tag{6}
$$
By definition of the Cartesian product, 
$$(x, y) \in X \times Y \tag{7}$$
Because $X \times Y$ contains at least one element $(x, y)$, it follows that 
$$X \times Y \neq \emptyset \tag{8}$$
Because an implication is logically equivalent to its contrapositive, 
$$
X \times Y = \emptyset \implies (X = \emptyset) \lor (Y = \emptyset) \tag{9}
$$
holds. 
$$\textbf{Q.E.D}$$
