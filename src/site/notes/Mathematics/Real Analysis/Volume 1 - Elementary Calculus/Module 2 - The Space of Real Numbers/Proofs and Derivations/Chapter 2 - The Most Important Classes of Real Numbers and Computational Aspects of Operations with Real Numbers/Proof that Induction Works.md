---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-induction-works/","dg-note-properties":{}}
---

Let $E$ be a subset of the natural numbers $\mathbb{N}$ satisfying the two hypotheses of the theorem:
$$
\begin{gather}
E \subset \mathbb{N} \\[2mm]
1 \in E \quad \wedge \quad \forall x \in \mathbb{R} \ (x \in E \implies (x + 1) \in E) \tag{1}
\end{gather}
$$
By the definition of an [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers\|inductive set]], the second condition in step 1 establishes that $E$ is itself an inductive subset of $\mathbb{R}$ containing the element $1$.

Recall that the set of natural numbers $\mathbb{N}$ is defined as the *smallest* inductive set containing $1$—that is, the intersection of the family $\mathcal{I}_1$ of all inductive subsets of $\mathbb{R}$ that contain $1$:
$$
\begin{gather}
\mathbb{N} := \bigcap_{X \in \mathcal{I}_1} X \tag{2}
\end{gather}
$$
Because $E$ is an inductive set containing $1$, $E$ is a member of the family $\mathcal{I}_1$. Since the intersection of a family of sets is a subset of every individual set in that family, it follows from step 2 that
$$
\begin{gather}
\mathbb{N} \subset E \tag{3}
\end{gather}
$$
Combining the initial hypothesis $E \subset \mathbb{N}$ from step 1 with the reverse inclusion $\mathbb{N} \subset E$ from step 3 yields, by the axiom of set extensionality,
$$
\begin{gather}
E = \mathbb{N} \tag{4}
\end{gather}
$$

>[!info]+ Remark: Predicate Formulation of Induction
>When the Principle of Induction is applied to a logical predicate $P(n)$ defined for $n \in \mathbb{N}$, one defines the truth set $E := \{n \in \mathbb{N} \mid P(n) \text{ is true}\}$. Verifying the base case $P(1)$ establishes $1 \in E$, and verifying the inductive step $P(k) \implies P(k + 1)$ establishes $k \in E \implies (k + 1) \in E$. By step 4, $E = \mathbb{N}$, confirming that $P(n)$ holds for all $n \in \mathbb{N}$.

$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$