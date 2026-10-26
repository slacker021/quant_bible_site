---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/chapter-1-limits-of-sequences/","dg-note-properties":{}}
---

Measuring real physical quantities is an imperfect process that raises three fundamental questions:
1. What relation does the sequence of approximations so obtained bear to the quantity being measured? In mathematics, this translates to obtaining an exact expression of the sequence of multiple values that describes the value of the quantity being measured. Is this description unambiguous, or can the same sequence correspond to different values of the measured quantity?
2. How are arithmetic operations on the approximate values connected with the same operations on the exact values, and how can the operations that may legitimately be carried out by replacing exact values with approximate ones be characterized?
3. Can a given sequence of numbers be determined to be a sequence of arbitrarily precise approximations of the value of some quantity, or does the sequence fail to approach any definitive value at all?

These questions are resolved through the concept of a _limit_, which plays a foundational role throughout calculus. Both sequences and functions utilize this concept; indeed, real analysis fundamentally relies on the rigorous formulation of limits.

---
# Limit of a Sequence

### Definition
To analyze the asymptotic behavior of a sequence—how its terms behave as the index grows infinitely large, additional information must be provided for the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 3 - Basic Lemmas Connected with the Completeness of the Real Numbers\|definition of a sequence]] that was established earlier:  
- In this context, the values $f(n)$ of the function $f$ are the _terms_ of the sequence.
- A sequence is standardly denoted by assigning an indexed symbol to the element of the codomain $X$ corresponding to each $n \in \mathbb{N}$. Thus, setting $x_{n} := f(n)$, the sequence is denoted by $\{x_{n}\}_{n \in \mathbb{N}}$ (or simply $\{x_{n}\}$). 
- This is called a sequence in $X$ or a sequence of elements of $X$, where $x_{n}$ is the $n$-th term of the sequence.

> [!info]+ Remark: Numerical Sequences
> The most common type of sequence in classical analysis is a real numerical sequence $f : \mathbb{N} \rightarrow \mathbb{R}$. Such a mapping provides an infinite, countably ordered list of real values whose asymptotic behavior is the primary object of focus in the theory of sequence limits.

The convergence of a sequence is determined by whether its terms approach a specific, definitive real value as the index $n \rightarrow \infty$. The behavior the sequence exhibits as the index increases without bound is its asymptotic behavior:
$$
\begin{gather}
\textbf{Definition: Limit of a Sequence and Convergence} \\[5mm]
\text{A real number } A \text{ is the limit of a sequence } \{x_n\} \text{ if for every } \varepsilon > 0, \\[2mm]
\text{there exists a natural number } N \in \mathbb{N} \text{ such that for all } n > N, \\[2mm]
\text{the inequality } |x_n - A| < \varepsilon \text{ holds.} \\[3.5mm]
\lim_{n \to \infty} x_n = A := \forall \varepsilon > 0 \ \exists N \in \mathbb{N} \ \forall n > N \ (|x_n - A| < \varepsilon) \\[3.5mm]
\text{If such a limit } A \in \mathbb{R} \text{ exists, the sequence is said to converge (or tend) to } A, \\[2mm]
\text{and is called a convergent sequence. If a sequence does not possess a finite limit,} \\[2mm]
\text{it is called a divergent sequence.}
\end{gather}
$$

> [!danger]+ Intuition: Error Tolerance
> In the rigorous definition of a limit, the quantity $\varepsilon > 0$ acts as an arbitrary error tolerance constraint. Regardless of how stringent a level of precision $\varepsilon > 0$ is prescribed, there exists a threshold index $N \in \mathbb{N}$ such that the absolute error $|x_n - A|$ in approximating the exact limit $A$ by the terms $x_n$ of the sequence remains strictly less than $\varepsilon$ for all indices $n > N$. Notably, the definition of the limit does not provide an algorithm to compute the candidate value $A$ a priori; rather, it serves as the formal criterion to verify that a proposed value $A$ is indeed the limit.
> 
> The definition of the limit of a sequence when used in the context of proving its existence only works when one proposes a candidate limit value, which is a real number. 

Broadly speaking, two structural classifications of sequences frequently emerge during asymptotic analysis:
$$
\begin{gather}
\textbf{Definition: Ultimately Constant and Bounded Sequences} \\[5mm]
\text{If there exist a number } A \text{ and an index } N \in \mathbb{N} \text{ such that } x_{n} = A \text{ for all } n > N, \\[2mm]
\text{the sequence } \{x_{n}\} \text{ is called ultimately constant.} \\[3.5mm]
\text{A sequence } \{x_{n}\} \text{ is bounded if there exists a real number } M > 0 \\[2mm]
\text{such that } |x_{n}| < M \text{ for all } n \in \mathbb{N}.
\end{gather}
$$

### Basic Properties of Limits
With the formal definitions established, fundamental properties governing the topological and algebraic behavior of limits can be deduced:
$$
\begin{gather}
\textbf{Theorem: Basic Properties of Limits} \\[5mm]
\text{1. An ultimately constant sequence converges.} \\[2mm]
\text{2. Any neighborhood of the limit of a sequence contains all but a finite number} \\[2mm]
\text{of terms of the sequence.} \\[2mm]
\text{3. A convergent sequence has a unique limit.} \\[2mm]
\text{4. Every convergent sequence is bounded.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|proof]])

