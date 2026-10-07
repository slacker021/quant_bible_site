---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/chapter-1-limits-of-sequences/","dg-note-properties":{}}
---

Measuring real physical quantities is an imperfect process that raises three important questions:
1. What relation does the sequence of approximations so obtained have to the quantity being measured? In mathematics, this can be translated to obtaining an exact expression of the sequence of multiple values which describes the value of the quantity being measured. Is the description unambiguous, or can the same sequence correspond to different values of the measured quantity?
2. How are the operations on the approximate values connected with the same operations on the exact values, and how can the operations that can legitimately be carried out by replacing exact values with approximate ones be characterized?
3. Can the sequence of numbers be determined to be a sequence of arbitrarily precise approximations of the values of some quantity, or does the sequence not approach some value at all?

These questions are answered by the concept of a _limit_, which plays a fundamental role in calculus. Both sequences and functions utilize this concept. In fact, it can be argued that real analysis fundamentally relies on the rigorous formulation of limits.

---
# Limit of a Sequence

### Definition
To analyze the asymptotic behavior of a sequence—how its terms behave as the index grows infinitely large—it is necessary to establish precise definitions: 
$$\begin{gather} \textbf{Definition: Sequence } \\[5mm] \text{A function } f:\mathbb{N} \rightarrow X \text{ whose domain of definition is the } \\ \text{set of natural numbers is called a sequence in } X. \end{gather}$$

In this context, the values $f(n)$ of the function $f$ are the _terms_ of the sequence. An alternative way to denote a sequence is by assigning it a symbol for an element of the set into which the mapping goes. Thus, $x_{n} := f(n)$, with the sequence as a set being denoted as $\{x_{n}\}_{n \in \mathbb{N}}$. This is called the sequence in $X$ or a sequence of elements of $X$, where $x_{n}$ is the $n$th term of the sequence.

> [!info]+ Remark: Most Common Type of Sequence 
> The most common type of sequence is $f:\mathbb{N} \rightarrow \mathbb{R}$. In other words, most sequences map the natural numbers to the real numbers, providing an infinite ordered list of values whose asymptotic behavior is the fundamental object of focus in the analysis of the limit of sequences.

The convergence of a sequence is determined by whether its terms approach a specific, definitive value as the index $n \rightarrow \infty$.  The behavior the sequence demonstrates as it goes on is its asymptotic behavior:
$$\begin{gather} \textbf{Definition: Limit of a Sequence and Convergence} \\[5mm] \text{A real number } A \text{ is the limit of a sequence } \{x_n\} \text{ if for every } \varepsilon > 0, \\ \text{there exists a natural number } N \text{ such that for all } n > N, \\ \text{the inequality } \vert{}x_n - A\vert{} < \varepsilon \text{ holds.} \\ \text{If such a limit exists, the sequence is said to converge or tend to } A, \\ \text{ denoted as } \lim_{n \to \infty} x_n = A. \text{ Such a sequence is considered convergent.} \\ \text{If a sequence does not possess a limit, it is considered divergent.} \end{gather}$$

> [!danger]+ Intuition: Error Tolerance 
> In the context of the rigorous definition of a limit, the value $\varepsilon$ acts as an arbitrary error tolerance constraint. No matter what level of precision $\varepsilon > 0$ is prescribed, there is an index $N$ such that the absolute error in approximating the number $A$ by terms of the sequence $\{ x_{n} \}$ is strictly less than $\varepsilon$ as soon as $n > N$. The definition of the limit does not actually calculate the value of the limit itself; instead, it is used to rigorously prove that a proposed limit $A$ is indeed correct.

Broadly speaking, two structural classifications of sequences frequently emerge during asymptotic analysis: 
$$\begin{gather} \textbf{Definition: Constant and Bounded Sequences } \\[5mm] \text{If there is a number } A \text{ and an index } N \text{ such that } x_{n} = A \text{ for all } n > N, \\ \text{the sequence } \{x_{n}\} \text{ is ultimately constant. } \\ \text{A sequence } \{ x_{n} \} \text{ is bounded if there exists an } M \text{ such that } \vert{}x_{n}\vert{} < M \text{ for all } n \in \mathbb{N}. \end{gather}$$

