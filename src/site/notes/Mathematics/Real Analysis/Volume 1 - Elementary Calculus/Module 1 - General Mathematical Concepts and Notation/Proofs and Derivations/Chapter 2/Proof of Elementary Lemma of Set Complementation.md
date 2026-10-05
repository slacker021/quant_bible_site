---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-elementary-lemma-of-set-complementation/","dg-note-properties":{}}
---

# Part 1: $(A \subset C) \wedge (B \subset C) \iff (A \cup B) \subset C$

### LHS ($\implies$)
Assume $(A \subseteq C) \land (B \subseteq C)$ and let $x \in A \cup B$ be an arbitrary element. By definition of the union, 
$$x \in A \cup B \implies (x \in A) \lor (x \in B) \tag{1}$$
This leads to two cases: 
$$
\begin{gather}
\text{Case 1: Since } A \subseteq C, x \in A \implies x \in C \\
\text{Case 2: Since } B \subseteq C, x \in B \implies x \in C \tag{2}
\end{gather}
$$
In both cases, $x \in C$. Thus, 
$$(A \cup B) \subseteq C \tag{3}$$

### RHS ($\impliedby$)
Assume $(A \cup B) \subseteq C$, where by definition of the set union
$$A \subseteq A \cup B \text{ and } B \subseteq A \cup B \tag{4}$$
Transitivity of subset inclusion states that
$$\text{If } S \subseteq T \text{ and } T \subseteq U, \text{ then } S \subseteq U \tag{5} $$
Applying transitivity shows that
$$
\begin{gather}
A \subseteq (A \cup B) \text{ and } (A \cup B) \subseteq C \implies A \subseteq C \\
B \subseteq (A \cup B)$ and $(A \cup B) \subseteq C \implies B \subseteq C \tag{6}
\end{gather}
$$
Therefore, 
$$(A \subseteq C) \land (B \subseteq C) \tag{7}$$

# Part 2: $(A \subseteq B) \iff C_M B \subseteq C_M A)$

### LHS ($\implies$) 
Assume $A \subseteq B$ and let $x \in C_{M}(B)$. By definition of the complement, 
$$x \in C_M B \implies (x \in M) \land (x \notin B) \tag{8}$$
Now, assume (for the purposes of contradiction) that $x \in A$. Since $A \subseteq B$,
$$x \in A \implies x \in B \tag{9}$$
which directly contradicts $x \not\in B$. Hence, $x \notin A$ Combined with $x \in M$, it can be inferred that
$$
x \in C_{M}(A) \tag{10}
$$
Therefore, 
$$
C_{M}(B) \subseteq C_{M}(A) \tag{11}
$$

### RHS ($\impliedby$)
Assume $C_{M}(B) \subseteq C_{M}(A)$ and let $x \in A$ be an arbitrary element. Since $A \subseteq M$, $x \in M$. Assume (for the purposes of contradiction) that $x \notin B$. Since $x \in M$ and $x \notin B$, it follows that
$$
x \in C_{M}(B) \tag{12}
$$
By the assumption
$$
C_{M}(B) \subseteq C_{M}(A) \implies x \in C_{M}(A) \tag{13}
$$
By definition of $C_{M}(A)$, 
$$x \in C_M(A) \implies x \notin A \tag{14}$$
Step 14 contradicts the initial premise that $x \in A$. Therefore, $x \in B$ establishes that 
$$A \subseteq B \tag{15}$$

# Part 3: $C_{M}(C_{M}(A)) = A$

### LHS ($C_{M}(C_{M}(A))$)
Let $x \in C_M{C}_M(A)$. By definition of complementation, 
$$x \in M \text{ and }x \notin C_M A \tag{16}$$
The statement $x \not\in C_{M}(A)$ means 
$$
\neg(x \in M \land x \notin A) \tag{17}
$$
which simplifies via De Morgan's laws of logic to
$$
(x \notin M) \lor (x \in A) \tag{18}
$$
Since $x \in M$ is true, $x \in A$ must hold. Thus,
$$ C_{M}(C_{M}(A)) \subseteq A \tag{19}$$

### RHS ($A$)
Let $x \in A$. Since $A \subseteq M$, $x \in M$. Since $x \in A$, the statement $x \not\in A$ is false and implies that
$$x \not\in C_{M}(A) \tag{20}$$
Since $x \not\in M$ and $x \not\in C_{M}(A)$, it follows by definition that
$$x \not\in C_{M}(C_{M}(A)) \tag{21}$$
Thus, 
$$A \subseteq C_M(C_M(A)) \tag{22}$$
$$\textbf{Q.E.D}$$