> [!warning]+ Warning: Convergence vs. Boundedness
> While convergence strictly implies boundedness, the converse is false. A bounded sequence can oscillate indefinitely—such as $x_n = (-1)^n$—without ever settling toward a single real value. To guarantee convergence in a bounded sequence, additional structural constraints, such as monotonicity, are required.

Because limits of real sequences are real numbers, standard arithmetic operations defined by the field axioms of addition and multiplication apply directly to convergent sequences:
$$
\begin{gather}
\textbf{Theorem: Arithmetic Properties of Limits} \\[5mm]
\text{If } \lim_{n \to \infty} x_{n} = A \text{ and } \lim_{n \to \infty} y_{n} = B, \text{ then:} \\[3.5mm]
\text{1. } \lim_{n \to \infty} (x_{n} + y_{n}) = A + B \\[2mm]
\text{2. } \lim_{n \to \infty} (x_{n} \cdot y_{n}) = A \cdot B \\[2mm]
\text{3. } \lim_{n \to \infty} \frac{x_n}{y_n} = \frac{A}{B}, \text{ provided } B \neq 0 \text{ and } y_{n} \neq 0 \text{ for all } n \in \mathbb{N}. \\[2mm]
\text{4. } \lim_{n \to \infty} (c x_{n}) = c A, \text{ where } c \in \mathbb{R} \text{ is a real-valued constant.} \\[2mm]
\text{5. } \lim_{n \to \infty} x_{n}^p = A^p, \text{ where } p \in \mathbb{R} \text{ is a real exponent, } x_{n} > 0, \text{ and } A > 0 \\[2mm]
\text{(or } x_n \ge 0 \text{ and } A \ge 0 \text{ when } p > 0\text{).}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|proof]])

Another consequence of sequence limits residing in $\mathbb{R}$ is that the order axioms can be applied to them, enabling bounded comparisons across sequences:
$$
\begin{gather}
\textbf{Theorem: Inequalities Involving Limits} \\[5mm]
\text{1. If } \{x_{n}\} \text{ and } \{y_{n}\} \text{ are two convergent sequences with } \lim_{n \to \infty} x_{n} = A \text{ and} \\[2mm]
\lim_{n \to \infty} y_{n} = B, \text{ where } A < B, \text{ then there exists an index } N \in \mathbb{N} \text{ such that} \\[2mm]
x_{n} < y_{n} \text{ for all } n > N. \\[3.5mm]
\text{2. Suppose the sequences } \{x_{n}\}, \{y_{n}\}, \text{ and } \{z_{n}\} \text{ satisfy } x_{n} \le y_{n} \le z_{n} \\[2mm]
\text{for all } n > N \text{ for some } N \in \mathbb{N}. \text{ If } \{x_{n}\} \text{ and } \{z_{n}\} \text{ both converge to the same limit } A, \\[2mm]
\text{then the intermediate sequence } \{y_{n}\} \text{ also converges to } A \text{ (The Squeeze Theorem).}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Inequalities Involving Limits\|proof]])

This ordered structure yields the following corollary governing the passage to the limit in strict and non-strict inequalities:
$$
\begin{gather}
\textbf{Corollary: Limit Inequalities} \\[5mm]
\text{Suppose } \lim_{n \to \infty} x_{n} = A \text{ and } \lim_{n \to \infty} y_{n} = B, \text{ and let } b \in \mathbb{R} \text{ be a constant.} \\[2mm]
\text{If there exists an index } N \in \mathbb{N} \text{ such that the given inequality holds for all } n > N, \text{ then:} \\[3.5mm]
\text{1. } (\forall n > N, \ x_{n} > y_{n}) \implies A \ge B \\[2mm]
\text{2. } (\forall n > N, \ x_{n} \ge y_{n}) \implies A \ge B \\[2mm]
\text{3. } (\forall n > N, \ x_{n} > b) \implies A \ge b \\[2mm]
\text{4. } (\forall n > N, \ x_{n} \ge b) \implies A \ge b
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Corollary for Limit Inequalities\|proof]])

> [!info]+ Remark: Strict Inequalities in Limits
> A strict inequality between sequence terms generally relaxes into a non-strict inequality in the limit. For instance, the strict inequality $\frac{1}{n} > 0$ holds for every $n \in \mathbb{N}$, yet $\lim_{n \to \infty} \frac{1}{n} = 0$.

The following theorem characterizes the convergence and limiting value of the geometric sequence $\{r^n\}$ across all possible real bases $r \in \mathbb{R}$:
$$
\begin{gather}
\textbf{Theorem: Convergence of the Geometric Sequence} \\[5mm]
\text{The geometric sequence } \{r^n\}_{n=1}^\infty \text{ converges if } -1 < r \le 1 \text{ and} \\[2mm]
\text{diverges for all other real values of } r \text{ (namely, } r \le -1 \text{ or } r > 1\text{). Furthermore:} \\[3.5mm]
\lim_{n \to \infty} r^n = \begin{cases}
0 & \text{if } -1 < r < 1 \\[2mm]
1 & \text{if } r = 1
\end{cases}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Theorem About r and n\|proof]])

Furthermore, the convergence of a sequence can be determined by partitioning its terms into even-indexed and odd-indexed progressions:
$$
\begin{gather}
\textbf{Theorem: Convergence via Even and Odd-Indexed Terms} \\[5mm]
\text{A sequence } \{x_{n}\} \text{ converges to a limit } A \in \mathbb{R} \text{ if and only if both} \\[2mm]
\lim_{n \to \infty} x_{2n} = A \quad \text{and} \quad \lim_{n \to \infty} x_{2n+1} = A.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Theorem Involving Odd and Even-Indexed Sequences\|proof]])

