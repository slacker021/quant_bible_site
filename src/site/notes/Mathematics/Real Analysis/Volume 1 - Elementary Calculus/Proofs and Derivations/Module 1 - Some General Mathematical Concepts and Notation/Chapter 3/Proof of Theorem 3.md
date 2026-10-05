---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-3/proof-of-theorem-3/","dg-note-properties":{}}
---

Assume $(A \subseteq X) \land (B \subseteq Y)$. Now, let $(a, b) \in A \times B$ be an arbitrary ordered pair. By definition of the Cartesian product:
$$(a, b) \in A \times B \implies (a \in A) \land (b \in B) \tag{1}$$
Which implies the following:
$$
\begin{gather}
\text{Since } A \subseteq X, a \in A \implies a \in X \\
\text{Since } B \subseteq Y, b \in B \implies b \in Y \tag{2}
\end{gather}
$$
Combining these statements yields
$$
(a \in X) \land (b \in Y) \tag{3}
$$
By definition of the Cartesian product, 
$$(a, b) \in A \times B \implies (a \in A) \land (b \in B) \tag{4}$$
Which then implies that
$$
\begin{gather}
\text{Since } A \subseteq X, a \in A \implies a \in X \\
\text{Since } B \subseteq Y, b \in B \implies b \in Y \tag{5}
\end{gather}
$$
Combining these statements yields
$$(a \in X) \land (b \in Y) \tag{6}$$
By definition of the Cartesian product $X \times Y$, 
$$ (a, b) \in X \times Y \tag{7}$$
Because every element of $A \times B$ is an element of $X \times Y$, it follows that:
$$A \times B \subseteq X \times Y \tag{8}$$

Now, Assume $A \times B \subseteq X \times Y$, with $A \neq \emptyset$ and $B \neq \emptyset$. Let $a \in A$ be an arbitrary element and since $B \neq \emptyset$, there exists at least one element $b_0 \in B$. This leads to the construction of the ordered pair $(a,b_{0})$. By definition, 
$$(a, b_0) \in X \times Y \tag{9}$$
By definition of the Cartesian product,
$$(a, b_0) \in X \times Y \implies a \in X \tag{10}$$
Since $a \in A$ was arbitrary, $a \in X$ holds for all $a \in A$. Hence, 
$$A \subseteq X \tag{11}$$

Now, let $b \in B$ be an arbitrary element and since $A \neq \emptyset$, there exists at least one element $a_0 \in A$. This leads to the construction of the ordered pair $(a_0, b)$. By definition,
$$(a_0, b) \in A \times B \tag{12}$$
By the premise $A \times B \subseteq X \times Y$,
$$(a_0, b) \in X \times Y \tag{13}$$
By definition of the Cartesian product,
$$(a_0, b) \in X \times Y \implies b \in Y \tag{14}$$
Since $b \in B$ was arbitrary, $b \in Y$ holds for all $b \in B$. Hence,
$$B \subseteq Y \tag{15}$$
Combining both inclusions yields
$$(A \subseteq X) \land (B \subseteq Y) \tag{16}$$
$$\textbf{Q.E.D}$$

