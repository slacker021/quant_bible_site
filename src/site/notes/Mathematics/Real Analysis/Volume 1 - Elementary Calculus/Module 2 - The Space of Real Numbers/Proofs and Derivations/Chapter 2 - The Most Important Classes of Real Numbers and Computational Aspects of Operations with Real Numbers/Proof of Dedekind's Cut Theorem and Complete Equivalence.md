---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-dedekind-s-cut-theorem-and-complete-equivalence/","dg-note-properties":{}}
---

It is assumed that the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|Axiom of Completeness holds]]. Let $X$ and $Y$ be non-empty subsets of the real numbers encompassing the entire real line. Additionally, let the following assumptions be declared:
$$\begin{gather} X \cup Y = \mathbb{R}, \quad X \neq \emptyset, \quad Y \neq \emptyset \tag{1} \end{gather}$$
It is established by hypothesis that every element of the first set is less than or equal to every element of the second set: 
$$\begin{gather} x \le y \quad \forall x \in X, \forall y \in Y \tag{2} \end{gather}$$
By the Axiom of Completeness, there exists a separating real number $c$ lying between the two sets:
$$\begin{gather} \exists c \in \mathbb{R} \text{ such that } x \le c \le y \quad \forall x \in X, \forall y \in Y \tag{3} \end{gather}$$
Since the union of the two sets exhausts the entire real line ($X \cup Y = \mathbb{R}$), the element $c$ must uniquely belong to either $X$ or $Y$. The two mutually exclusive cases are evaluated below: 
$$\begin{gather} c \in X \implies \forall x \in X \ (x \le c) \implies c = \max X  \\
c \in Y \implies \forall y \in Y \ (c \le y) \implies c = \min Y 
\tag{4} \end{gather}$$
It is impossible for both a maximal element of $X$ and a minimal element of $Y$ to exist simultaneously without intersecting at a single point. However, the theorem only requires that either condition is met, thereby establishing the forward implication: 
$$\begin{gather} (c = \max X) \lor (c = \min Y) \tag{5} \end{gather}$$

It is now assumed that Dedekind's Theorem, which was proven in steps 1 through 5, holds. It must be shown that for any two non-empty subsets $A, B \subset \mathbb{R}$ where $a \le b$ for all $a \in A$ and $b \in B$, there exists a real number $c \in \mathbb{R}$ separating them: 
$$\begin{gather} \exists c \in \mathbb{R} \text{ such that } a \le c \le b \quad \forall a \in A, \forall b \in B \tag{6} \end{gather}$$
A Dedekind cut $(X, Y)$ on the real line is constructed. Let $Y$ be defined as the set of all strict upper bounds of $A$: 
$$\begin{gather} Y = \{ y \in \mathbb{R} \mid \forall a \in A \ (a < y) \} \tag{7} \end{gather}$$

Let $X$ be defined as the complement of $Y$ in $\mathbb{R}$: 
$$\begin{gather} X = \mathbb{R} \setminus Y = \{ x \in \mathbb{R} \mid \exists a \in A \text{ such that } x \le a \} \tag{8} \end{gather}$$
The properties of the cut $(X, Y)$ are verified to be exhaustive, ordered, and non-empty. Since $A$ is non-empty, choosing any $a_0 \in A$ gives $a_0 \in X$, ensuring $X \neq \emptyset$. Any $b \in B$ acts as an upper bound for $A$. If $b \notin Y$, then $b \in X$, meaning $b \le a'$ for some $a' \in A$. Since $a \le b$ for all $a \in A$, this forces $b = a'$. In this boundary scenario, $b+1$ is strictly greater than all elements in $A$, ensuring $Y \neq \emptyset$:
$$\begin{gather} X \cup Y = \mathbb{R}, \quad X \cap Y = \emptyset \\
\forall x \in X, \forall y \in Y \implies x < y
 \tag{9} \end{gather}$$

The sets $X$ and $Y$ satisfy the hypotheses of Dedekind's Theorem. Therefore, a distinguished separating element $c$ must exist: $$\begin{gather} \exists c \in \mathbb{R} \text{ such that } (c = \max X) \lor (c = \min Y) \tag{10} \end{gather}$$$$\begin{gather} x \le c \le y \quad \forall x \in X, \forall y \in Y \tag{11} \end{gather}$$
Because $A \subset X$, it naturally follows that $c$ bounds $A$ from above:
$$\begin{gather} \forall a \in A \implies a \le c \tag{12} \end{gather}$$
For any element $b \in B$, $b$ is an upper bound for $A$. If $b \in Y$, then $c \le b$. If $b \notin Y$, then $b \in X$, which requires $b = \max A$. In this boundary case, $c = b$, meaning $c \le b$ still holds:

$$\begin{gather} \forall b \in B \implies c \le b \tag{13} \end{gather}$$
This establishes that $c$ separates the original sets $A$ and $B$, perfectly satisfying the Axiom of Completeness:$$\begin{gather} a \le c \le b \quad \forall a \in A, \forall b \in B \tag{14} \end{gather}$$$$\begin{gather} \textbf{Q.E.D} \end{gather}$$