This theorem provides a necessary and sufficient condition for the convergence of a sequence: the parent sequence $\{x_n\}$ converges to $A$ if and only if its even-indexed terms $\{x_{2n}\}$ and odd-indexed terms $\{x_{2n+1}\}$ both converge to the common limit $A$. This technique is particularly effective for decomposing an oscillating or piecewise-defined sequence into two simpler progressions.

### Existence of Limits
Relying on an external candidate value $A$ to verify convergence is frequently impractical when the exact limit is unknown a priori. A purely internal criterion is therefore necessary—one that examines how the terms of the sequence behave relative to one another rather than comparing them against a predefined target:
$$
\begin{gather}
\textbf{Definition: Cauchy Sequence} \\[5mm]
\text{A sequence } \{x_{n}\} \text{ is called a fundamental sequence (or Cauchy sequence) if for every } \varepsilon > 0, \\[2mm]
\text{there exists an index } N \in \mathbb{N} \text{ such that } |x_{m} - x_{n}| < \varepsilon \text{ whenever } n > N \text{ and } m > N.
\end{gather}
$$

The completeness of the real numbers guarantees that this internal stabilization is both necessary and sufficient for convergence:
$$
\begin{gather}
\textbf{Theorem: Cauchy Criterion for Convergence} \\[5mm]
\text{A sequence of real numbers converges if and only if it is a Cauchy sequence.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Criterion for Sequences\|proof]])

The Cauchy Criterion is one of the most profound principles in mathematical analysis. It supplies an intrinsic test for convergence that depends solely on the mutual distances between terms of the sequence, eliminating the need to identify the limiting value beforehand.

A particularly important class of sequences arises when the terms consistently progress in a single direction as the index increases:
$$
\begin{gather}
\textbf{Definition: Monotonic Sequences} \\[5mm]
\text{1. A sequence } \{x_{n}\} \text{ is increasing (strictly increasing) if } x_{n} < x_{n+1} \text{ for all } n \in \mathbb{N}. \\[2mm]
\text{2. A sequence } \{x_{n}\} \text{ is nondecreasing if } x_{n} \le x_{n+1} \text{ for all } n \in \mathbb{N}. \\[2mm]
\text{3. A sequence } \{x_{n}\} \text{ is decreasing (strictly decreasing) if } x_{n} > x_{n+1} \text{ for all } n \in \mathbb{N}. \\[2mm]
\text{4. A sequence } \{x_{n}\} \text{ is nonincreasing if } x_{n} \ge x_{n+1} \text{ for all } n \in \mathbb{N}. \\[3.5mm]
\text{Sequences satisfying any of these four conditions are called monotonic.}
\end{gather}
$$

When paired with boundedness, monotonic sequences exhibit guaranteed convergence:
$$
\begin{gather}
\textbf{Theorem: Weierstrass Theorem on Monotonic Sequences} \\[5mm]
\text{1. A nondecreasing sequence } \{x_n\} \text{ converges if and only if it is bounded above,} \\[2mm]
\text{in which case } \lim_{n \to \infty} x_n = \sup_{n \in \mathbb{N}} x_n. \\[3.5mm]
\text{2. A nonincreasing sequence } \{x_n\} \text{ converges if and only if it is bounded below,} \\[2mm]
\text{in which case } \lim_{n \to \infty} x_n = \inf_{n \in \mathbb{N}} x_n.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|proof]])

This theorem directly facilitates the evaluation of fundamental root limits:
$$
\begin{gather}
\textbf{Corollary: Asymptotics of } n\textbf{-th Roots} \\[5mm]
\text{1. } \lim_{n \to \infty} \sqrt[n]{n} = 1 \\[2mm]
\text{2. } \lim_{n \to \infty} \sqrt[n]{a} = 1 \text{ for any constant } a > 0
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Corollary of the Weierstrass Theorem\|proof]])

Another critical application of the Weierstrass Theorem establishes the convergence of the sequence $\left\{\left(1 + \frac{1}{n}\right)^n\right\}$, which is strictly increasing and bounded above, thereby defining the foundational constant governing continuous compounding, growth, and decay:
$$
\begin{gather}
\textbf{Theorem and Definition: Euler's Number } (e) \\[5mm]
\text{The sequence } x_n = \left(1 + \frac{1}{n}\right)^n \text{ is strictly increasing and bounded above.} \\[2mm]
\text{Its finite limit defines Euler's number } e\text{:} \\[3.5mm]
e := \lim_{n \to \infty} \left(1 + \frac{1}{n} \right)^n
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Derivation of Euler's Constant\|proof]])

### Subsequences and Partial Limits
Analogous to extracting subsets in set theory, one can construct subsequences from a parent sequence by selecting an infinite progression of terms while strictly preserving their original index ordering:
$$
\begin{gather}
\textbf{Definition: Subsequence} \\[5mm]
\text{If } \{x_{n}\} \text{ is a sequence and } n_{1} < n_{2} < \dots < n_{k} < \dots \\[2mm]
\text{is a strictly increasing sequence of natural numbers, then the sequence } \{x_{n_k}\}_{k \in \mathbb{N}} \text{ given by} \\[2mm]
x_{n_{1}}, x_{n_{2}}, \dots , x_{n_{k}}, \dots \text{ is called a subsequence of the original sequence } \{x_{n}\}.
\end{gather}
$$

> [!example]- Example: Extracting a Subsequence
> The sequence $1, 3, 5, \dots$ of positive odd integers in their natural order is a valid subsequence of the parent sequence $1, 2, 3, \dots$ (corresponding to indices $n_k = 2k - 1$). However, the sequence $3, 1, 5, 7, 9, \dots$ is not a valid subsequence of $1, 2, 3, \dots$ because it violates the strictly increasing index condition $n_1 < n_2$.

Combining boundedness with the extraction of subsequences yields one of the most vital lemmas in real analysis:
$$
\begin{gather}
\textbf{Lemma: Bolzano-Weierstrass} \\[5mm]
\text{Every bounded sequence of real numbers contains a convergent subsequence.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Bolzano-Weierstrass Lemma\|proof]])

