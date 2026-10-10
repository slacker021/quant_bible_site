---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-3/proof-of-the-second-useful-property-of-cartesian-products/","dg-note-properties":{}}
---

Assume $(A \subseteq X) \land (B \subseteq Y)$. Now, let $(a, b) \in A \times B$ be an arbitrary ordered pair. By definition of the Cartesian product:
$$(a, b) \in A \times B \implies (a \in A) \land (b \in B) \tag{1}$$
Which implies the following:
$$
\begin{gather}
A \subseteq X, a \in A \implies a \in X \\
B \subseteq Y, b \in B \implies b \in Y \tag{2}
\end{gather}
$$
Combining these statements yields
$$
(a \in X) \land (b \in Y) \tag{3}
$$
By definition of the Cartesian product $X \times Y$, 
$$ (a, b) \in X \times Y \tag{4}$$
Because every element of $A \times B$ is an element of $X \times Y$, it follows that:
$$A \times B \subset X \times Y \tag{5}$$

Now, Assume $A \times B \subseteq X \times Y$, with $A \neq \emptyset$ and $B \neq \emptyset$. Let $a \in A$ be an arbitrary element and since $B \neq \emptyset$, there exists at least one element $b_0 \in B$. This leads to the construction of the ordered pair $(a,b_{0})$. By definition, 
$$(a, b_0) \in X \times Y \tag{6}$$
By definition of the Cartesian product,
$$(a, b_0) \in X \times Y \implies a \in X \tag{7}$$
Since $a \in A$ was arbitrary, $a \in X$ holds for all $a \in A$. Hence, 
$$A \subset X \tag{8}$$

Now, let $b \in B$ be an arbitrary element and since $A \neq \emptyset$, there exists at least one element $a_0 \in A$. This leads to the construction of the ordered pair $(a_0, b)$. By definition,
$$(a_0, b) \in A \times B \tag{9}$$
By the premise $A \times B \subseteq X \times Y$,
$$(a_0, b) \in X \times Y \tag{10}$$
By definition of the Cartesian product,
$$(a_0, b) \in X \times Y \implies b \in Y \tag{11}$$
Since $b \in B$ was arbitrary, $b \in Y$ holds for all $b \in B$. Hence,
$$B \subset Y \tag{12}$$
Combining both inclusions yields
$$(A \subset X) \land (B \subset Y) \tag{13}$$
$$\textbf{Q.E.D}$$
