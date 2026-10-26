---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/chapter-4-the-cardinality-of-the-continuum/","dg-note-properties":{}}
---

# Countable Sets
The formalization of equipotence enables the rigorous comparison of the cardinalities, or "sizes," of infinite sets. Using the set of natural numbers $\mathbb{N} := \{1, 2, 3, \dots\}$ as the foundational benchmark, it is possible to categorize infinite subsets of the real numbers $\mathbb{R}$ into distinct cardinal regimes. The most elementary class of infinite sets consists of those whose elements can be enumerated sequentially:
$$
\begin{gather}
\textbf{Definition: Countable Set} \\[5mm]
\text{A set } X \text{ is called countable (or countably infinite) if it is equipotent to the set of natural numbers } \mathbb{N}. \\[2mm]
\text{Equivalently, there exists a bijective mapping } f: \mathbb{N} \to X, \text{ allowing the} \\[2mm]
\text{elements of } X \text{ to be indexed as an infinite sequence } x_1, x_2, \dots, x_n, \dots. \\[3.5mm]
\text{A set that is either finite or countably infinite is called at most countable.}
\end{gather}
$$
Operating on countable and at most countable sets yields several foundational closure properties under standard set-theoretic operations:
$$
\begin{gather}
\textbf{Proposition: Subsets of Countable Sets} \\[5mm]
\text{Every subset of a countable set is at most countable} \\[2mm]
\text{(that is, any subset of a countable set is either finite or countably infinite).}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of First Proposition for Countable Sets\|proof]])

$$
\begin{gather}
\textbf{Proposition: Union of Countable Sets} \\[5mm]
\text{The union of a nonempty finite or countable family of at most countable sets is at most countable.} \\[2mm]
\text{In particular, the union of a nonempty finite or countable family of countable sets is a countable set.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of Proposition 2 for Countable Sets\|proof]])

Using Proposition 2, one can determine the exact cardinality of the rational numbers. Although the rational numbers are topologically dense across the entire real number line, their cardinal quantity remains strictly bound to the countable infinity of the natural numbers:
$$
\begin{gather}
\textbf{Theorem: Countability of Rational Numbers} \\[5mm]
\text{The set of all rational numbers } \mathbb{Q} \text{ is countable.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Countability of Rational Numbers\|proof]])

---
# Uncountable Sets and the Cardinality of the Continuum
Given that both the set of integers $\mathbb{Z}$ and the dense set of rational numbers $\mathbb{Q}$ are countable, it is natural to ask whether every infinite set is countable. As Georg Cantor demonstrated in 1874, the answer is decisively negative. There exist infinite sets whose cardinality is strictly greater than the countable infinity of the natural numbers:
$$
\begin{gather}
\textbf{Theorem: Uncountability of Real Numbers (Cantor's Diagonalization)} \\[5mm]
\text{The set of real numbers } \mathbb{R} \text{ is uncountable.} \\[2mm]
\text{Specifically, neither the open interval } ]0, 1[ \text{ nor the closed interval } [0, 1] \text{ can be placed} \\[2mm]
\text{in a bijective correspondence with the set of natural numbers } \mathbb{N}.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Uncountability of the Real Numbers\|proof]])

Cantor's theorem forces the recognition of a hierarchy of distinct infinities. To classify sets that share this higher order of infinity with the real number line—including every non-degenerate open interval $]a, b[$ and closed interval $[a, b]$—a specific cardinal designation is introduced:
$$
\begin{gather}
\textbf{Definition: Cardinality of the Continuum} \\[5mm]
\text{Any set that is equipotent to the set of real numbers } \mathbb{R} \text{ (or equivalently, to } [0, 1] \text{ or } ]0, 1[\text{)} \\[2mm]
\text{is said to have the cardinality of the continuum, denoted by the symbol } \mathfrak{c}.
\end{gather}
$$
Because the set of all real numbers $\mathbb{R}$ has the cardinality of the continuum $\mathfrak{c}$, whereas the subset of rational numbers $\mathbb{Q} \subset \mathbb{R}$ is merely countable, it follows that the overwhelming majority of points on the real number line are irrational:
$$
\begin{gather}
\textbf{Corollary: Uncountability of Irrational Numbers} \\[5mm]
\text{The set of irrational numbers } \mathbb{R} \setminus \mathbb{Q} \text{ has the cardinality of the continuum } \mathfrak{c} \\[2mm]
\text{and is therefore uncountable.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Uncountability of Irrational Numbers\|proof]])

> [!danger]+ Intuition: Topological Density Versus Cardinality
> The *topological* density of a set does not dictate its *cardinal* size. By the corollaries to the Principle of Archimedes, between any two distinct real numbers $a < b$, no matter how close, there lies at least one rational number. Yet, despite this ubiquitous density, the infinity of irrational numbers is strictly larger than the infinity of rational numbers. If a point is selected uniformly at random from the continuous interval $[0, 1]$, the probability of selecting a rational number is precisely zero. Measure-theoretically and cardinally, the real line is populated almost entirely by irrational numbers.

An even more striking classification arises when distinguishing real numbers by their algebraic structure. A real number is called *algebraic* if it is a root of a non-constant polynomial with integer coefficients (such as $\frac{3}{4}$ or $\sqrt{2}$), and *transcendental* otherwise (such as $e$ or $\pi$). Although proving that a specific constant is transcendental requires delicate analytical machinery, Cantor's cardinal arithmetic proves the existence—and preponderance—of transcendental numbers purely from set-theoretic principles:
$$
\begin{gather}
\textbf{Corollary: Existence of Transcendental Numbers} \\[5mm]
\text{The set of all real algebraic numbers } \mathbb{A} \subset \mathbb{R} \text{ (real roots of non-constant polynomial} \\[2mm]
\text{equations with integer coefficients) is countable. Consequently, the set of real transcendental} \\[2mm]
\text{numbers } \mathbb{T} := \mathbb{R} \setminus \mathbb{A} \text{ is nonempty, has the cardinality of the continuum } \mathfrak{c}, \text{ and is uncountable.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Existence of Transcendental Numbers\|proof]])
