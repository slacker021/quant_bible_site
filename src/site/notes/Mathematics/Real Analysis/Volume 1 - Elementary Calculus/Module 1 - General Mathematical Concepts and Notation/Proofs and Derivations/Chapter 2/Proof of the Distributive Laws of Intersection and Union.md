---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-the-distributive-laws-of-intersection-and-union/","dg-note-properties":{}}
---

Let $A,B,C$ be subsets of $M$. 
# Proposition 1

### Necessity
Let $x \in A \cap (B \cup C)$. By definition of the intersection, 
$$
x \in A \wedge x \in (B \cup C) \tag{1}
$$
and by definition of the union, 
$$x \in B \lor x \in C \tag{2}$$
Regardless of whether or not $x$ is in $B$ or $C$, the following hold true because $x \in A$: 
$$
\begin{align}
x \in A \cup B & \\ 
x \in A \cup C \tag{3}
\end{align}
$$

If the two sets above were to be intersected, 
$$
x \in (A \cup B) \cap (A \cup C) \tag{4}
$$
Therefore, 
$$
A \cap (B \cup C) \subset (A \cap B) \cup (A \cap C) \tag{5}
$$

### Sufficiency 
Let $x \in (A \cup B) \cap (A \cup C)$. By definition of the intersection, 
$$
x \in (A \cup B) \text{ and } x \in (A \cup C) \tag{6}
$$
and by definition of the union, 
$$
x \in A \lor x \in B \text{ and } x \in A \lor x \in C \tag{7}
$$
This leads to two cases: 
1. $x \in A \cap (B \cup C) \implies x \in A \land (x \in B \lor x \in C) \implies (x \in A \land x \in B) \lor (x \in A \land x \in C) \implies x \in (A \cap B) \cup (A \cap C)$. 
2. $x∈(A∩B)∪(A∩C)⟹(x∈A∧x∈B)∨(x∈A∧x∈C)⟹x∈A∧(x∈B∨x∈C)⟹x∈A∩(B∪C).$
Therefore, 
$$
(A \cap B) \cup (A \cap C) \subset A \cap (B \cup C) \tag{8}
$$

---
# Proposition 2

### LHS: $A \cup (B \cap C)$
Let $x \in A \cup (B \cap C)$. The definition of the union would provide two cases: 
1. If $x \in A$, then $x \in A \cup B$ and $x \in A \cup C$. 
2. If $x \in B \cap C$, then $x \in A \cup B$ and $x \in A \cup C$. 
Both cases hold, which infers that
$$
A \cup (B \cap C) \subseteq (A \cup B) \cap (A \cup C) \tag{9}
$$

### RHS: $(A \cup B) \cap (A \cup C)$
Let $x \in (A \cup B) \cap (A \cup C)$. This implies two cases:
1. If $x \in A$, then $x \in A \cup (B \cap C)$. 
2. If $x \in B \cap C$, then $x \in A \cup (B \cap C)$.
Both cases hold, inferring that
$$
A \cup (B \cap C) \supseteq (A \cup B) \cap (A \cup C) \tag{10}
$$
$$\textbf{Q.E.D}$$