While an unbounded sequence may fail to converge to a finite real number, its asymptotic trajectory can still be rigorously classified if it escapes toward infinity:
$$
\begin{gather}
\textbf{Definition: Trending Towards Infinity} \\[5mm]
\text{1. A sequence } \{ x_{n} \} \text{ tends to positive infinity if for every real number } c \in \mathbb{R}, \text{ there exists } N \in \mathbb{N} \\[2mm]
\text{such that } x_{n} > c \text{ for all } n > N. \text{ Symbolically:} \\[3.5mm]
x_{n} \rightarrow +\infty := \forall c \in \mathbb{R} \ \exists N \in \mathbb{N} \ \forall n > N \ (x_{n} > c) \\[3.5mm]
\text{2. A sequence } \{ x_{n} \} \text{ tends to negative infinity if for every real number } c \in \mathbb{R}, \text{ there exists } N \in \mathbb{N} \\[2mm]
\text{such that } x_{n} < c \text{ for all } n > N. \text{ Symbolically:} \\[3.5mm]
x_{n} \rightarrow -\infty := \forall c \in \mathbb{R} \ \exists N \in \mathbb{N} \ \forall n > N \ (x_{n} < c) \\[3.5mm]
\text{3. A sequence } \{ x_{n} \} \text{ tends to unsigned infinity if for every real number } c \in \mathbb{R}, \text{ there exists } N \in \mathbb{N} \\[2mm]
\text{such that } |x_{n}| > c \text{ for all } n > N. \text{ Symbolically:} \\[3.5mm]
x_{n} \rightarrow \infty := \forall c \in \mathbb{R} \ \exists N \in \mathbb{N} \ \forall n > N \ (|x_{n}| > c)
\end{gather}
$$

> [!info]+ Remark: Unbounded Sequences Without an Infinite Limit
> A sequence may be unbounded without trending uniformly toward $+\infty$, $-\infty$, or $\infty$. For instance, the sequence $x_{n} = n^{(-1)^n}$ alternates between arbitrarily large even terms ($2k$) and arbitrarily small positive odd terms ($\frac{1}{2k-1}$), failing to satisfy $|x_n| > c$ for all $n > N$.

Nevertheless, every sequence of real numbers admits a subsequence with a definitive asymptotic fate:
$$
\begin{gather}
\textbf{Lemma: Subsequences and Infinity} \\[5mm]
\text{From every sequence of real numbers, one can extract either} \\[2mm]
\text{a convergent subsequence or a subsequence that tends to infinity.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that a Convergent Subsequence or Subsequence Tending to Infinity Can be Constructed From a Sequence of Real Numbers\|proof]])

Suppose that $\{x_{k}\}$ is a sequence of real numbers bounded below. For each $n \in \mathbb{N}$, one may define the tail infimum $i_{n} := \inf_{k \ge n} x_{k}$. Because taking the infimum over a progressively smaller set of indices cannot decrease its value, the sequence $\{i_n\}$ is nondecreasing ($i_{n} \le i_{n+1}$ for all $n \in \mathbb{N}$). Consequently, either $\{ i_{n} \}$ converges to a finite limit $\lim_{n \to \infty} i_{n} = l \in \mathbb{R}$ or $i_{n} \rightarrow +\infty$. Applying the dual reasoning to the tail supremum $s_n := \sup_{k \ge n} x_k$ motivates the definitions of the inferior and superior limits:
$$
\begin{gather}
\textbf{Definition: Inferior and Superior Limits} \\[5mm]
\text{1. The quantity } l = \lim_{n \to \infty} \left(\inf_{k \ge n} x_{k}\right) \text{ is called the inferior limit (or limit inferior) of } \{ x_{k} \}, \\[2mm]
\text{denoted by } \liminf_{k \to \infty} x_{k} \text{ or } \underline{\lim}_{k \to \infty} x_k. \text{ If } i_{n} = \inf_{k \ge n} x_k \rightarrow +\infty, \text{ then } \liminf_{k \to \infty} x_k := +\infty. \\[2mm]
\text{If } \{ x_{k} \} \text{ is unbounded below, then } i_{n} = -\infty \text{ for all } n \in \mathbb{N}, \text{ and } \liminf_{k \to \infty} x_k := -\infty. \\[3.5mm]
\text{2. The quantity } L = \lim_{n \to \infty} \left(\sup_{k \ge n} x_{k}\right) \text{ is called the superior limit (or limit superior) of } \{ x_{k} \}, \\[2mm]
\text{denoted by } \limsup_{k \to \infty} x_{k} \text{ or } \overline{\lim}_{k \to \infty} x_k. \text{ If } s_{n} = \sup_{k \ge n} x_{k} \rightarrow -\infty, \text{ then } \limsup_{k \to \infty} x_k := -\infty. \\[2mm]
\text{If } \{ x_{k} \} \text{ is unbounded above, then } s_{n} = +\infty \text{ for all } n \in \mathbb{N}, \text{ and } \limsup_{k \to \infty} x_k := +\infty.
\end{gather}
$$

