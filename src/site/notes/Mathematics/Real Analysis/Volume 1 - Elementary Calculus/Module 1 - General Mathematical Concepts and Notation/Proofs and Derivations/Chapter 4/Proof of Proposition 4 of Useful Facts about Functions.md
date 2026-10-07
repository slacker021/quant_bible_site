---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-4/proof-of-proposition-4-of-useful-facts-about-functions/","dg-note-properties":{}}
---

#  Proposition 1

### LHS ($\implies$)
Assume that $f: X \to Y$ is surjective and let $B' \subseteq Y$ be an arbitrary subset. From [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 1 - General Mathematical Concepts and Notation/Proofs and Derivations/Chapter 4/Proof of Proposition 3 of Useful Facts about Functions\|proposition 3]], the containment $f(f^{-1}(B')) \subseteq B'$ holds for any mapping $f$. To establish the reverse inclusion $B' \subseteq f(f^{-1}(B'))$, let $y \in B'$ be an arbitrary element. Since $f$ is surjective, there exists at least one element $x \in X$ such that $f(x) = y$. Because $f(x) = y \in B'$, by definition of the inverse image,
$$
x \in f^{-1}(B') \tag{1}
$$
Applying the direct image mapping to $x \in f^{-1}(B')$ gives:
$$f(x) \in f(f^{-1}(B')) \implies y \in f(f^{-1}(B')) \tag{2}$$
Thus, 
$$B' \subseteq f(f^{-1}(B')) \tag{3}$$
Combining both inclusions yields 
$$f(f^{-1}(B')) = B' \tag{4}$$

### RHS ($\impliedby$)
Assume that $f(f^{-1}(B')) = B'$ holds for every subset $B' \subseteq Y$. Choose $B' = Y$, the entire codomain. By assumption:
$$f(f^{-1}(Y)) = Y \tag{5}$$
Since $f^{-1}(Y) \subseteq X$ (by definition of pre-images), taking direct images gives
$$f(f^{-1}(Y)) \subseteq f(X) \tag{6}$$
Therefore, $Y = f(f^{-1}(Y)) \subseteq f(X) \subseteq Y$, which forces:
$$f(X) = Y \tag{7}$$
By definition, $f(X) = Y$ means that every element of the codomain $Y$ has at least one pre-image in $X$. Hence, $f$ is surjective.

---
#  Proposition 2

### LHS ($\implies$)
Assume $f: X \to Y$ is bijective. Since, $f$ is surjective, part 1 guarantees that $f(f^{-1}(B')) = B'$ for all $B' \subseteq Y$. Now, let $A \subseteq X$. From Proposition 3, $A \subseteq f^{-1}(f(A))$ holds for any mapping $f$. To establish $f^{-1}(f(A)) \subseteq A$, let $x \in f^{-1}(f(A))$. By definition of the pre-image, 
$$f(x) \in f(A) \tag{8}$$
By definition of the direct image,
$$f(x) \in f(A) \implies \exists a \in A \text{ such that } f(x) = f(a) \tag{9}$$
Since $f$ is injective (one-to-one),
$$f(x) = f(a) \implies x = a \tag{10}$$
Since $a \in A$, $x \in A$. Thus, 
$$f^{-1}(f(A)) \subseteq A \tag{11}$$
Combining inclusions yields 
$$f^{-1}(f(A)) = A \text{ for all } A \subseteq X \tag{12}$$

### RHS ($\impliedby$)
Assume that $f^{-1}(f(A)) = A$ for all $A \subseteq X$ and $f(f^{-1}(B')) = B'$ for all $B' \subseteq Y$. Since $f(f^{-1}(B')) = B'$ holds for all $B' \subseteq Y$, $f$ is surjective (according to part 1). Now, $x_1, x_2 \in X$ such that 
$$f(x_{1}) = f(x_{2}) \tag{13}$$
Consider the singleton subset $A = \{x_1\} \subseteq X$, which has a direct image of
$$f(A) = \{f(x_1)\} \tag{14}$$
Since $f(x_2) = f(x_1)$, 
$$f(x_2) \in f(A) \tag{15}$$
By definition of pre-images, 
$$f(x_2) \in f(A) \implies x_2 \in f^{-1}(f(A)) \tag{16}$$
By the starting premise, 
$$f^{-1}(f(A)) = A = \{x_1\} \tag{17}$$
Therefore,
$$x_2 \in \{x_1\} \implies x_2 = x_1 \tag{18}$$
Since $f(x_1) = f(x_2) \implies x_1 = x_2$, $f$ is injective. Because $f$ is both surjective and injective, $f$ is bijective.
$$\textbf{Q.E.D}$$