### Basic Properties of Limits
With the formal definitions established, fundamental properties regarding the behavior and algebra of limits can be deduced.  

$$\begin{gather} \textbf{Theorem: Basic Properties of Limits} \\[5mm] \text{1. An ultimately constant sequence converges.} \\ \text{2. Any neighborhood of the limit of a sequence contains all but a finite number} \\ \text{of terms of the sequence.} \\ \text{3. A convergent sequence has a unique limit.} \\ \text{4. A convergent sequence is bounded.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|proof]])

> [!warning]+ Warning: Convergence vs. Boundedness
>  It is crucial to note that while convergence strictly implies boundedness, the converse is decisively false. A bounded sequence can oscillate indefinitely (e.g., $x_n = (-1)^n$) without ever settling toward a single point. To guarantee convergence in a bounded sequence, additional structural conditions, such as monotonicity, must be introduced.

Given that existent limits are real numbers, it naturally follows that standard arithmetic operations defined by the axioms of addition and multiplication apply directly to limits:  
$$\begin{gather} \textbf{Theorem: Arithmetic Properties of Limits} \\[5mm] \text{If } \lim_{ n \to \infty } x_{n} = A \text{ and } \lim_{ n \to \infty } y_{n} = B, \text{ then:} \\ \text{1. } \lim_{ n \to \infty }(x_{n} + y_{n}) = A + B \\ \text{2. } \lim_{ n \to \infty }(x_{n} \cdot y_{n}) = A \cdot B \\ \text{3. } \lim_{ n \to \infty } \frac{x_n}{y_n} = \frac{A}{B} \text{ if } B \neq 0 \text{ and } y_{n} \neq 0 \text{ for all } n. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|proof]])

Another consequence of sequence limits being real numbers is that the axioms of ordering can be applied to them, allowing for bounded comparisons:  
$$\begin{gather} \textbf{Theorem: Inequalities Involving Limits} \\[5mm] \text{1. If } \{x_{n}\} \text{ and } \{y_{n}\} \text{ are two convergent sequences with } \lim_{ n \to \infty } x_{n} = A \text{ and } \\ \lim_{ n \to \infty } y_{n} = B, \text{ where } A < B, \text{ then there exists an index } N \in \mathbb{N} \text{ such that } \\ x_{n} < y_{n} \text{ for all } n > N. \\ \text{2. Suppose the sequences } \{x_{n}\}, \{y_{n}\}, \text{ and } \{z_{n}\} \text{ are such that } x_{n} \le y_{n} \le z_{n} \\ \text{ for all } n > N \in \mathbb{N}. \text{ If } \{x_{n}\} \text{ and } \{z_{n}\} \text{ both converge to the same limit, } \\ \text{ then the sequence } \{ y_{n} \} \text{ also converges to that limit (The Squeeze Theorem). } \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Inequalities Involving Limits\|proof]])

This ordered structure yields the following corollary regarding strict and non-strict inequalities:  
$$\begin{gather} \textbf{Corollary: Limit Inequalities} \\[5mm] \text{Suppose } \lim_{ n \to \infty } x_{n} = A \text{ and } \lim_{ n \to \infty } y_{n} = B. \text{ If there exists an } N \text{ such that } \\ \text{for all } n > N, \text{ then:} \\ \text{1. } x_{n} > y_{n} \implies A \ge B \\ \text{2. } x_{n} \ge y_{n} \implies A \ge B \\ \text{3. } x_{n} > b \implies A \ge b \text{ (where } b \text{ is a constant)} \\ \text{4. } x_{n} \ge b \implies A \ge b \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Corollary for Limit Inequalities\|proof]])

> [!info]+ Remark: Strict Inequalities in Limits 
> It is worth noting that a strict inequality between sequence terms may degrade into an equality in the limit. For example, $\frac{1}{n} > 0$ for all $n \in \mathbb{N}$, yet the limit as $n \to \infty$ of $\frac{1}{n}$ is exactly $0$.