The structural meaning of these asymptotic bounds is illuminated by examining the set of all possible subsequential limits of the parent sequence:
$$
\begin{gather}
\textbf{Definition: Partial Limit} \\[5mm]
\text{A real number } a \in \mathbb{R} \text{ (or one of the extended symbols } -\infty \text{ or } +\infty\text{) is called a partial limit} \\[2mm]
\text{of a sequence } \{x_n\} \text{ if there exists a subsequence } \{x_{n_k}\} \text{ that converges to } a \text{ (or tends to } -\infty \text{ or } +\infty\text{).}
\end{gather}
$$

The relationship between the set of partial limits and the inferior and superior limits is formalized in the following proposition:
$$
\begin{gather}
\textbf{Proposition: Inferior and Superior Partial Limits} \\[5mm]
\text{1. Both the inferior limit } \liminf_{n \to \infty} x_n \text{ and the superior limit } \limsup_{n \to \infty} x_n \text{ of a sequence } \{x_n\} \\[2mm]
\text{are themselves partial limits of } \{x_n\}\text{; in particular, if } \{x_n\} \text{ is bounded, both are finite real partial limits.} \\[3.5mm]
\text{2. For any sequence } \{x_n\}, \text{ the inferior limit is the smallest of its partial limits,} \\[2mm]
\text{and the superior limit is the largest of its partial limits.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that the Inferior (Superior) Limit is the Smallest (Largest) of its Partial Limits\|proof]])

From this proposition, essential corollaries governing overall sequence convergence emerge:
$$
\begin{gather}
\textbf{Corollary: Unification of Partial Limits} \\[5mm]
\text{1. A sequence } \{x_n\} \text{ converges to a finite limit } A \in \mathbb{R} \text{ (or tends to } -\infty \text{ or } +\infty\text{) if and only if} \\[2mm]
\text{its inferior and superior limits coincide: } \liminf_{n \to \infty} x_n = \limsup_{n \to \infty} x_n = A. \\[3.5mm]
\text{2. A sequence converges to } A \text{ if and only if every subsequence of it converges to } A. \\[3.5mm]
\text{3. The Bolzano-Weierstrass Lemma (both restricted and general forms)} \\[2mm]
\text{follows directly from the existence of the inferior and superior partial limits.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Corollary of Partial Limits Proposition\|proof]])

---
# Elementary Facts About Series

### The Sum of a Series and the Cauchy Criterion
Moving beyond individual sequences, mathematical analysis requires a rigorous framework for the infinite accumulation of terms, assigning a precise meaning to the formal infinite sum $a_1 + a_2 + \dots + a_n + \dots$:
$$
\begin{gather}
\textbf{Definition: Infinite Series} \\[5mm]
\text{The formal expression } a_1 + a_2 + \dots + a_n + \dots \text{ is denoted by the symbol } \sum_{n=1}^\infty a_n \\[2mm]
\text{and is called an infinite series (or simply a series). The numbers } a_n \text{ are the terms of the series,} \\[2mm]
\text{and the finite sum } s_n := \sum_{k=1}^n a_k \text{ is called the } n\text{-th partial sum of the series.}
\end{gather}
$$

The convergence of an infinite series is defined entirely through the asymptotic behavior of its sequence of partial sums $\{s_n\}$:
$$
\begin{gather}
\textbf{Definition: Convergence and Sum of a Series} \\[5mm]
\text{If the sequence of partial sums } \{s_n\} \text{ converges to a finite limit } s := \lim_{n \to \infty} s_n, \\[2mm]
\text{the series is said to converge, and the real number } s \text{ is called the sum of the series,} \\[2mm]
\text{denoted by } \sum_{n=1}^\infty a_n = s. \text{ If the sequence } \{s_n\} \text{ diverges, the series is said to diverge.}
\end{gather}
$$

Applying the Cauchy convergence criterion to the sequence of partial sums $\{s_n\}$ yields an equivalent internal criterion for the convergence of a series, along with a fundamental necessary condition on its individual terms:
$$
\begin{gather}
\textbf{Theorem: Cauchy Convergence Criterion for a Series} \\[5mm]
\text{The series } \sum_{n=1}^\infty a_n \text{ converges if and only if for every } \varepsilon > 0, \text{ there exists an index } N \in \mathbb{N} \\[2mm]
\text{such that for all } m \ge n > N, \text{ the inequality } \left| \sum_{k=n}^m a_k \right| < \varepsilon \text{ holds.} \\[5mm]
\textbf{Corollary: Necessary Condition for Series Convergence} \\[5mm]
\text{A necessary condition for the convergence of the series } \sum_{n=1}^\infty a_n \text{ is that} \\[2mm]
\text{its individual terms tend to zero as } n \to \infty\text{: } \lim_{n \to \infty} a_n = 0.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|proof]])

