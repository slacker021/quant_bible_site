---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-2/proof-of-proposition-1/","dg-note-properties":{}}
---

# Proof Method 1: Vacuous Truth
Let $A$ be any arbitrary set. By definition, a set $S$ is a subset of set $T$ if and only if every element of $S$ is also an element of $T$: 
$$S \subseteq T \iff \forall x \, (x \in S \implies x \in T) \tag{1}$$
Now, suppose that $S = \emptyset$ and $T = A$, the inclusion statement $\emptyset \subseteq A$ requires proving the conditional implication:
$$\forall x \, (x \in \emptyset \implies x \in A) \tag{2}$$
By the definition of the empty set $\emptyset$, there exists no element $x$ such that $x \in \emptyset$; the proposition $x \in \emptyset$ is false for every object $x$. This is considered a *vacuous truth*, where the statement
$$P \implies Q \tag{3}$$
evaluates to true if the antecedent $P$ is false. In this case, the statement is true whether $Q$ is true or false. Consequently, the implication $x \in \emptyset \implies x \in A$ holds vacuously for all $x$. 

Because every element of $\emptyset$ (of which there are none) is an element of $A$, it follows directly from the definition of subset inclusion that $\emptyset \subseteq A$.
$$\textbf{Q.E.D}$$
---
# Proof Method 2: Contradiction
Suppose that the empty set isn't a subset of any arbitrary set. This would imply that there's an element $x \in \emptyset$ but $x \notin A$, where $A$ is an arbitrary set. By definition of the subset, $\emptyset$ cannot be a subset of $A$. However, the definition of the empty set is that it's a set with no elements. This is a contradiction, which implies that the empty set must be a subset of any arbitrary set. 
$$\textbf{Q.E.D}$$