### Existence of Limits
Relying on an external candidate $A$ to verify convergence is frequently impractical. A purely internal criterion is necessary, one that examines how elements of the sequence behave relative to one another rather than comparing them to a predefined target:  
$$\begin{gather} \textbf{Definition: Cauchy Sequence } \\[5mm] \text{A sequence } \{x_{n}\} \text{ is a fundamental or Cauchy sequence if for any } \varepsilon > 0, \text{ there exists } \\ \text{an index } N \in \mathbb{N} \text{ such that } \vert{}x_{m} - x_{n}\vert{} < \varepsilon \text{ whenever } n > N \text{ and } m > N. \end{gather}$$
The completeness of the real numbers ensures that this internal stabilization perfectly aligns with standard convergence. 

$$\begin{gather} \textbf{Theorem: Cauchy Criterion for Convergence} \\[5mm] \text{A sequence of real numbers converges if and only if it is a Cauchy sequence.} \end{gather}$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Criterion for Sequences\|proof]])
The Cauchy Criterion is perhaps the most profound concept in early real analysis. It provides an internal test for convergence that relies solely on the distances between sequence terms, eliminating the need to propose a target limit beforehand. 

A specific type of sequence can be constructed depending on whether the size of the terms persistently increases or decreases as the sequence progresses:  
$$\begin{gather} \textbf{Definition: Monotonic Sequences} \\[5mm] \text{1. A sequence } \{x_{n}\} \text{ is increasing if } x_{n} < x_{n+1} \text{ for all } n \in \mathbb{N}. \\ \text{2. A sequence } \{x_{n}\} \text{ is nondecreasing if } x_{n} \ge x_{n+1} \text{ for all } n \in \mathbb{N}. \\ \text{3. A sequence } \{x_{n}\} \text{ is decreasing if } x_{n} > x_{n+1} \text{ for all } n \in \mathbb{N}. \\ \text{4. A sequence } \{x_{n}\} \text{ is nonincreasing if } x_{n} \le x_{n+1} \text{ for all } n \in \mathbb{N}. \\ \text{Sequences satisfying any of these conditions are considered monotonic.} \end{gather}$$

When combined with the concept of boundedness, monotonic sequences display a guaranteed convergence behavior:  
$$\begin{gather} \textbf{Theorem: Weierstrass Theorem on Monotonic Sequences} \\[5mm]\text{1. For a nondecreasing sequence to have a limit, it is necessary and sufficient} \\ \text{that it be bounded above.} \\ \text{2. For a nonincreasing sequence to have a limit, it is necessary and sufficient} \\ \text{that it be bounded below.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|proof]])

This theorem directly facilitates the evaluation of limits involving specific roots:
$$\begin{gather} \textbf{Corollary: } \\[5mm] \text{1. } \lim_{ n \to \infty } \sqrt[n]{n} = 1 \\ \text{2. } \lim_{ n \to \infty } \sqrt[n]{a} = 1 \text{ for any } a > 0 \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Corollary of the Weierstrass Theorem\|proof]])

Another critical limit derived from sequence analysis yields a foundational mathematical constant governing continuous growth and decay:  
$$\begin{gather} \textbf{Definition: Euler's Number } (e) \\[5mm] e := \lim_{ n \to \infty } \left(1 + \frac{1}{n} \right)^n \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Derivation of Euler's Constant\|proof]])

### Subsequences and Partial Limits
Similar to the concept of subsets in set theory, one can construct subsequences from parent sequences by maintaining the original ordering but skipping terms: 
$$\begin{gather} \textbf{Definition: Subsequences } \\[5mm] \text{If } \{x_{n}\} \text{ is a sequence and } n_{1} < n_{2} < \dots < n_{k} < \dots \\ \text{ is an increasing sequence of natural numbers, then the sequence } \\ x_{n_{1}}, x_{n_{2}}, \dots , x_{n_{k}}, \dots \text{ is a subsequence of the original sequence } \{x_{n}\}. \end{gather}$$

