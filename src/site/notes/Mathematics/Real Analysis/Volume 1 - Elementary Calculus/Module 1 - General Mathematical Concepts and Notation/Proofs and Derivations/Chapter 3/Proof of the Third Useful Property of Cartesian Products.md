---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-3/proof-of-the-third-useful-property-of-cartesian-products/","dg-note-properties":{}}
---

# Proof Method 1: Mutual Subset Containment

### Necessity
Let $(a, b) \in (X \times Y) \cup (Z \times Y)$ be an arbitrary element. By definition of the set union, 
$$(a, b) \in (X \times Y) \lor (a, b) \in (Z \times Y) \tag{1}$$
This leads to two cases: 
$$
\begin{gather}
\text{Case 1: Assume } (a, b) \in X \times Y \\
\text{By definition of the Cartesian product, } a \in X \text{ and } b \in Y.  \\
\text{Since } a \in X, \text{ it follows by definition of the union that } a \in X \cup Z.  \\
\text{Combining } a \in X \cup Z \text{ and } b \in Y \text{ yields } \\
(a, b) \in (X \cup Z) \times Y.  \\[2.5mm]

\text{Case 2: Assume } (a,b) \in Z \times Y \\
\text{By definition of the Cartesian product, } a \in Z \text{ and } b \in Y.  \\
\text{Since } a \in Z, \text{ it follows by definition of the union that } a \in X \cup Z.  \\
\text{Combining } a \in X \cup Z \text{ and } b \in Y \text{ yields } \\
(a, b) \in (X \cup Z) \times Y. \tag{2}
\end{gather}
$$
Because $(a, b) \in (X \cup Z) \times Y$ holds in both cases, every element of $(X \times Y) \cup (Z \times Y)$ belongs to $(X \cup Z) \times Y$. Therefore, 
$$
(X \times Y) \cup (Z \times Y) \subseteq (X \cup Z) \times Y \tag{3}
$$

### Sufficiency
Let $(a, b) \in (X \cup Z) \times Y$ be an arbitrary element. By definition of set union,
$$a \in X \cup Z \implies (a \in X) \lor (a \in Z) \tag{4}$$
This leads to two cases:
$$
\begin{gather}
\text{Case 1: Assume } a \in X. \\
\text{Since } b \in Y \text{, the pair satisfies } (a,b) \in X \times Y.  \\
\text{By definition of the set union, } (a,b) \in (X \times Y) \cup (Z \times Y).  \\[2.5mm]

\text{Case 2: Assume } a \in X.  \\
\text{Since } b \in Y \text{, the pair satisfies } (a,b) \in Z \times Y.  \\
\text{By definition of the set union, } (a,b) \in (X \times Y) \cup (Z \times Y). \tag{5}
\end{gather}
$$
Because $(a, b) \in (X \times Y) \cup (Z \times Y)$ holds in both cases, every element of $(X \cup Z) \times Y$ belongs to $(X \times Y) \cup (Z \times Y)$. Therefore, 
$$ (X \cup Z) \times Y \subseteq (X \times Y) \cup (Z \times Y) \tag{6}$$
$$
\textbf{Q.E.D}
$$

---
# Proof Method 2: Direct Logical Equivalence
Classic predicate logic can be used to verify the theorem: 
$$
\begin{aligned} 
(a, b) \in (X \cup Z) \times Y &\iff (a \in X \cup Z) \land (b \in Y) & \text{(Definition of Cartesian Product)} \\ &\iff ((a \in X) \lor (a \in Z)) \land (b \in Y) & \text{(Definition of Set Union)} \\ &\iff ((a \in X) \land (b \in Y)) \lor ((a \in Z) \land (b \in Y)) & \text{(Distributivity of } \land \text{ over } \lor \text{)} \\ &\iff ((a, b) \in X \times Y) \lor ((a, b) \in Z \times Y) & \text{(Definition of Cartesian Product)} \\ &\iff (a, b) \in (X \times Y) \cup (Z \times Y) & \text{(Definition of Set Union)}  \\[2.5mm]
& & \text{(7)}
\end{aligned}
$$
$$\textbf{Q.E.D}$$