### Absolute Convergence and Comparison Tests
While the vanishing of terms ($\lim_{n \to \infty} a_n = 0$) is a necessary condition for convergence, it is not sufficient (as exemplified by the harmonic series $\sum_{n=1}^\infty \frac{1}{n}$). Furthermore, analyzing series whose terms alternate or vary arbitrarily in sign can be delicate. To address this, a stricter mode of convergence based on term magnitudes is introduced:
$$
\begin{gather}
\textbf{Definition: Absolute and Conditional Convergence} \\[5mm]
\text{A series } \sum_{n=1}^\infty a_n \text{ is called absolutely convergent if the series of absolute values } \sum_{n=1}^\infty |a_n| \text{ converges.} \\[2mm]
\text{If a series } \sum_{n=1}^\infty a_n \text{ converges, but the series } \sum_{n=1}^\infty |a_n| \text{ diverges, the series is called conditionally convergent.}
\end{gather}
$$

By virtue of the triangle inequality $\left| \sum_{k=n}^m a_k \right| \le \sum_{k=n}^m |a_k|$ and the Cauchy Criterion, every absolutely convergent series is guaranteed to converge in the ordinary sense:
$$
\begin{gather}
\textbf{Theorem: Absolute Convergence Implies Convergence} \\[5mm]
\text{If the series } \sum_{n=1}^\infty a_{n} \text{ is absolutely convergent, then it is also convergent.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Theorem of Absolute Convergence\|proof]])

This theorem serves as a bridge between the behavior of the magnitudes of the terms in a series and the convergence of the series itself. Consequently, to establish absolute convergence, one need only analyze series with non-negative terms. Because the partial sums $s_n = \sum_{k=1}^n a_k$ of a series with $a_n \ge 0$ form a nondecreasing sequence, the Weierstrass Theorem immediately yields:
$$
\begin{gather}
\textbf{Theorem: Convergence Criterion for Series with Non-Negative Terms} \\[5mm]
\text{A series } \sum_{n=1}^\infty a_n \text{ with non-negative terms } (a_n \ge 0 \text{ for all } n \in \mathbb{N}) \text{ converges} \\[2mm]
\text{if and only if its sequence of partial sums is bounded above.}
\end{gather}
$$

This bounding principle leads directly to the standard comparison test, wherein an unknown series is benchmarked against a series of known behavior:
$$
\begin{gather}
\textbf{Theorem: Standard Comparison Test} \\[5mm]
\text{Let } \sum_{n=1}^\infty a_n \text{ and } \sum_{n=1}^\infty b_n \text{ be two series with non-negative terms.} \\[2mm]
\text{If there exists an index } N \in \mathbb{N} \text{ such that } a_n \le b_n \text{ for all } n > N, \text{ then:} \\[3.5mm]
\text{1. The convergence of } \sum_{n=1}^\infty b_n \text{ implies the convergence of } \sum_{n=1}^\infty a_n. \\[2mm]
\text{2. The divergence of } \sum_{n=1}^\infty a_n \text{ implies the divergence of } \sum_{n=1}^\infty b_n.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Standard Comparison Test\|proof]])

An asymptotic formulation of the comparison principle compares the limiting ratio of the terms of two positive series:
$$
\begin{gather}
\textbf{Theorem: Limit Comparison Test} \\[5mm]
\text{Let } \sum_{n=1}^\infty x_{n} \text{ and } \sum_{n=1}^\infty y_{n} \text{ be two series with } x_{n} \ge 0 \text{ and } y_{n} > 0 \text{ for all } n \in \mathbb{N}. \\[2mm]
\text{If the limit } c = \lim_{n \to \infty} \frac{x_{n}}{y_{n}} \text{ exists and satisfies } 0 < c < +\infty, \text{ then either} \\[2mm]
\text{both series converge simultaneously or both series diverge simultaneously.}
\end{gather}
$$

Comparing an arbitrary series against a geometric series via the Standard Comparison Theorem yields the classical operational tests for series convergence:
$$
\begin{gather}
\textbf{Corollary: Standard Convergence Tests} \\[5mm]
\text{1. \textbf{Comparison Test for Absolute Convergence}: If } |x_n| \le y_n \text{ for all } n > N \text{ and } \sum_{n=1}^\infty y_n \text{ converges,} \\[2mm]
\text{then the series } \sum_{n=1}^\infty x_n \text{ converges absolutely.} \\[3.5mm]
\text{2. \textbf{Cauchy's Root Test}: Let } \alpha = \limsup_{n \to \infty} \sqrt[n]{|x_n|}. \text{ If } \alpha < 1, \text{ the series } \sum_{n=1}^\infty x_n \\[2mm]
\text{converges absolutely; if } \alpha > 1, \text{ the series } \sum_{n=1}^\infty x_n \text{ diverges.} \\[3.5mm]
\text{3. \textbf{d'Alembert's Ratio Test}: Suppose } x_n \neq 0 \text{ for all } n > N, \text{ and let } \alpha = \lim_{n \to \infty} \left| \frac{x_{n+1}}{x_n} \right|. \\[2mm]
\text{If } \alpha < 1, \text{ the series } \sum_{n=1}^\infty x_n \text{ converges absolutely; if } \alpha > 1, \text{ the series } \sum_{n=1}^\infty x_n \text{ diverges.} \\[3.5mm]
\text{4. \textbf{Divergence Test (n-th Term Test)}: If } \lim_{n \to \infty} x_{n} \text{ does not exist or } \lim_{n \to \infty} x_{n} \neq 0, \\[2mm]
\text{then the series } \sum_{n=1}^\infty x_{n} \text{ diverges.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Corollary for Standard Convergence Test\|proof]])

