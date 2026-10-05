---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-4/proof-of-theorem-2/","dg-note-properties":{}}
---

# Part 1: Existence of an Injection ($\vert{}X\vert{} \le \vert{}\mathcal{P}(X)\vert{}$)
Define the mapping $f: X \to \mathcal{P}(X)$ by assigning to each element $x \in X$ its singleton set:
$$f(x) := \{x\} \tag{1}$$
Let $x_1, x_2 \in X$ and suppose $f(x_1) = f(x_2)$. By definition of $f$, 
$$\{x_1\} = \{x_2\} \tag{2}$$
By the Axiom of Extensionality, two singleton sets are equal if and only if their constituent elements are equal: 
$$x_1 = x_2 \tag{3}$$
Thus, $f$ is an injective mapping (one-to-one), establishing that
$$\vert{}X\vert{} \le \vert{}\mathcal{P}(X)\vert{} \tag{4}$$
# Part 2: Non-Existence of a Surjection ($\vert{}X\vert{} \neq \vert{}\mathcal{P}(X)\vert{}$)
Let $g: X \to \mathcal{P}(X)$ be an arbitrary mapping. To demonstrate that $g$ cannot be surjective, it suffices to construct a subset $D \in \mathcal{P}(X)$ that is not in the image of $g$. Construct the "diagonal" set $D$ consisting of all elements in $X$ that are not members of the subset to which $g$ maps them:
$$D := \{ x \in X \mid x \notin g(x) \} \tag{5}$$
Because $D$ is composed entirely of elements from $X$, $D \subseteq X$, which implies $D \in \mathcal{P}(X)$. Now, assume for the sake of contradiction that $g$ is surjective. If $g$ is surjective, then every element in the codomain $\mathcal{P}(X)$ has a pre-image in $X$. In particular, there must exist some element $d \in X$ such that
$$g(d) = D \tag{6}$$
Now, evaluate whether $d$ belongs to $D$:
$$
\begin{gather}
\text{Case 1: Assume } d \in D. \text{By definition of the set } D, d \in D \implies d \not\in g(d).  \\
\text{Since } g(d) = D, \text{ this yields } d \not\in D. \text{This is a contradiction.} \\[2.5mm]
\text{Case 2: Assume } d \not\in D. \text{ Since } g(d) = D, \text{ this means } d\not\in g(d). \\
 \text{By definition of the set } D, d \not\in g(D) \implies d \in d. \text{This is also a contradiction.} \tag{7}
\end{gather}
$$
In both cases, a logical contradiction is derived ($d \in D \iff d \notin D$). Therefore, the assumption that $g(d) = D$ for some $d \in X$ must be false. The set $D$ has no pre-image under $g$, meaning $g$ cannot be surjective.
$$\textbf{Q.E.D}$$