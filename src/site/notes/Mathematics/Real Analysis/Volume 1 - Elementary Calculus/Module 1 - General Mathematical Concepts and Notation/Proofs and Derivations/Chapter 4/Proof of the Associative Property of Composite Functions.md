---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-4/proof-of-the-associative-property-of-composite-functions/","dg-note-properties":{}}
---

# Proposition 1
Consider $g \circ f$. Since $f: X \to Y$ and $g: Y \to Z$, the composition $g \circ f$ is a well-defined function $g \circ f: X \to Z$. Composing this with $h: Z \to W$ yields
$$h \circ (g \circ f) : X \to W \tag{1}$$
Additionally, consider $h \circ g$. Since $g: Y \to Z$ and $h: Z \to W$, the composition $h \circ g$ is a well-defined function $h \circ g: Y \to W$. Composing this with $f: X \to Y$ yields
$$(h \circ g) \circ f : X \to W \tag{2}$$
Both composite functions $h \circ (g \circ f)$ and $(h \circ g) \circ f$ map from the common domain $X$ into the common codomain $W$. 

---
#  Proposition 2
Let $x \in X$ be an arbitrary element of the domain.

### LHS
Evaluating the left-hand side at $x$ yields
$$\begin{aligned}
(h \circ (g \circ f))(x) &= h\big((g \circ f)(x)\big) & \text{(Definition of function composition)} \\ &= h\big(g(f(x))\big) & \text{(Definition of function composition)}  \\
& &\text{(3)}
\end{aligned}$$
### RHS
Evaluating the right-hand side at $x$ yields
$$
\begin{aligned} 
((h \circ g) \circ f)(x) &= (h \circ g)\big(f(x)\big) & \text{(Definition of function composition)} \\ &= h\big(g(f(x))\big) & \text{(Definition of function composition)} \\
& & \text{(4)}
\end{aligned}$$
Because $(h \circ (g \circ f))(x) = ((h \circ g) \circ f)(x) = h\big(g(f(x))\big)$ for every $x \in X$, and both composite functions possess the same domain $X$ and codomain $W$, it follows by the Axiom of Extensionality for functions that such that
$$h \circ (g \circ f) = (h \circ g) \circ f \tag{5}$$
$$\textbf{Q.E.D}$$

