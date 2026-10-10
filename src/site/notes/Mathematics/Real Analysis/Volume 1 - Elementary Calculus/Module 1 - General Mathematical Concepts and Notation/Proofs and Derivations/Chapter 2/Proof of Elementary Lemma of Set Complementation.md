---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-elementary-lemma-of-set-complementation/","dg-note-properties":{}}
---

# Proposition 1

### Necessity
Assume $A$ and $B$ are both proper subsets of $C$, and let $x \in A \cup B$. By definition of the union, 
$$x \in A \cup B \implies (x \in A) \lor (x \in B) \tag{1}$$
This leads to two cases: 
$$
\begin{gather}
\text{Case 1: Since } A \subset C, x \in A \implies x \in C \\
\text{Case 2: Since } B \subset C, x \in B \implies x \in C \tag{2}
\end{gather}
$$
In both cases, $x \in C$. Thus, 
$$(A \cup B) \subset C \tag{3}$$

### Sufficiency 
Assume $(A \cup B) \subset C$, where by definition of the set union
$$A \subset A \cup B \text{ and } B \subset A \cup B \tag{4}$$
By the transitivity of subset relation, both $A$ and $B$ are proper subsets of $C$. Therefore, 
$$(A \subset C) \land (B \subset C) \tag{5}$$

---
# Proposition 2

### Necessity
Assume $A \subset B$ and let $x \in C_{M}(B)$. By definition of the complement, 
$$x \in C_M B \implies (x \in M) \land (x \notin B) \tag{6}$$
Now, assume for the purposes of contradiction, that $x \in A$: 
$$x \in A \implies x \in B \tag{7}$$
since $A \subset B$, which directly contradicts $x \not\in B$. Hence, $x \notin A$ and $x \in M$:  
$$
x \in C_{M}(A) \tag{8}
$$
Therefore, 
$$
C_{M}(B) \subset C_{M}(A) \tag{9}
$$

### Sufficiency
Assume $C_{M}(B) \subset C_{M}(A)$ and let $x \in A$ . Since $A \subset M$, $x \in M$. Assume, for the purposes of contradiction, that $x \notin B$. Since $x \in M$ and $x \notin B$, it follows that
$$
x \in C_{M}(B) \tag{10}
$$
By the assumption
$$
C_{M}(B) \subset C_{M}(A) \implies x \in C_{M}(A) \tag{11}
$$
By definition of $C_{M}(A)$, 
$$x \in C_M(A) \implies x \notin A \tag{12}$$
Step 12 contradicts the initial premise that $x \in A$. Therefore, $x \in B$ establishes that 
$$A \subset B \tag{13}$$

---
# Proposition 3

### Necessity
Let $x \in C_M{C}_M(A)$. By definition of complementation, 
$$x \in M \text{ and }x \notin C_M A \tag{14}$$
The statement $x \not\in C_{M}(A)$ means 
$$
\neg(x \in M \land x \notin A) \tag{15}
$$
Since $x \in M$, the only way for the statement to be true is if $x \in A$. Thus,
$$ C_{M}(C_{M}(A)) \subset A \tag{16}$$

### Sufficiency
Let $x \in A$. Since $A \subset M$, $x \in M$. Since $x \in A$,
$$x \not\in C_{M}(A) \tag{17}$$
Since $x \in A$ and $x \not\in C_{M}(A)$, while $x \in M$ but $x \not\in C_{M}(A)$: 
$$x \in C_{M}(C_{M}(A)) \tag{18}$$
Thus, 
$$A \subset C_M(C_M(A)) \tag{19}$$
$$\textbf{Q.E.D}$$

