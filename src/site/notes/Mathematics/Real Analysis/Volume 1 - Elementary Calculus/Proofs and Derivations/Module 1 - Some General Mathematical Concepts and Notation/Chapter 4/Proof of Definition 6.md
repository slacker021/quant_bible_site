---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-4/proof-of-definition-6/","dg-note-properties":{}}
---

Let $X$ and $Y$ be non-empty sets, and let $f: X \to Y$ be a bijective mapping. The binary relation $f^{-1} \subseteq Y \times X$ defined by
$$f^{-1} := \{ (y, x) \in Y \times X \mid (x, y) \in f \} \tag{1}$$

# Part 1: Existence (Surjectivity of $f$)
Let $y \in Y$ be an arbitrary element of the domain of $f^{-1}$. Since $f: X \to Y$ is bijective, $f$ is in particular **surjective** (onto). By the definition of surjectivity, for every $y \in Y$, there exists at least one element $x \in X$ such that $f(x) = y$, which in set-theoretic relation terms means
$$
(x,y) \in f \tag{2}
$$
By the set-builder definition of $f^{-1}$:
$$(x, y) \in f \implies (y, x) \in f^{-1} \tag{3}$$
Thus, for every $y \in Y$, there exists at least one $x \in X$ such that
$$(y, x) \in f^{-1} \tag{4}$$
# Part 2: Uniqueness (Injectivity of $f$)
Let $y \in Y$ be an arbitrary element, and suppose there exist elements $x_1, x_2 \in X$ such that
$$(y, x_1) \in f^{-1} \text{ and } (y, x_2) \in f^{-1} \tag{5}$$ By definition of $f^{-1}$, this implies:
$$(x_1, y) \in f \quad \text{and} \quad (x_2, y) \in f \tag{6}$$In function notation, $f(x_1) = y$ and $f(x_2) = y$, which yields $f(x_1) = f(x_2)$. Since $f: X \to Y$ is bijective, $f$ is in particular injective. By definition of injectivity, 
$$
f(x_1) = f(x_2) \implies x_1 = x_2 \tag{7}
$$
Therefore, the element $x \in X$ assigned to $y$ by $f^{-1}$ is unique.

Because $f^{-1}$ satisfies both existence and uniqueness for every element $y \in Y$, the binary relation $f^{-1}$ is a well-defined mapping $f^{-1}: Y \to X$.
$$\textbf{Q.E.D}$$

