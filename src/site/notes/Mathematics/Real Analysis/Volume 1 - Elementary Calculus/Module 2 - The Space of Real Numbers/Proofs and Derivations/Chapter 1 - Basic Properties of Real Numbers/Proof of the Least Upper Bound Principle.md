---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-1-basic-properties-of-real-numbers/proof-of-the-least-upper-bound-principle/","dg-note-properties":{}}
---

Let $X \subset \mathbb{R}$ be a given set and $Y = \{ y \in \mathbb{R} \ | \ \forall x \in X (x \le y) \}$. By hypothesis, $X \ne \emptyset$ and $Y = \emptyset$. By the axiom of completeness, 
$$
c \in \mathbb{R} \text{ such that } \forall x \in X \ \forall y \in Y \ (x \le c \le y) \tag{1}  
$$
The number $c$ is therefore simultaneously the *majorant* (upper bound) of $X$ and *minorant* (lower bound) of $Y$. Being a majorant of $X$, $c$ is an element of $Y$. However, as a minorant of $Y$, it must be the minimal element of $Y$. Therefore, 
$$
c = \text{min } Y = \text{sup } X \tag{2}
$$
$$
\textbf{Q.E.D}
$$
