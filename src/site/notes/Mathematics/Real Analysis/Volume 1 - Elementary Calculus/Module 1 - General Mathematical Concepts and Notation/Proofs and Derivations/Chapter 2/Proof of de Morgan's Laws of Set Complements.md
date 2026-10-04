---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-de-morgan-s-laws-of-set-complements/","dg-note-properties":{}}
---

Let $A$ and $B$ be both subsets of $M$. 

# Part 1: $C_{M}(A \cup B) = C_{M}(A) \cap C_{M}(B)$

### LHS: $C_{M}(A\cup B)$
Let $x \in C_{M}(A \cup B)$. By definition of the complement, 
$$x \not\in A \cup B \tag{1}$$which implies that 
$$
x \not\in A \text{ and } x \not\in B \tag{2}
$$
Conversely, 
$$
x \in C_{M}(A) \text{ and } x \in C_{M}(B) \tag{3}
$$
By definition of the intersection, 
$$
x \in C_{M}(A) \cap C_{M}(B) \tag{4}
$$
Therefore, 
$$
C_{M}(A \cup B) \subseteq C_{M}(A) \cap C_{M}(B) \tag{5}
$$
### RHS: $C_{M}(A) \cap C_{M}(B)$
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
Running through the definition of the complement again shows that
$$
x \in C_{M}(A \cup B) \tag{9}
$$
Therefore, 
$$ 
C_{M}(A \cup B) \supseteq C_{M}(A) \cap C_{M}(B) \tag{10}
$$
# Part 2: $C_{M}(A \cap B) = C_{M}(A) \cup C_{M}(B)$

### LHS: $C_{M}(A \cap B)$
Let $x \in C_{M}(A\cap B)$. By definition of the complement, 
$$
x \not\in A \cap B \tag{11}
$$
which implies that
$$
x \not\in A \text{ and } x \not\in B \tag{12}
$$
Running through the definition of the complement again shows that
$$
x \in C_{M}(A) \text{ and } x \in C_{M}(B) \tag{13}
$$
By definition of the intersection, 
$$
x \in C_{M}(A) \cup C_{M}(B) \tag{14}
$$
Therefore, 
$$
C_{M}(A \cap B) \subseteq C_{M}(A) \cup C_{M}(B) \tag{15}
$$

### RHS: $C_{M}(A) \cup C_{M}(B)$
Let $x \in C_{M}(A) \cup C_{M}(B)$. By definition of the complement, 
$$
x \not\in A \text{ and } x \not\in B \tag{16}
$$
and by definition of the intersection, 
$$
x \not\in A \cap B \tag{17}
$$
Running through the definition of the complement again shows that 
$$
x \in C_{M}(A \cap B) \tag{18}
$$
Therefore, 
$$
C_{M}(A \cap B) \supseteq C_{M}(A) \cup C_{M}(B) \tag{19}
$$