> [!warning]+ Warning: Inconclusiveness When $\alpha = 1$
> If $\alpha = 1$ in either Cauchy's Root Test or d'Alembert's Ratio Test, the test yields no information: a series with $\alpha = 1$ may either converge (such as $\sum_{n=1}^\infty \frac{1}{n^2}$) or diverge (such as $\sum_{n=1}^\infty \frac{1}{n}$), necessitating more refined convergence tests.

For series whose terms are non-negative and monotonically nonincreasing, Cauchy's condensation technique reduces convergence analysis to an exponentially condensed sub-series:
$$
\begin{gather}
\textbf{Proposition: Cauchy Condensation Test} \\[5mm]
\text{If } a_1 \ge a_2 \ge \dots \ge a_n \ge \dots \ge 0, \text{ then the series } \sum_{n=1}^\infty a_n \text{ converges if and only if} \\[2mm]
\text{the exponentially condensed series } \sum_{k=0}^\infty 2^k a_{2^k} \text{ converges.} \\[5mm]
\textbf{Corollary: Convergence of the p-Series} \\[5mm]
\text{The Dirichlet } p\text{-series } \sum_{n=1}^\infty \frac{1}{n^p} \text{ converges for } p > 1 \text{ and diverges for } p \le 1.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Condensation Test\|proof]])

### Arithmetic Properties of Series
Because the sum of a convergent series is the finite limit of its sequence of partial sums, convergent series obey linearity under termwise scalar multiplication and addition:
$$
\begin{gather}
\textbf{Proposition: Arithmetic Properties of Series} \\[5mm]
\text{If } \sum_{n=1}^\infty x_{n} \text{ and } \sum_{n=1}^\infty y_{n} \text{ are convergent series, then for any real constant } c \in \mathbb{R}\text{:} \\[3.5mm]
\text{1. } \sum_{n=1}^\infty (c x_{n}) = c \sum_{n=1}^\infty x_{n} \\[2mm]
\text{2. } \sum_{n=1}^\infty (x_{n} \pm y_{n}) = \sum_{n=1}^\infty x_{n} \pm \sum_{n=1}^\infty y_{n}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Properties of Series\|proof]])

### Series Rearrangement
If $\sigma : \mathbb{N} \rightarrow \mathbb{N}$ is a bijection of the set of natural numbers onto itself, the series $\sum_{n=1}^\infty x_{\sigma(n)}$ is called a _rearrangement_ of the original series $\sum_{n=1}^\infty x_n$. Whether the sum of a series remains invariant under arbitrary permutations of its terms depends entirely on whether the series converges absolutely or conditionally:
$$
\begin{gather}
\textbf{Proposition: Rearrangement of Series} \\[5mm]
\text{1. \textbf{Dirichlet's Theorem}: If } \sum_{n=1}^\infty x_{n} \text{ is absolutely convergent with sum } x, \text{ then every} \\[2mm]
\text{rearrangement } \sum_{n=1}^\infty x_{\sigma(n)} \text{ also converges absolutely and has the same sum } x. \\[3.5mm]
\text{2. \textbf{Riemann's Rearrangement Theorem}: If } \sum_{n=1}^\infty x_{n} \text{ is conditionally convergent and } y \in \mathbb{R} \\[2mm]
\text{is any prescribed real number, then there exists a rearrangement } \sum_{n=1}^\infty x_{\sigma(n)} \text{ that converges to } y.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Series Rearrangement Proposition\|proof]])

### Alternating Series Test
When the terms of a series alternate in sign between positive and negative values, the series may converge even when the sum of the absolute values of its terms diverges. Before attempting to evaluate the exact sum of such a series, one can verify its convergence via Leibniz's criterion:
$$
\begin{gather}
\textbf{Theorem: Alternating Series Test (Leibniz's Test)} \\[5mm]
\text{Let } \sum_{n=1}^\infty x_{n} \text{ be an alternating series of the form } x_{n} = (-1)^n y_{n} \text{ or } x_{n} = (-1)^{n+1}y_{n}, \\[2mm]
\text{where } y_{n} \ge 0 \text{ for all } n \in \mathbb{N}. \text{ If } \{y_{n}\} \text{ is a nonincreasing sequence } (y_n \ge y_{n+1} \text{ for all } n \in \mathbb{N}) \\[2mm]
\text{and } \lim_{n \to \infty} y_{n} = 0, \text{ then the alternating series } \sum_{n=1}^\infty x_{n} \text{ converges.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Alternating Series Test\|proof]])

---
# Additional Useful Facts

### Binomial Theorem
A foundational algebraic identity utilized extensively in the analysis of sequences and series (such as proving the convergence of Euler's number $e$) is the *Binomial Theorem*. Known variously in the mathematical literature as the *binomial formula*, *binomial expansion*, or *binomial identity*, its finite algebraic formulation is given as follows:
$$
\begin{gather}
\textbf{Theorem: Binomial Theorem} \\[5mm]
\text{For any real numbers } x, y \in \mathbb{R} \text{ and any non-negative integer } n \in \mathbb{N} \cup \{0\}\text{:} \\[3.5mm]
(x + y)^n = \sum_{k=0}^n \binom{n}{k} x^{n-k} y^k, \quad \text{where } \binom{n}{k} := \frac{n!}{k!(n - k)!}.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Binomial Theorem\|proof]])

