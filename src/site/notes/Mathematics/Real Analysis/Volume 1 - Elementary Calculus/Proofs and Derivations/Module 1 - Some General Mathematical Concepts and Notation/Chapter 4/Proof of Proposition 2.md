---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-4/proof-of-proposition-2/","dg-note-properties":{}}
---

### Part 1: $f^{-1}(A' \setminus B') = f^{-1}(A') \setminus f^{-1}(B')$
To establish set equality, a continuous chain of logical equivalences is demonstrated for an arbitrary element $x \in X$:
$$\begin{aligned} x \in f^{-1}(A' \setminus B') &\iff f(x) \in A' \setminus B' & \text{(Definition of inverse image)} \\ &\iff (f(x) \in A') \land (f(x) \notin B') & \text{(Definition of set difference)} \\ &\iff (x \in f^{-1}(A')) \land (x \notin f^{-1}(B')) & \text{(Definition of inverse image)} \\ &\iff x \in f^{-1}(A') \setminus f^{-1}(B') & \text{(Definition of set difference)} & & \text{(1)}
\end{aligned}$$
Because every step is a logical equivalence ($\iff$), the set identity $f^{-1}(A' \setminus B') = f^{-1}(A') \setminus f^{-1}(B')$ holds.

# Part 2: $f^{-1}(C_Y (A') = C_X f^{-1}(A')$

### Proof Method 1: Direct Application of Set Difference (Part 1)
Since $f: X \to Y$ is a well-defined mapping from domain $X$ to codomain $Y$, every element $x \in X$ maps into $Y$. Thus, the inverse image of the total codomain is the total domain:
$$f^{-1}(Y) = X \tag{2}$$

Applying part 1 with $A' = Y$ and $B' = A'$:
$$f^{-1}(\mathcal{C}_Y A') = f^{-1}(Y \setminus A') = f^{-1}(Y) \setminus f^{-1}(A') = X \setminus f^{-1}(A') = \mathcal{C}_X f^{-1}(A') \tag{3}$$
Therefore, $f^{-1}(\mathcal{C}_Y A') = \mathcal{C}_X f^{-1}(A')$. 
$$\textbf{Q.E.D}$$

### Proof Method 2: Pointwise Verification
Alternatively, for an arbitrary element $x \in X$:
$$\begin{aligned} x \in f^{-1}(C_Y(A')) &\iff f(x) \in C_Y(A') & \text{(Definition of inverse image)} \\ &\iff (f(x) \in Y) \land (f(x) \notin A') & \text{(Definition of relative complement)} \\ &\iff (x \in X) \land (x \notin f^{-1}(A')) & \text{(Since } f: X \to Y \text{ and definition of } f^{-1}\text{)} \\ &\iff x \in C_X f^{-1}(A') & \text{(Definition of relative complement)} \\
& & \text{(4)} \end{aligned}$$
Because each step is a logical equivalence ($\iff$), $f^{-1}(C_Y A') = C_X f^{-1}(A')$ holds.
$$\textbf{Q.E.D}$$