> [!example]- Example: Extracting a Subsequence 
> The sequence $1, 3, 5, \dots$ of positive odd integers in their natural order is a valid subsequence of the parent sequence $1, 2, 3, \dots$. However, the sequence $3, 1, 5, 7, 9, \dots$ is not a valid subsequence because it violates the strictly increasing index order of the original set.

The combination of boundedness and subsequences leads to one of the most vital lemmas in real analysis:  
$$\begin{gather} \textbf{Lemma: Bolzano-Weierstrass} \\[5mm] \text{Every bounded sequence of real numbers contains a convergent subsequence.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Bolzano-Weierstrass Lemma\|proof]])

While a sequence may not converge to a finite limit, its asymptotic behavior can still be rigorously classified if it escapes to infinity: 
$$\begin{gather} \textbf{Definition: Trending Towards Infinity} \\ \text{1. A sequence } \{ x_{n} \} \text{ tends to positive infinity if for each number } c, \text{ there is an } N \in \mathbb{N} \\ \text{ such that } x_{n} > c \text{ for all values of } n > N. \text{ This is symbolically denoted as:} \\ x_{n} \rightarrow +\infty := \forall c \in \mathbb{R}, \exists N \in \mathbb{N}, \forall n > N \ (x_{n} > c). \\ \text{2. A sequence } \{ x_{n} \} \text{ tends to negative infinity if for each number } c, \text{ there is an } N \in \mathbb{N} \\ \text{ such that } x_{n} < c \text{ for all values of } n > N. \text{ This is symbolically denoted as:} \\ x_{n} \rightarrow -\infty := \forall c \in \mathbb{R}, \exists N \in \mathbb{N}, \forall n > N \ (x_{n} < c). \\ \text{3. A sequence } \{ x_{n} \} \text{ tends to infinity if for each number } c, \text{ there is an } N \in \mathbb{N} \\ \text{ such that } \vert{}x_{n}\vert{} > c \text{ for all values of } n > N. \text{ This is symbolically denoted as:} \\ x_{n} \rightarrow \infty := \forall c \in \mathbb{R}, \exists N \in \mathbb{N}, \forall n > N \ (\vert{}x_{n}\vert{} > c). \end{gather}$$

> [!info]+ Remark: Unbounded but Without a Definitive Infinite Trend 
> A sequence may be unbounded but fail to trend uniformly toward positive, negative, or standard infinity. An example is the oscillating sequence $x_{n} = n^{(-1)^n}$, which jumps between large positive numbers and small fractions close to zero.

$$\begin{gather} \textbf{Lemma: Subsequences and Infinity} \\[5mm] \text{From each sequence of real numbers, one can extract either } \\ \text{a convergent subsequence or a subsequence that tends to infinity.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that a Convergent Subsequence or Subsequence Tending to Infinity Can be Constructed From a Sequence of Real Numbers\|proof]])

Suppose that $\{x_{k}\}$ is an arbitrary sequence of real numbers bounded below. It may be considered as the sequence $i_{n} = \inf_{k \ge n} x_{k}$. Since $i_{n} \le i_{n+1}$ for any $n \in \mathbb{N}$, either the sequence $\{ i_{n} \}$ has a finite limit $\lim_{n \to \infty} i_{n} = l$ or $i_{n} \rightarrow +\infty$. This behavior is generalized through the concepts of inferior and superior limits:  
$$\begin{gather} \textbf{Definition: Inferior and Superior Limits} \\[5mm] \text{1. The number } l = \lim_{ n \to \infty } \inf_{k \ge n} x_{k} \text{ is the inferior limit of the sequence } \{ x_{k} \}, \\ \text{ denoted as } \liminf_{k \to \infty} x_{k}. \text{ If } i_{n} \rightarrow +\infty, \text{ then the inferior limit equals } \\ \text{ positive infinity. If } \{ x_{k} \} \text{ is unbounded below, then } i_{n} = \inf_{k \ge n} x_{k} = -\infty, \\ \text{ meaning the inferior limit equals negative infinity.} \\ \text{2. The number } L = \lim_{ n \to \infty } \sup_{k \ge n} x_{k} \text{ is the superior limit of the sequence } \{ x_{k} \}, \\ \text{ denoted as } \limsup_{k \to \infty} x_{k}. \text{ If } s_{n} = \sup_{k \ge n} x_{k} \rightarrow -\infty, \text{ the superior limit} \\ \text{ equals negative infinity. If } \{ x_{k} \} \text{ is unbounded above, the superior limit} \\ \text{ equals positive infinity.} \end{gather}$$

