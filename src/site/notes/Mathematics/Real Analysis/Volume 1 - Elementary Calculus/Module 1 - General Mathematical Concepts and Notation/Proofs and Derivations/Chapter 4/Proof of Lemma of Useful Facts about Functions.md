---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-4/proof-of-lemma-of-useful-facts-about-functions/","dg-note-properties":{}}
---

# Part 1: $A' \subseteq B' \implies f^{-1}(A') \subseteq f^{-1}(B')$
Let $x \in f^{-1}(A')$ be an arbitrary element. By the definition of the inverse image,
$$x \in f^{-1}(A') \implies f(x) \in A' \tag{1}$$
Since $A' \subseteq B'$, 
$$f(x) \in A' \implies f(x) \in B' \tag{2}$$
By the definition of the inverse image, 
$$f(x) \in B' \implies x \in f^{-1}(B') \tag{3}$$
Since $x \in f^{-1}(A') \implies x \in f^{-1}(B')$, it follows that
$$ f^{-1}(A') \subseteq f^{-1}(B') \tag{4}$$
# Part 2: $f^{-1}(A' \cap B') = f^{-1}(A') \cap f^{-1}(B')$
Establishing set equality can be done by using a continuous chain of logic equivalences for an arbitrary element $x \in X$: 
$$\begin{aligned} 
x \in f^{-1}(A' \cap B') &\iff f(x) \in A' \cap B' & \text{(Definition of inverse image)} \\ &\iff (f(x) \in A') \land (f(x) \in B') & \text{(Definition of set intersection)} \\ &\iff (x \in f^{-1}(A')) \land (x \in f^{-1}(B')) & \text{(Definition of inverse image)} \\ &\iff x \in f^{-1}(A') \cap f^{-1}(B') & \text{(Definition of set intersection)} \\
& & \text{(5)}
\end{aligned}$$
Because each step is a logical equivalence ($\iff$), the set identity $f^{-1}(A' \cap B') = f^{-1}(A') \cap f^{-1}(B')$ holds directly for any mapping $f$.

# Part 3: $f^{-1}(A' \cup B') = f^{-1}(A') \cup f^{-1}(B')$
Similar to part 2, this can proven using a chain of logical equivalences for an arbitrary element 
$x \in X$:

$$\begin{aligned} x \in f^{-1}(A' \cup B') &\iff f(x) \in A' \cup B' & \text{(Definition of inverse image)} \\ &\iff (f(x) \in A') \lor (f(x) \in B') & \text{(Definition of set union)} \\ &\iff (x \in f^{-1}(A')) \lor (x \in f^{-1}(B')) & \text{(Definition of inverse image)} \\ &\iff x \in f^{-1}(A') \cup f^{-1}(B') & \text{(Definition of set union)} \\
& & \text{(6)}
\end{aligned}$$

Because each step is a logical equivalence ($\iff$), the set identity $f^{-1}(A' \cup B') = f^{-1}(A') \cup f^{-1}(B')$ holds directly for any mapping $f$.
$$\textbf{Q.E.D}$$