### Squeeze Theorem and Absolute Value Convergence
Restating the bounding principle established in the second part of the Theorem on Inequalities Involving Limits provides the standalone formulation of the Squeeze Theorem:
$$
\begin{gather}
\textbf{Theorem: Squeeze Theorem} \\[5mm]
\text{Let } \{ a_{n} \}, \{ b_{n} \}, \text{ and } \{ x_{n} \} \text{ be sequences such that } a_{n} \le x_{n} \le b_{n} \text{ for all } n \in \mathbb{N} \text{ (or all } n > N\text{).} \\[2mm]
\text{If } \{ a_{n} \} \text{ and } \{ b_{n} \} \text{ converge to the same limit } \lim_{n \to \infty} a_{n} = \lim_{n \to \infty} b_{n} = x, \\[2mm]
\text{then } \{ x_{n} \} \text{ also converges and } \lim_{n \to \infty} x_{n} = x.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Squeeze Theorem\|proof]])

Applying the Squeeze Theorem to the inequality $-|x_n| \le x_n \le |x_n|$ yields a frequently used corollary characterizing sequences that converge to zero:
$$
\begin{gather}
\textbf{Corollary: Vanishing of Absolute Values} \\[5mm]
\text{For any sequence } \{x_n\}, \quad \lim_{n \to \infty} |x_{n}| = 0 \iff \lim_{n \to \infty} x_{n} = 0.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Corollary for the Squeeze Theorem of Limits\|proof]])

### Representing Values in Computational Bases
The following theorem is fundamental for distinguishing between rational and irrational quantities within positional numeral systems, characterizing how real numbers are represented in arbitrary computational bases:
$$
\begin{gather}
\textbf{Theorem: Periodicity of Rational } q\textbf{-ary Expansions} \\[5mm]
\text{A real number } x \in \mathbb{R} \text{ is rational if and only if its canonical } q\text{-ary expansion} \\[2mm]
\text{in any integer base } q \ge 2 \text{ is eventually periodic.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of q-ary Representation Theorem\|proof]])

### The Pigeonhole Principle
A critical step in many existence and periodicity proofs (including the proof of the $q$-ary expansion theorem above) consists of demonstrating that two indices in a finite state space must yield the same value. The *Pigeonhole Principle* (Dirichlet's Box Principle) formalizes this combinatorially:
$$
\begin{gather}
\textbf{Theorem: The Pigeonhole Principle} \\[5mm]
\text{If } n + 1 \text{ (or more) objects are distributed into } n \text{ boxes } (n \in \mathbb{N}), \\[2mm]
\text{then at least one box must contain at least two objects.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Pigeonhole Principle\|proof]])

> [!danger]+ Intuition: The Pigeonhole Principle
> In analytical proofs, the strategy is to define the "boxes" as equivalence classes or possible remainders (such as the $q$ possible remainders modulo $q$ in long division) and the "objects" as successive steps of an iterative process. Once the number of steps exceeds the number of available states, a repetition is guaranteed.

### Power Sums of the First $n$ Integers
In combinatorics, number theory, discrete calculus, and the evaluation of Riemann sums of polynomials, closed-form expressions for the power sums of the first $n$ positive integers are known as *Faulhaber's Formulae*. Formulating this theorem first requires defining a univariate polynomial:
$$
\begin{gather}
\textbf{Definition: Univariate Polynomial} \\[5mm]
\text{A univariate polynomial over } \mathbb{R} \text{ is a function } P : \mathbb{R} \rightarrow \mathbb{R} \text{ expressible as a finite linear} \\[2mm]
\text{combination of non-negative integer powers of a single variable } x\text{:} \\[3.5mm]
P(x) = a_{n}x^n + a_{n-1}x^{n-1} + \dots + a_{2}x^2 + a_{1}x + a_{0} \\[3.5mm]
\text{where } n \in \mathbb{N} \cup \{0\} \text{ and } a_0, a_1, \dots, a_n \in \mathbb{R} \text{ are real constants called the coefficients.} \\[2mm]
\text{If } a_n \neq 0, \text{ the non-negative integer } n \text{ is called the degree of the polynomial.}
\end{gather}
$$

With this definition established, the structure of power sums over finite integer ranges is given by Faulhaber's Theorem:
$$
\begin{gather}
\textbf{Theorem: Faulhaber's Formula} \\[5mm]
\text{For any non-negative integer } k \in \mathbb{N} \cup \{0\}, \text{ the sum of the } k\text{-th powers of the first } n \text{ positive} \\[2mm]
\text{integers, } S_{k}(n) := \sum_{i=1}^n i^k, \text{ is a polynomial in } n \text{ of degree } k + 1 \text{ with leading coefficient } a_{k+1} = \frac{1}{k + 1}\text{:} \\[3.5mm]
S_{k}(n) = \frac{1}{k + 1}n^{k+1} + a_{k}n^{k} + \dots + a_{1}n
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Derivation of Faulhaber's Formulae\|proof]])