The origin of these bounds can be explained by examining the possible convergent sub-paths of the parent sequence: 
$$\begin{gather} \textbf{Definition: Partial Limit} \\[5mm] \text{A number (or the symbols } -\infty \text{ or } +\infty \text{) is a partial limit of a sequence } \\ \text{if the sequence contains a subsequence converging to that number.} \end{gather}$$

The relationship between partial limits and the superior/inferior bounds is formalized as follows:  
$$\begin{gather} \textbf{Proposition: Inferior and Superior Partial Limits} \\[5mm] \text{1. The inferior and superior limits of a bounded sequence are, respectively, } \\ \text{the smallest and largest partial limits of the sequence.} \\ \text{2. For any sequence, the inferior limit is the smallest of its partial limits, } \\ \text{and the superior limit is the largest of its partial limits.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof that the Inferior (Superior) Limit is the Smallest (Largest) of its Partial Limits\|proof]])

From this proposition, essential corollaries regarding overall sequence convergence emerge:  
$$\begin{gather} \textbf{Corollary: Unification of Partial Limits} \\[5mm] \text{1. A sequence has a limit or tends to negative/positive infinity if and only if } \\ \text{its inferior and superior limits are exactly the same.} \\ \text{2. A sequence converges if and only if every subsequence of it converges.} \\ \text{3. The Bolzano–Weierstrass Lemma (both restricted and general forms)} \\ \text{follows directly from the existence of these partial limits.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Corollary of Partial Limits Proposition\|proof]])

---
# Elementary Facts About Series

### The Sum of a Series and the Cauchy Criterion
Moving beyond simple sequences, analysis requires a precise framework for dealing with the continuous accumulation of terms, assigning a rigorous mathematical meaning to the infinite sum $a_1 + a_2 + \dots + a_n + \dots$. This is a special type of sequence that is frequently encountered and very useful: 
$$\begin{gather} \textbf{Definition: Infinite Series} \\[5mm] \text{The expression } a_1 + a_2 + \dots + a_n + \dots \text{ is denoted by the symbol } \sum_{n=1}^\infty a_n \\ \text{and is called a series or an infinite series. The elements } a_n \text{ are the terms of the series, } \\ \text{and the finite sum } s_n = \sum_{k=1}^n a_k \text{ is called the } n\text{th partial sum of the series.} \end{gather}$$

The convergence of an infinite series is tied entirely to the asymptotic behavior of its sequence of partial sums:  
$$\begin{gather} \textbf{Definition: Convergence and Sum of a Series} \\[5mm] \text{If the sequence of partial sums } \{s_n\} \text{ converges, the series is said to converge. } \\ \text{If } \{s_n\} \text{ diverges, the series is considered divergent.} \\ \text{The limit } \lim_{n \to \infty} s_n = s \text{, if it exists, is the definitive sum of the series, } \\ \text{denoted as } \sum_{n=1}^\infty a_n = s. \end{gather}$$

By applying the Cauchy convergence criterion to the sequence of partial sums, an equivalent internal criterion for the convergence of a series is derived:  
$$\begin{gather} \textbf{Theorem: Cauchy Convergence Criterion for a Series} \\[5mm]\text{The series } \sum_{n=1}^\infty a_n \text{ converges if and only if for every } \varepsilon > 0 \text{ there exists an index } \\ N \in \mathbb{N} \text{ such that for all } m \ge n > N, \text{ the inequality } \left\vert{} \sum_{k=n}^m a_k \right\vert{} < \varepsilon \text{ holds.} \\ \textbf{Corollary: Necessary Condition for Series Convergence} \\ \text{A necessary condition for the convergence of the series } \sum_{n=1}^\infty a_n \text{ is that} \\ \text{its individual terms tend to zero: } \lim_{n \to \infty} a_n = 0. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Convergence Criterion for a Series\|proof]])

