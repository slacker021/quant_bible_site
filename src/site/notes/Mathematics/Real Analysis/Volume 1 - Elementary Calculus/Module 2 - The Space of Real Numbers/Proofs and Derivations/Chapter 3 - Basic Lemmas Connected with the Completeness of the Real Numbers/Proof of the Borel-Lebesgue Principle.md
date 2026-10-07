---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-3-basic-lemmas-connected-with-the-completeness-of-the-real-numbers/proof-of-the-borel-lebesgue-principle/","dg-note-properties":{}}
---

Let $S =\{U\}$ be a system of open intervals $U$ that cover the closed interval $[a,b] = I_{1}$. If the interval $I_{1}$ couldn't be covered by a finite set of intervals of the system $S$, then, dividing $I_{1}$ into two halves, one would find that at least one of the two halves, which is denoted by $I_{2}$, doesn't admit a finite covering. This procedure shall now be repeated with the interval $I_{2}$ and so on. 

In this way a nested sequence $I_{1} \supset I_{2} \supset \dots \supset I_{n} \supset \dots$ of closed intervals arises, none of which admit a covering by a finite subsystem of $S$. Since the length of the interval $I_{n}$ is $| I_{n} |$ is $|I_n| = |I_{1}| \cdot 2^{-n}$, the sequence $\{I_{n} \}$ contains intervals of arbitrarily small length (see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers\|computational aspects of real numbers]]). But the nested interval theorem implies that there's a point $c$ belonging to all of the intervals $I_{n}, n \in \mathbb{N}$. Since $c \in I_{1} = [a,b]$, there's an open interval $]\alpha,\beta[ = U \subset S$ containing $c$, such that $\alpha < c < \beta$. Let $\varepsilon = \text{min}(\{ c- \alpha, \beta - c \})$. In the sequence just constructed, an interval $I_{n}$ can be found such that $|I_{n}| < \varepsilon$. Since $c \in I_{n}$ and $|I_{n}| < \varepsilon$, it can be concluded that $I_{n} \subset U = ]\alpha,\beta[$. However, this contradicts the fact that $I_{n}$ can't be covered by a finite set of intervals from the system. 
$$
\textbf{Q.E.D}
$$



