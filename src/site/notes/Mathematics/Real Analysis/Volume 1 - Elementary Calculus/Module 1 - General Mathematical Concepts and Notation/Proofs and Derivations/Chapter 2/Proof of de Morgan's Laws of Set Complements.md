---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-de-morgan-s-laws-of-set-complements/","dg-note-properties":{}}
---

Let $A$ and $B$ be both subsets of $M$. 

---
# Proposition 1

### Necessity
Let $x \in C_{M}(A \cup B)$. By definition of the complement, 
$$x \not\in A \cup B \tag{1}$$which implies that 
$$
x \not\in A \text{ and } x \not\in B \tag{2}
$$
and
$$
x \in C_{M}(A) \text{ and } x \in C_{M}(B) \tag{3}
$$
By definition of the intersection, 
$$
x \in C_{M}(A) \cap C_{M}(B) \tag{4}
$$
Therefore, 
$$
C_{M}(A \cup B) \subset C_{M}(A) \cap C_{M}(B) \tag{5}
$$
### Sufficiency
Let $x \in C_{M}(A) \cap C_{M}(B)$. By definition of the intersection, 
$$
x \in C_{M}(A) \text{ and } x \in C_{M}(B) \tag{6}
$$
By definition of the complement, 
$$
x \not\in A \text{ and } x \not\in B \tag{7}
$$
Which would then imply that 
$$
x \not\in A \cup B \tag{8}
$$
Again, the definition of the complement shows that
$$
x \in C_{M}(A \cup B) \tag{9}
$$
Therefore, 
$$ 
C_{M}(A \cup B) \supset C_{M}(A) \cap C_{M}(B) \tag{10}
$$

---
# Proposition 2

### Necessity
Let $x \in C_{M}(A\cap B)$. By definition of the complement, 
$$
x \not\in A \cap B \tag{11}
$$
which implies that
$$
x \not\in A \text{ or } x \not\in B \tag{12}
$$
If $x$ isn't in $A$ nor $B$, then 
$$
x \not\in A \cap B \implies x \not\in A \lor x \not\in B \tag{13}
$$
The negation of the conclusion of step 13 would be
$$
x \in C_{M}(A) \lor x \in C_{M}(B) \tag{14}
$$
Therefore, 
$$
C_{M}(A \cap B) \supset C_{M}(A) \cup C_{M}(B) \tag{15}
$$

### Sufficiency
Let $x \in C_{M}(A) \cup C_{M}(B)$. By definition of the union and complement, 
$$
x \in C_{M}(A) \cup C_{M}(B) \implies x \not\in A \text{ or } x \not\in B \tag{16}
$$
and by definition of the intersection, 
$$
x \not\in A \cap B \tag{17}
$$
Again, definition of the complement again shows that 
$$
x \in C_{M}(A \cap B) \tag{18}
$$
Therefore, 
$$
C_{M}(A \cap B) \supseteq C_{M}(A) \cup C_{M}(B) \tag{19}
$$
$$
\textbf{Q.E.D}
$$