### Absolute Convergence and Comparison Tests
While the necessary condition is straightforward, analyzing series containing a mix of positive and negative terms can be difficult. Thus, a stricter form of convergence is defined to simplify stability tests: 
$$\begin{gather} \textbf{Definition: Absolute Convergence} \\[5mm] \text{The series } \sum_{n=1}^\infty a_n \text{ is absolutely convergent if the corresponding series} \\ \text{of absolute values } \sum_{n=1}^\infty \vert{}a_n\vert{} \text{ converges.} \end{gather}$$

Because of the triangle inequality $\left\vert{} \sum_{k=n}^m a_k \right\vert{} \le \sum_{k=n}^m \vert{}a_k\vert{}$, any absolutely convergent series is mathematically guaranteed to be convergent in the ordinary sense. Therefore, to test for absolute convergence, analysts only need to study series constructed with non-negative terms: 
$$\begin{gather} \textbf{Theorem: Convergence Criterion for Series with Non-negative Terms} \\[5mm] \text{A series } \sum_{n=1}^\infty a_n \text{ with } a_n \ge 0 \text{ converges if and only if } \\ \text{its sequence of partial sums is bounded above.} \end{gather}$$

This bounding logic leads to a highly practical evaluation method where unknown series are compared against known baseline series: 
$$\begin{gather} \textbf{Theorem: Comparison} \\[5mm] \text{Let } \sum_{n=1}^\infty a_n \text{ and } \sum_{n=1}^\infty b_n \text{ be two series with non-negative terms. } \\ \text{If there exists an index } N \in \mathbb{N} \text{ such that } a_n \le b_n \text{ for all } n > N, \text{ then:} \\ \text{1. The convergence of } \sum_{n=1}^\infty b_n \text{ strictly implies the convergence of } \sum_{n=1}^\infty a_n. \\ \text{2. The divergence of } \sum_{n=1}^\infty a_n \text{ strictly implies the divergence of } \sum_{n=1}^\infty b_n. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Comparison Theorem\|proof]])

The Comparison Theorem directly yields several robust algebraic tests used to rapidly determine series convergence:  
$$\begin{gather} \textbf{Corollary: Standard Convergence Tests} \\[5mm] \text{1. \textbf{Weierstrass M-Test}: If } \vert{}a_n\vert{} \le b_n \text{ for all } n > N \text{ and } \sum_{n=1}^\infty b_n \text{ converges, } \\ \text{then the original series } \sum_{n=1}^\infty a_n \text{ converges absolutely.} \\ \text{2. \textbf{Cauchy's Root Test}: Let } \alpha = \limsup_{n \to \infty} \sqrt[n]{\vert{}a_n\vert{}}. \text{ If } \alpha < 1, \text{ the series } \\ \text{converges absolutely; if } \alpha > 1, \text{ the series diverges.} \\ \text{3. \textbf{d'Alembert's Ratio Test}: Let } \alpha = \lim_{n \to \infty} \left\vert{} \frac{a_{n+1}}{a_n} \right\vert{}. \text{ If } \alpha < 1, \text{ the series } \\ \text{converges absolutely; if } \alpha > 1, \text{ the series diverges.} \end{gather}$$
Note that if $\alpha = 1$ in either Cauchy's or d'Alembert's tests, the methodology is inconclusive, requiring more advanced convergence tests. (see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Standard Convergence Tests\|proof]])

Finally, for sequences where the terms are strictly monotonic and decreasing towards zero, a highly specialized condensation test exists:  
$$\begin{gather} \textbf{Proposition: Cauchy Condensation Test} \\ \text{If } a_1 \ge a_2 \ge \dots \ge 0, \text{ the series } \sum_{n=1}^\infty a_n \text{ converges if and only if } \\ \text{the exponentially condensed series } \sum_{k=0}^\infty 2^k a_{2^k} \text{ converges.} \\ \textbf{Corollary: Convergence of the p-Series} \\ \text{The fundamental p-series } \sum_{n=1}^\infty \frac{1}{n^p} \text{ converges for } p > 1 \text{ and diverges for } p \le 1. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Cauchy Condensation Test\|proof]])

