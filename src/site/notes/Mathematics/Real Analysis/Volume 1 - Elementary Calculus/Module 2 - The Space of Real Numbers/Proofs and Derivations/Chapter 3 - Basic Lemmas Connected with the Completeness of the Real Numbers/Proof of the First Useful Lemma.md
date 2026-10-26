---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-3-basic-lemmas-connected-with-the-completeness-of-the-real-numbers/proof-of-the-first-useful-lemma/","dg-note-properties":{}}
---

# Prelude: At Most Countable
Let $X$ be a countably infinite set, and let $A \subset X$ be a subset of $X$. If $A = \emptyset$, then $A$ is finite and therefore at most countable. Assume henceforth that $A$ is nonempty ($A \ne \emptyset$).

Because $X$ is countably infinite, there exists a bijective mapping $f: \mathbb{N} \to X$. This bijection enumerates the elements of $X$ as a sequence of distinct terms $x_1, x_2, \dots, x_n, \dots$, where $x_n := f(n)$ for each $n \in \mathbb{N}$.

Because $A$ is a nonempty subset of $X$, the set of indices $\{n \in \mathbb{N} \mid x_n \in A\}$ is a nonempty subset of $\mathbb{N}$. By the Well-Ordering Principle ([[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Proposition 7 of the Properties of Natural Numbers]]), this set possesses a unique minimal element:
$$
\begin{gather}
n_1 := \min\{n \in \mathbb{N} \mid x_n \in A\} \tag{1}
\end{gather}
$$
Proceeding recursively, once $n_{k-1}$ has been defined, if the set $\{n \in \mathbb{N} \mid n > n_{k-1} \wedge x_n \in A\}$ is nonempty, define $n_k$ via the Well-Ordering Principle as its unique minimal element:
$$
\begin{gather}
n_k := \min\{n \in \mathbb{N} \mid n > n_{k-1} \text{ and } x_n \in A\} \tag{2}
\end{gather}
$$
By construction, this selection generates a strictly increasing sequence of natural-number indices $n_1 < n_2 < \dots < n_k < \dots$, and defines a mapping $g$ by setting $g(k) := x_{n_k} \in A$. There are two exhaustive outcomes for this recursive process:
1. **The process terminates at step $k$:** If $\{n \in \mathbb{N} \mid n > n_k \wedge x_n \in A\} = \emptyset$ for some $k \in \mathbb{N}$, then no element of $A$ appears in the enumeration of $X$ beyond index $n_k$. Thus, $A = \{x_{n_1}, x_{n_2}, \dots, x_{n_k}\}$ contains exactly $k$ distinct elements and is finite.
2. **The process does not terminate:** If the selection continues for all $k \in \mathbb{N}$, the mapping $g: \mathbb{N} \to A$ given by $g(k) = x_{n_k}$ is defined on all of $\mathbb{N}$:
   * **Injectivity:** For any $i, j \in \mathbb{N}$ with $i < j$, strict monotonicity of the indices yields $n_i < n_j$, so $n_i \ne n_j$. Because $f: \mathbb{N} \to X$ is injective, $g(i) = f(n_i) \ne f(n_j) = g(j)$.
   * **Surjectivity:** Let $a \in A \subset X$ be arbitrary. Because $f: \mathbb{N} \to X$ is surjective, there exists $m \in \mathbb{N}$ such that $a = x_m$. Since $n_1 \ge 1$ and $n_k > n_{k-1}$ implies $n_k \ge k$ by induction, the set $\{k \in \mathbb{N} \mid n_k \ge m\}$ is nonempty. Let $k$ be its minimal element; by the minimal choice in steps 1 and 2, $n_k$ cannot strictly exceed $m$ without $m$ having already been selected, forcing $n_k = m$ and $g(k) = x_{n_k} = x_m = a$.

Thus, $g: \mathbb{N} \to A$ is a bijection, and $A$ is countably infinite. In either case, $A$ is either finite or countably infinite, establishing that $A$ is at most countable.

---
# Main Proof
Let $I = \{[a, b]\}$ be a nonempty system of nested closed intervals in $\mathbb{R}$, meaning that for any two intervals $[a_1, b_1], [a_2, b_2] \in I$, either $[a_1, b_1] \subset [a_2, b_2]$ or $[a_2, b_2] \subset [a_1, b_1]$. Define the sets of left and right endpoints of the intervals in $I$:
$$
\begin{gather}
A := \{a \in \mathbb{R} \mid [a, b] \in I\} \quad \text{and} \quad B := \{b \in \mathbb{R} \mid [a, b] \in I\} \tag{1}
\end{gather}
$$
Because $I$ is nonempty, both $A$ and $B$ are nonempty subsets of $\mathbb{R}$. For any $a_1 \in A$ and $b_2 \in B$, let $[a_1, b_1], [a_2, b_2] \in I$ be their corresponding intervals. Since one interval is contained in the other, either $[a_1, b_1] \subset [a_2, b_2]$ (so $a_2 \le a_1 \le b_1 \le b_2$) or $[a_2, b_2] \subset [a_1, b_1]$ (so $a_1 \le a_2 \le b_2 \le b_1$). In either case:
$$
\begin{gather}
a_1 \le b_2 \quad \forall a_1 \in A, \ \forall b_2 \in B \tag{2}
\end{gather}
$$
Step 2 demonstrates that $A$ is bounded above by every $b \in B$, and $B$ is bounded below by every $a \in A$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|Least Upper Bound and Greatest Lower Bound Principles]], the supremum $\alpha := \sup A$ and the infimum $\beta := \inf B$ exist in $\mathbb{R}$. Furthermore, by [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Monotonicity and Ordering of Extrema\|Monotonicity and Ordering of Extrema]], step 2 implies
$$
\begin{gather}
a \le \alpha = \sup A \le \inf B = \beta \le b \quad \forall [a, b] \in I \tag{3}
\end{gather}
$$
Because $\alpha \le \beta$, the closed interval $[\alpha, \beta]$ is well-defined and nonempty. It remains to establish the set equality $[\alpha, \beta] = \bigcap_{[a, b] \in I} [a, b]$ via mutual inclusion:
1. **Forward Inclusion ($[\alpha, \beta] \subset \bigcap_{[a, b] \in I} [a, b]$):** Let $x \in [\alpha, \beta]$, so $\alpha \le x \le \beta$. For every interval $[a, b] \in I$, step 3 gives $a \le \alpha \le x \le \beta \le b$, which implies $x \in [a, b]$ for all $[a, b] \in I$. Thus, $x \in \bigcap_{[a, b] \in I} [a, b]$.
2. **Reverse Inclusion ($\bigcap_{[a, b] \in I} [a, b] \subset [\alpha, \beta]$):** Let $x \in \bigcap_{[a, b] \in I} [a, b]$. Then $a \le x \le b$ holds for every $[a, b] \in I$, which means $x$ is an upper bound for $A$ and a lower bound for $B$. By the definitions of the least upper bound $\alpha = \sup A$ and greatest lower bound $\beta = \inf B$, it follows that $\alpha \le x \le \beta$, so $x \in [\alpha, \beta]$.

Combining both inclusions establishes the identity
$$
\begin{gather}
[\alpha, \beta] = \bigcap_{[a, b] \in I} [a, b] \tag{4}
\end{gather}
$$
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
