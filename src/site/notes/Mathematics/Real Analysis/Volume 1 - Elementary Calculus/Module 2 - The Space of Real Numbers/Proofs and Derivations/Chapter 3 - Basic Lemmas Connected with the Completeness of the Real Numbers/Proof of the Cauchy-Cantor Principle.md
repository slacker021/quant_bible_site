---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-3-basic-lemmas-connected-with-the-completeness-of-the-real-numbers/proof-of-the-cauchy-cantor-principle/","dg-note-properties":{}}
---

For any two closed intervals $I_{m} = [a_{m}, b_{m}]$ and $I_{n} = [a_{n}, b_{n}$ ] of the sequence, it's inferred that $a_{m} \le b_{m}$. Otherwise, there would be a $a_{n} \le b_{n} < a_{m} \le b_{m}$, that is, the intervals $I_{m}$ and $I_{n}$ would be mutually disjoint, while one of them—which is the one with the larger index—is contained in the other. 

Thus, the numerical sets $A = \{a_{m} \ | \ m \in \mathbb{N} \  \}$ and $B = \{b_{n} \in \ | \ n \in \mathbb{N} \}$ satisfy the hypotheses of the axiom of the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|completeness]], because there's a number $c \in \mathbb{R}$ such that $a_{m} \le c \le b_{n}$ for all $a_{m} \in A$ and all $b_{n} \in B$. In particular $a_{n} \le c \le b_{n}$ for all $n \in \mathbb{N}$. But that would mean point $c$ belongs to all the intervals $I_{n}$. 

Lastly, let $c_{1}$ and $c_{2}$ be two points with this property. If they're different, say $c_{1} < c_{2}$, then for any $n \in \mathbb{N}$, there is $a_{n} \le c_{1} < c_{2} \le b$, and therefore $0 < c_{2} - c_{1} < b_{n} - a_{n}$, so that the length of an interval in the sequence cannot be less than $c_{2} - c_{1}$. Hence if there're intervals of arbitrarily small length in the sequence, their common point is unique. 
$$
\textbf{Q.E.D}
$$