---
# Additional Useful Facts

### Binomial Theorem
An interesting application of series within mathematics is the *binomial theorem*. Although there're many closely related results that're known by this—with some results being variously known as the *binomial formula, binomial expansion, binomial identity, binomial series*, or *binomial expansion*. Below is the most general case of this interesting fact: 
$$
\begin{gather}
\textbf{Binomial Theorem: } \\[5mm]
(x + y)^n = \sum_{k=0}^n \binom{n}{k} x^{n-k} y^k
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Binomial Theorem\|proof]])

### Squeeze Theorem
The following is an intuitive theorem:
$$
\begin{gather}
\textbf{Squeeze Theorem:} \\[5mm]
\text{Let } \{ a_{n} \}, \{ b_{n} \}, \{ x_{n} \} \text{ be sequences such that for all } n \in \mathbb{N}, a_{n} \le x_{n} \le b_{k}.  \\
\text{Further suppose that } \{ a_{n} \} \text{ and } \{ b_{n} \} \text{ converge, where } \lim_{ n \to \infty }  a_{n} = \lim_{ n \to \infty }  b_{n} = x.  \\
\text{Therefore, } \{ x_{n} \} \text{ converges and } \lim_{ n \to \infty } x_{n} = x
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Squeeze Theorem\|proof]])

### Representing Values in Computational Bases
The following is crucial for distinguishing between discrete and continuous systems, being a cornerstone of positional notation and is essential for understanding how values in various computational bases are to be represented: 
$$
\begin{gather}
\textbf{Theorem: } \\[5mm]
\text{A real number } x \text{ is rational if and only if its } q\text{-ary expansion in any integer base } q \ge 2 \\
\text{is eventually periodic.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of q-ary Representation Theorem\|proof]])

### The Pigeonhole Principle
A key step in many proofs consists of showing two possibly different values are in fact the same. The *Pigeonhole Principle* is a simple yet elegant theorem demonstrating this:
$$
\begin{gather}
\textbf{Theorem: The Pigeonhole Principle} \\[5mm]
\text{If } n + 1 \text{ (or more) objects are put into } n \text{ boxes, then some box contains } \\
\text{ at least two objects.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Pigeonhole Principle\|proof]])
This seemingly simple fact has many uses. 

>[!danger]+ Intuition: The Pigeonhole Principle
> The key typically is to put objects into boxes according to some rule, so that when two objects end up in the same box it is because they have some desired relationship.

### Power Sums of the First $n$ Integers
In the broader scope of mathematics, these are known as *Faulhaber's Formulae*. These see heavy use in *combinatorics, number theory,* and *discrete calculus*. These serve as the foundation for understanding the sum of *polynomials* over finite ranges:
$$
\begin{gather}
\textbf{Definition: Univariate Polynomial}  \\[5mm]
\text{A univariate polynomial is an expression involving a sum of powers } \\
\text{in one variable multiplied by coefficients. This is expressed as } \\[2.5mm]
a_{n}x^n + \dots + a_{2}x^2 + a_{1} x + a_{0} \\[2.5mm]
\text{where } a \text{ is a coefficient and } x \text{ is a variable.} \text{ The degree of the polynomial is } \\
\text{ the highest power or exponent of a variabe in the expression. }
\end{gather}
$$
With that definition, the formula may be derived:
$$
\begin{gather}
\textbf{Theorem: Faulhaber's Formula} \\[5mm]
\text{For any non-integer } k \text{, the sum of the } k\text{-th powers of the first } n \text{ positive } \\
\text{integers, } S_{k}(n) = \sum_{i=1}^n i^k, \text{ is a polynomial in } n \text{ of degree } k + 1. \text{ Generally speaking, } \\[2.5mm]
S_{k}(n) = a_{k+1}n^{k+1} + \dots + a_{1}n + a_{0}
\end{gather}
$$
(see [[Derivation of Faulhaber's Formulae\|proof]])
