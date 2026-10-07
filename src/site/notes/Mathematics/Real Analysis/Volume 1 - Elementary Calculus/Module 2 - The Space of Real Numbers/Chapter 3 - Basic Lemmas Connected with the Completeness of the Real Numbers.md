---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/chapter-3-basic-lemmas-connected-with-the-completeness-of-the-real-numbers/","dg-note-properties":{}}
---

# Basic Lemmas Connected with Completeness
In the study of real analysis, the axiom of completeness separates the set of real numbers $\mathbb{R}$ from the set of rational numbers $\mathbb{Q}$. It is the foundational principle that guarantees the real number line has no "gaps" or "holes." While the supremum and infimum principles establish this continuity algebraically, this underlying reality can be formulated in several geometrically and topologically intuitive ways.

These alternative formulations are often cited as the _basic lemmas of completeness_. In classical analysis, these lemmas serve as the operational machinery for proving the most critical theorems of calculus.

---
# The Nested Interval Lemma (Cauchy-Cantor Principle)
A functional application of the natural numbers and its inductive properties comes in the form of *sequences*: 
$$
\begin{gather}
\textbf{Definition: Sequence } \\
\text{A functional } f:\mathbb{N} \rightarrow \text{ of a natural-number argument is a sequuence, or more } \\
\text{specifically, a sequence of elements of } X. 
\end{gather}
$$
Multiple sequences can become subsets of one another, depending on the lower and upper bounds of the sequences:
$$
\begin{gather} \textbf{Definition: Sequence of Nested Intervals} \\[5mm] \text{A sequence of closed intervals } I_1, I_2, \dots, I_n, \dots \text{ is called nested if} \ I_1 \supset I_2 \supset \dots \supset I_n \supset \dots \\[2.5mm] \text{Symbolically, if } I_n = [a_n, b_n], \text{ then for all } n \in \mathbb{N}: \\ a_n \le a_{n+1} \le b_{n+1} \le b_n. \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers/Proof of the Cauchy-Cantor Principle\|proof]])

With the definition of both sequences and nested intervals having been established, several lemmas can be established. 

The geometric intuition is that these intervals narrow down as the index $n$ increases. The completeness of the real numbers guarantees that they must narrow down to at least one specific point: 
$$
\begin{gather} \textbf{Lemma: The Cauchy-Cantor Principle} \\[5mm] \text{For any sequence of nested closed intervals } I_1 \supset I_2 \supset \dots \supset I_n \supset \dots \ \text{there exists at least one point } \\ c \in \mathbb{R} \text{ that belongs to all of them. } \\ \text{Symbolically: } \bigcap_{n=1}^\infty I_n \neq \emptyset. \\[2.5mm] \text{If, moreover, for any } \epsilon > 0 \text{ there is an interval } I_n \text{ whose length } \ |I_n| = b_n - a_n \text{ is strictly less than } \epsilon, \\ \text{ then the point } c \text{ is unique.} \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers/Proof of the Cauchy-Cantor Principle\|proof]])

> [!danger]+ Intuition: Closed vs. Open Intervals
>  It is crucial that the intervals in the Cauchy-Cantor Principle are _closed_. If one considers a nested sequence of _open_ intervals, such as $I_n = (0, 1/n)$, the intersection $\bigcap_{n=1}^\infty (0, 1/n)$ is exactly empty. The endpoints must be included to capture the limiting boundary.

---
# The Finite Covering Lemma (Borel-Lebesgue Principle)

The next lemma transitions from examining nested sets to understanding how sets can be entirely covered by other subsets, introducing the concept of compactness in $\mathbb{R}$:
$$
\begin{gather}
\textbf{Definition: Cover} \\[5mm]
\text{A subset of a set } S = \{X\} \text{ of sets } X \text{ is said to cover a set } Y \text{ if } Y \subset \bigcup_{X \in S}X,  \\
\text{that is, if every element } y \in Y \text{belongs to at least one of the sets in the } \\
\text{system }S.  
\end{gather}
$$

$$
\begin{gather} \textbf{Lemma: The Borel-Lebesgue Principle (Heine-Borel Theorem)} \\[5mm] \text{Every open cover of a closed and bounded interval } [a,b] \\ \text{contains a finite subcover. That is, if } [a,b] \subset \bigcup_{\alpha \in A} U_\alpha, \text{ where } U_\alpha \text{ are open intervals,} \\ \text{then there exists a finite subset of indices } \alpha_1, \dots, \alpha_n \in A \text{ such that } \\[2.5mm] [a,b] \subset \bigcup_{i=1}^n U_{\alpha_i}. \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers/Proof of the Borel-Lebesgue Principle\|proof]])

> [!info]+ Remark: Necessity of Boundedness and Closedness 
> For the Borel-Lebesgue Principle to hold, the set must be both closed and bounded. For example, the open interval $(0, 1)$ can be covered by the infinite family of intervals $(1/n, 1)$, but no finite subset of this family will cover the entire interval $(0, 1)$. Similarly, the unbounded closed ray $[1, \infty)$ covered by $(0, n)$ has no finite subcover.

---
# The Limit Point Lemma (Bolzano-Weierstrass Principle)

The third and final major lemma deals with the accumulation of infinite points within a bounded spatial domain:
$$
\begin{gather} \textbf{Definition: Limit Point} \\[5mm] \text{A point } p \in \mathbb{R} \text{ is a limit point of a set } X \subset \mathbb{R} \\ \text{ if every } \ \epsilon\text{-neighborhood of } p \text{ contains infinitely many points of } X. \\ \text{Equivalently, every deleted neighborhood of } p \text{ contains at least} \ \text{one point of } X. \end{gather}
$$

$$
\begin{gather} \textbf{Lemma: The Bolzano-Weierstrass Principle} \\[5mm] \text{Every bounded infinite subset of the real numbers } \mathbb{R} \ \text{has at least one limit point in } \mathbb{R}. \end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers/Proof of the Bolzano-Weierstrass Principle\|proof]])

> [!info]+ Remark: Equivalence of the Completeness Lemmas 
> The Cauchy-Cantor Principle, the Borel-Lebesgue Principle, and the Bolzano-Weierstrass Principle are inextricably linked. Within the framework of Archimedean ordered fields, each of these three lemmas is logically equivalent to the Axiom of Completeness (the existence of a supremum). If any one of these lemmas is taken as an axiom instead, the others, including the Supremum Principle, can be derived as theorems.

---
# Additional Useful Facts
$$
\begin{gather}
\textbf{Lemma: } \\[5mm]
\text{If } I \text{ is any system of closed intervals, then } \\[2.5mm]
\text{sup}\{ a \in \mathbb{R} \ | \ [a,b] \in I \} = \alpha \le \beta = \text{inf}\{ b \in \mathbb{R} \ | \ [a,b] \in I \} \\[2.5mm]
\text{ and } \\[2.5mm]
[\alpha, \beta] = \bigcap_{[a.b] \in I} [a,b] 
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers/Proof of the First Useful Lemma\|proof]])

$$
\begin{gather}
\textbf{Theorem: Alternative Axiomatic Foundation} \\[5mm]
\text{An axiom system equivalent to the one that was established in the first chapter} \\
\text{of these notes can be obtained if one of the following previously-derived} \\
\text{facts are held in place of the axiom of completeness: } \\[2.5mm]
\text{1. Bolzano-Weierstrass} \\
\text{2. Borel-Legesgue} \\
\text{3. Cauchy-Cantor Principle}
\end{gather} 
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers/Proof that Different Axioms Can be Used\|proof]])