---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-4/proof-of-proposition-5-of-useful-facts-about-functions/","dg-note-properties":{}}
---


This proof is unique because the equivalence of these five statements is established via a circular chain of implications: 

#  Proposition 1
Assume $f$ is injective. Let $A \subseteq X$ be an arbitrary subset. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 1 - General Mathematical Concepts and Notation/Proofs and Derivations/Chapter 4/Proof of Proposition 3 of Useful Facts about Functions\|proposition 3]], the containment $A \subseteq f^{-1}(f(A))$ holds for any mapping $f$. To establish the reverse inclusion $f^{-1}(f(A)) \subseteq A$, let $x \in f^{-1}(f(A))$ be an arbitrary element. By definition of the inverse image,
$$x \in f^{-1}(f(A)) \implies f(x) \in f(A) \tag{1}$$
By definition of the direct image,
$$f(x) \in f(A) \implies \exists a \in A \text{ such that } f(x) = f(a) \tag{2}$$
Since $f$ is injective (one-to-one),
$$f(x) = f(a) \implies x = a \tag{3}$$
Since $a \in A$, it follows that $x \in A$. Thus, $f^{-1}(f(A)) \subseteq A$. Combining both inclusions yields 
$$f^{-1}(f(A)) = A \tag{4}$$

---
#  Proposition 2
Assume $f^{-1}(f(S)) = S$ holds for every subset $S \subseteq X$. Let $A, B \subseteq X$. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 1 - General Mathematical Concepts and Notation/Proofs and Derivations/Chapter 4/Proof of Proposition 1 of Useful Facts about Functions\|proposition 1]], the inclusion $$f(A \cap B) \subseteq f(A) \cap f(B) \tag{5}$$ holds for any mapping $f$. To establish the reverse inclusion
$$f(A) \cap f(B) \subseteq f(A \cap B) \tag{6}$$let $y \in f(A) \cap f(B)$ be an arbitrary element. By definition of set intersection, 
$$y \in f(A) \text{ and } y \in f(B) \tag{7}$$
By definition of direct images, there exist elements $a \in A$ and $b \in B$ such that 
$$f(a) = y \text{ and } f(b) = y \tag{8}$$
Let $x \in X$ be any element such that $f(x) = y$: 
$$
\begin{gather}
\text{Since } f(x) = y \in f(A), \text{ by definition of pre-images } x \in f^{-1}(f((A)).  \\
\text{By the initial premise of this part, } f^{-1}(f(A)) = A, \text{ so } x \in A. \\[2.5mm]
 

\text{Since } f(x) = y \in f(B), \text{ by definition of pre-images } x \in f^{-1}(f((B)).  \\
\text{By the initial premise of this part, } f^{-1}(f(B)) = B, \text{ so } x \in B. \tag{9}
\end{gather}
$$
Combining these gives
$$x \in A \cap B \tag{10}$$
Taking the direct image yields
$$f(x) = y \in f(A \cap B) \tag{11}$$
Thus, $f(A) \cap f(B) \subseteq f(A \cap B)$, establishing 
$$f(A \cap B) = f(A) \cap f(B) \tag{12}$$

---
#  Proposition 3

### LHS ($\implies$) 
Assume $f(A \cap B) = f(A) \cap f(B)$ for all $A, B \subseteq X$. By this premise, 
$$f(A \cap B) = f(A) \cap f(B) = \emptyset \tag{13}$$
If $A \cap B \neq \emptyset$, then by Proposition 1 (Fact 2), $f(A \cap B) \neq \emptyset$, which contradicts $f(A \cap B) = \emptyset$. Therefore, 
$$A \cap B = \emptyset \tag{14}$$
### RHS ($\impliedby$)
Applying the assumption of **LHS** directly:
$$f(A) \cap f(B) = f(A \cap B) = f(\emptyset) = \emptyset \tag{15}$$
Therefore,
$$f(A) \cap f(B) = \emptyset \iff A \cap B = \emptyset \tag{16}$$

---
#  Proposition 4
Assume $f(A) \cap f(B) = \emptyset \iff A \cap B = \emptyset$ for all $A, B \subseteq X$. Let $B \subseteq A \subseteq X$. 

### LHS (Forward Inclusion)
Since $A \setminus B \subseteq A$, taking direct images gives $f(A \setminus B) \subseteq f(A)$. By definition of set difference,
$$(A \setminus B) \cap B = \emptyset \tag{17}$$
Applying the forward direction of part 4 yields
$$f(A \setminus B) \cap f(B) = \emptyset \tag{18}$$
Since $f(A \setminus B)$ is contained in $f(A)$ and disjoint from $f(B)$, it must be contained in the difference:
$$f(A \setminus B) \subseteq f(A) \setminus f(B) \tag{19}$$

### RHS (Reverse Inclusion)
Let $y \in f(A) \setminus f(B)$. By definition, $y \in f(A)$ and $y \notin f(B)$. Since $y \in f(A)$, there exists $x \in A$ such that $f(x) = y$. If $x \in B$, then $f(x) = y \in f(B)$, which contradicts $y \notin f(B)$. Hence, $x \notin B$, which implies $x \in A \setminus B$. Taking the direct image gives
$$
f(x) = y \in f(A \setminus B) \tag{20}
$$
Thus, 
$$$f(A) \setminus f(B) \subseteq f(A \setminus B) \tag{21}$$
Combining inclusions gives $f(A \setminus B) = f(A) \setminus f(B)$

---
#  Proposition 5
Assume $f(A \setminus B) = f(A) \setminus f(B)$ whenever $B \subseteq A \subseteq X$. Let $x_1, x_2 \in X$ be distinct elements ($x_1 \neq x_2$). It must be shown that
$$f(x_1) \neq f(x_2) \tag{22}$$
Define the subsets $A = \{x_1, x_2\}$ and $B = \{x_2\}$, which implies that
$$
B \subseteq A \subseteq X \tag{23}
$$
The set difference is $A \setminus B = \{x_1\}$. Applying condition 5: 
$$f(\{x_1\}) = f(A \setminus B) = f(A) \setminus f(B) = f(\{x_1, x_2\}) \setminus f(\{x_2\}) \tag{24}$$
Evaluating the direct images yields:
$$\{f(x_1)\} = \{f(x_1), f(x_2)\} \setminus \{f(x_2)\} \tag{25}$$
If $f(x_1) = f(x_2)$, then $\{f(x_1), f(x_2)\} \setminus \{f(x_2)\} = \emptyset$, whereas $\{f(x_1)\} \neq \emptyset$. Thus, for the set equality to hold, it must be that
$$f(x_1) \neq f(x_2) \tag{26}$$
Therefore, $x_1 \neq x_2 \implies f(x_1) \neq f(x_2)$, proving $f$ is injective. 
$$\textbf{Q.E.D}$$
