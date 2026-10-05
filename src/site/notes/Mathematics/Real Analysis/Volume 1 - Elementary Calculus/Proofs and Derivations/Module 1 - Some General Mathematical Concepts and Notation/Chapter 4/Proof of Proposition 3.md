---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-4/proof-of-proposition-3/","dg-note-properties":{}}
---

# Part 1: $A \subseteq f^{-1}(f(A))$
Let $x \in A$ be an arbitrary element. By definition of the direct image under $f$,
$$
x \in A \implies f(x) \in f(A) \tag{1}
$$
Now, the definition of the inverse image (pre-image) for any subset $S \subseteq Y$ is
$$f^{-1}(S) := \{ z \in X \mid f(z) \in S \} \tag{2}$$
Instantiating $S = f(A)$ yields
$$f^{-1}(f(A)) = \{ z \in X \mid f(z) \in f(A) \} \tag{3}$$
Since $f(x) \in f(A)$, the element $x$ satisfies the defining condition $f(x) \in f(A)$, which implies
$$x \in f^{-1}(f(A)) \tag{4}$$
Because $x \in A \implies x \in f^{-1}(f(A))$ for all $x \in A$, it follows that 
$$A \subseteq f^{-1}(f(A)) \tag{5}$$

# Part 2: $f(f^{-1}(B')) \subseteq B'$
Let $y \in f(f^{-1}(B'))$ be an arbitrary element. By definition of the direct image, $y \in f(f^{-1}(B'))$ implies that there exists at least one element $x \in f^{-1}(B')$ such that $f(x) = y$. By definition of the inverse image, 
$$
x \in f^{-1}(B') \implies f(x) \in B' \tag{6}
$$
Substituting $y = f(x)$ yields $y \in B'$. Because $y \in f(f^{-1}(B')) \implies y \in B'$ for all $y \in f(f^{-1}(B'))$, it follows that 
$$f(f^{-1}(B')) \subseteq B' \tag{7}$$
$$\textbf{Q.E.D}$$
