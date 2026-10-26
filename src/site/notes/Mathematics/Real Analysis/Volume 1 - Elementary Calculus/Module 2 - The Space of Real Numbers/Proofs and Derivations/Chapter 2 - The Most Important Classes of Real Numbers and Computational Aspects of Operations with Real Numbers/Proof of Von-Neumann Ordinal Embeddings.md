---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-von-neumann-ordinal-embeddings/","dg-note-properties":{}}
---

# Injectivity of the Von Neumann Successor Operation
Let $x$ and $y$ be Von Neumann ordinals satisfying the successor equality

$$
\begin{gather}
x^+ = y^+ \iff x \cup \{x\} = y \cup \{y\} \tag{1}
\end{gather}
$$

Suppose, for the sake of contradiction, that $x \ne y$. Because $x \in x \cup \{x\}$, step 1 requires that
$$
\begin{gather}
x \in y \cup \{y\} \implies (x \in y) \vee (x \in \{y\}) \tag{2}
\end{gather}
$$

Since $x \ne y$ by assumption, $x \in \{y\}$ is impossible, which forces
$$
\begin{gather}
x \in y \tag{3}
\end{gather}
$$

By symmetric reasoning, since $y \in y \cup \{y\} = x \cup \{x\}$ and $y \ne x$, it follows that
$$
\begin{gather}
y \in x \tag{4}
\end{gather}
$$

Combining step 3 and step 4 produces the mutual membership cycle $(x \in y) \wedge (y \in x)$. In Zermelo-Fraenkel set theory (ZF), consider the pair set
$$
\begin{gather}
S := \{x, y\} \tag{5}
\end{gather}
$$

The *Axiom of Regularity* (Axiom of Foundation) dictates that every nonempty set $A$ contains an element $z \in A$ disjoint from $A$ ($A \cap z = \emptyset$). Evaluating the two elements of $S$:
* If $z = x$, then $y \in x$ and $y \in S$ imply $y \in S \cap x \ne \emptyset$.
* If $z = y$, then $x \in y$ and $x \in S$ imply $x \in S \cap y \ne \emptyset$.

Thus, no element of $S$ is disjoint from $S$, violating the Axiom of Regularity. Therefore, the assumption $x \ne y$ is false, establishing that $x^+ = y^+ \implies x = y$.

---
# Immediate Successor and Well-Ordering Properties
On Von Neumann ordinals, every ordinal is a transitive set (if $u \in v$ and $v \in w$, then $u \in w$), and the strict order relation is defined by set membership (or proper inclusion):
$$
\begin{gather}
x < y \iff x \in y \iff x \subsetneq y \tag{6}
\end{gather}
$$

For any ordinal $x$, since $x \in x \cup \{x\} = x^+$, there is a $x < x^+$. Moreover, for any ordinal $z < x^+$, the relation $z \in x \cup \{x\}$ implies either $z \in x$ (so $z < x$) or $z = x$, meaning no ordinal lies strictly between $x$ and $x^+$.

Finally, let $X$ be any nonempty subset of Von Neumann ordinals. Applying the Axiom of Regularity directly to the nonempty set $X$ guarantees the existence of an element $x_{\min} \in X$ such that
$$
\begin{gather}
X \cap x_{\min} = \emptyset \tag{7}
\end{gather}
$$
If there existed any element $x \in X$ satisfying $x < x_{\min}$, then by step 6 there would be a $x \in x_{\min}$, which implies $x \in X \cap x_{\min}$, contradicting step 7. Because trichotomy holds between any two ordinals, every $x \in X$ must satisfy $x_{\min} \le x$, proving that $x_{\min}$ is the minimal element of $X$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$