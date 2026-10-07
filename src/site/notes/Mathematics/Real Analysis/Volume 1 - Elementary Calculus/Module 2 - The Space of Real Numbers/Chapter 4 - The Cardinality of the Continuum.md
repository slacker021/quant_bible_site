---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/chapter-4-the-cardinality-of-the-continuum/","dg-note-properties":{}}
---

# Countable Sets
The formalization of equipotence enables the rigorous comparison of the cardinalities, or "sizes," of infinite sets. Using the natural numbers $\mathbb{N} := \{1, 2, 3, \dots\}$ as the foundational metric, it is possible to categorize subsets of the real numbers $\mathbb{R}$ into distinct cardinal regimes. The most elementary class of infinite sets consists of those that can be enumerated sequentially:
$$
\begin{gather} \textbf{Definition: Countable Set} \\[5mm] \text{A set } X \text{ is countable if it is equipotent to the set of natural numbers } \mathbb{N}. \\ \text{In other words, there exists a bijective mapping } f: \mathbb{N} \to X, \text{ allowing the} \\ \text{elements of } X \text{ to be indexed as a sequence } x_1, x_2, \dots, x_n, \dots. \\[2.5mm] \text{Sets that are either finite or countable are often referred to as} \ \text{at most countable.} \end{gather}
$$
Operating on countable sets yields several foundational algebraic properties that act as closure mechanisms under standard set-theoretic operations: 
$$
\begin{gather} \textbf{Proposition: Subsets of Countable Sets} \\[5mm] \text{Every subset of a countable set is at most countable} \ \text{(that is, it is either finite or countable).} \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of First Proposition for Countable Sets\|proof]])

$$
\begin{gather} \textbf{Proposition: Union of Countable Sets} \\[5mm] \text{The union of a finite or countable family of countable sets is a countable set.} \end{gather}
$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of Proposition 2 for Countable Sets\|proof]])
Using Proposition 2, one can construct the cardinality of the rational numbers. Though the rational numbers appear ubiquitous and dense across the entire real number line, their quantity remains strictly bound to the cardinality of the natural numbers: 
$$
\begin{gather} \textbf{Theorem: Countability of Rational Numbers} \\[5mm] \text{The set of all rational numbers } \mathbb{Q} \text{ is countable.} \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Countability of Rational Numbers\|proof]])

---
# Uncountable Sets and the Cardinality of the Continuum
Given that the set of integers $\mathbb{Z}$ and the set of rational numbers $\mathbb{Q}$ are countable, it is a natural assumption that perhaps all infinite sets are countable. However, this is decisively false. There exist sets whose infinity is fundamentally larger and denser than the countable infinity of the natural numbers: 
$$
\begin{gather} \textbf{Theorem: Uncountability of Real Numbers (Cantor's Diagonalization)} \\[5mm] \text{The set of real numbers } \mathbb{R} \text{ is uncountable.} \\ \text{Specifically, the closed interval } [0,1] \subset \mathbb{R} \text{ cannot be placed in a } \\ \text{one-to-one correspondence with the natural numbers } \mathbb{N}. \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Uncountability of the Real Numbers\|proof]])
This theorem forces the acknowledgment of multiple, distinct layers of infinity. To rigorously classify sets that share this higher order of infinity with the real numbers, a specific cardinal designation is assigned:
$$
\begin{gather} \textbf{Definition: Cardinality of the Continuum} \\[5mm] \text{Any set that is equipotent to the set of real numbers } \mathbb{R} \\ \text{is said to have the cardinality of the continuum, denoted by the symbol } \mathfrak{c}. \end{gather}
$$
If the set of all real numbers $\mathbb{R}$ has the cardinality of the continuum, and the set of rational numbers $\mathbb{Q} \subset \mathbb{R}$ is merely countable, it logically follows that the "bulk" of the real number line is composed of elements that are not rational.

$$
\begin{gather} \textbf{Corollary: Uncountability of Irrational Numbers} \\[5mm] \text{The set of irrational numbers } \mathbb{R} \setminus \mathbb{Q} \text{ has the cardinality of the continuum} \\ \text{and is therefore uncountable.} \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Uncountability of Irrational Numbers\|proof]])

> [!danger]+ Intuition: The Density and Quantity of Numbers 
> The *topological* density of a set does not dictate its cardinality. Between any two distinct real numbers, no matter how close, there is always a rational number. Yet, despite this extreme density, the infinity of irrational numbers is strictly "larger" than the infinity of rational numbers. If one were to reach into the continuous interval $[0,1]$ and pull out a number perfectly at random, the probability of selecting a rational number is precisely zero. The real line is almost entirely populated by irrationals.

$$
\begin{gather} \textbf{Corollary: Existence of Transcendental Numbers} \\[5mm] \text{The set of all algebraic numbers (roots of non-zero polynomial equations with integer coefficients) } \\ \text{is countable. Since } \mathbb{R} \text{ is uncountable, there must exist real numbers that are not algebraic.} \\ \text{These are transcendental numbers, and the set of all transcendental numbers is uncountable.} \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Existence of Transcendental Numbers\|proof]]) 