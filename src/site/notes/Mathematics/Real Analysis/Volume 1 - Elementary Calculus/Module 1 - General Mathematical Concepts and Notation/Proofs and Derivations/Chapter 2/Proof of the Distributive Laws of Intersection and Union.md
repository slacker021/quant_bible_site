---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-the-distributive-laws-of-intersection-and-union/","dg-note-properties":{}}
---

Let $A,B,C$ be subsets of $M$. 

# Proposition 1

### LHS: $A \cap (B \cup C)$
Let $x \in A \cap (B \cup C)$. By definition of the intersection, 
$$
x \in A \wedge x \text{ and } (B \cup C) \tag{1}
$$
and by definition of the union, 
$$x \in B \lor x \in C \tag{2}$$
Regardless of whether or not $x$ is in $B$ or/and $C$, the following hold true because $x \in A$: 
$$
\begin{align}
x \in A \cup B & \\ 
x \in A \cup C \tag{3}
\end{align}
$$

If the two sets above we to be intersected, 
$$
x \in (A \cup B) \cap (A \cup C) \tag{4}
$$
Therefore, 
$$
A \cap (B \cup C) \subseteq (A \cup B) \cap (A \cup C) \tag{5}
$$

### RHS: $(A \cup B) \cap (A \cup C)$
Let $x \in (A \cup B) \cap (A \cup C)$. By definition of the intersection, 
$$
x \in (A \cup B) \text{ and } x \in (A \cup C) \tag{6}
$$
and by definition of the union, 
$$
x \in A \lor x \in B \text{ and } x \in A \lor x \in C \tag{7}
$$
This leads to two cases: 
1. If $x \in A \cap B$. Then $x \in A$ and $x \in B$. Since $x \in B$, $x \in B \cup C$. Thus, $x \in A \cap (B \cup C)$.
2. If $x \in A \cap C$. Then $x \in A$ and $x \in C$. Since $x \in C$, $x \in B \cup C$. Thus, $x \in A \cap (B \cup C)$.
Therefore, 
$$
(A \cap B) \cup (A \cap C) \subseteq A \cap (B \cup C) \tag{8}
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