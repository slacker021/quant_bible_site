---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-3-basic-lemmas-connected-with-the-completeness-of-the-real-numbers/proof-that-different-axioms-can-be-used/","dg-note-properties":{}}
---

# Theorem 1: Cauchy-Cantor and Archimedes Principles $\implies$ Axiom of Completeness
Let $X \subset \mathbb{R}$ be a non-empty set that is bounded from above. If $X$ possesses a maximum element, that element is trivially the supremum and the proof is complete. Assume $X$ has no maximum element, which implies that no element within $X$ is an upper bound.

Now, select an element $a_0 \in X$ (which is not an upper bound) and an upper bound $b_0$ of $X$. Construct the closed interval $I_0 = [a_0, b_0]$. Bisect $I_0$ at its midpoint $m_0 = \frac{a_0 + b_0}{2}$.
- If $m_0$ is an upper bound of $X$, define the next interval as $I_1 = [a_0, m_0]$.
- If $m_0$ is not an upper bound of $X$, define the next interval as $I_1 = [m_0, b_0]$.

Applying this bisection algorithm recursively generates a sequence of nested closed intervals $I_n = [a_n, b_n]$:
$$
\begin{gather} I_0 \supset I_1 \supset I_2 \supset \dots \supset I_n \supset \dots \tag{1} \end{gather} 
$$
By construction, an invariant is maintained: for every $n \in \mathbb{N}$, the right endpoint $b_n$ is an upper bound of $X$, and the left endpoint $a_n$ is strictly not an upper bound.

The length of the $n$-th interval is exactly $\vert{}I_n\vert{} = \frac{b_0 - a_0}{2^n}$. By the Principle of Archimedes, this length becomes arbitrarily small as $n$ approaches infinity. By the Cauchy-Cantor Principle, there exists a unique point $c \in \mathbb{R}$ that belongs to every interval $I_n$:
$$\begin{gather} c \in \bigcap_{n=1}^\infty I_n \tag{2} \end{gather} $$

To prove that $c = \sup X$, it must be shown that $c$ is an upper bound and that no smaller upper bound exists:
1. $c$ **is an upper bound:** Assume, for the sake of contradiction, that $c$ is not an upper bound. Then there exists $x \in X$ such that $x > c$. Let $\epsilon = x - c > 0$. By the Archimedean principle, there exists an integer $N$ such that $\vert{}I_N\vert{} < \epsilon$. Because $c \in I_N$, $b_N - c \le b_N - a_N < \epsilon$, which implies $b_N < x$. This contradicts the invariant that $b_N$ is an upper bound for $X$. Thus, $c$ must be an upper bound.
2. $c$ **is the least upper bound:** Assume there exists another upper bound $y$ such that $y < c$. Let $\epsilon = c - y > 0$. There exists an integer $N$ such that $\vert{}I_N\vert{} < \epsilon$. Because $c \in I_N$, $c - a_N \le b_N - a_N < \epsilon$, which implies $a_N > y$. Since $y$ is an upper bound of $X$, any number strictly greater than $y$ must also be an upper bound, forcing $a_N$ to be an upper bound. This contradicts the invariant that $a_n$ is never an upper bound.

Therefore, $c = \sup X$, establishing the Axiom of Completeness.

# Theorem 2: Bolzano-Weierstrass Principle $\implies$ Axiom of Completeness
To utilize the proof from Part 1, it suffices to show that the Bolzano-Weierstrass Principle implies both the Principle of Archimedes and the Cauchy-Cantor Principle.

Assume, for the sake of contradiction, that the set of natural numbers $\mathbb{N}$ is bounded from above in $\mathbb{R}$. As an infinite bounded set, $\mathbb{N}$ must possess a limit point $c \in \mathbb{R}$ by the Bolzano-Weierstrass Principle. By the definition of a limit point, any $\epsilon$-neighborhood around $c$, including $(c - 1/2, c + 1/2)$, must contain infinitely many points of $\mathbb{N}$. However, the distance between any two distinct natural numbers is at least $1$. Consequently, an open interval of length $1$ can contain at most one natural number. This yields a direct contradiction, proving that $\mathbb{N}$ is unbounded and the Principle of Archimedes holds.

Then, let $I_n = [a_n, b_n]$ be a sequence of nested closed intervals. Consider the set of left endpoints $A = \{a_n \mid n \in \mathbb{N}\}$. This set $A$ is bounded from above by $b_1$: 
- If $A$ is a finite set, the non-decreasing sequence $\{a_n\}$ must eventually become constant at some value $a^*$. Thus, $a^* \in I_n$ for all $n \in \mathbb{N}$, and the intersection is non-empty.
- If $A$ is an infinite set, it is bounded and, by the Bolzano-Weierstrass Principle, possesses a limit point $c$. Because $A$ is non-decreasing, the limit point $c$ must be greater than or equal to all $a_n$. Furthermore, since every $a_n$ is bounded by any right endpoint $b_m$, the limit point $c$ must be less than or equal to all $b_m$. Thus, $a_n \le c \le b_n$ for all $n \in \mathbb{N}$.

In both cases, $c \in \bigcap_{n=1}^\infty I_n$, satisfying the Cauchy-Cantor Principle. Since the Bolzano-Weierstrass Principle guarantees both Archimedes and Cauchy-Cantor, it guarantees the Axiom of Completeness via Part 1.

# Part 3: Borel-Lebesgue Principle $\implies$ Axiom of Completeness
Let $X \subset \mathbb{R}$ be a non-empty set bounded from above. Let $M$ be the set of all upper bounds of $X$. Since $X$ is bounded from above, $M$ is non-empty. Assume, for the sake of contradiction, that $X$ has no least upper bound.

Because $X$ possesses no least upper bound, the set $M$ possesses no minimum element. Thus, for every upper bound $y \in M$, there exists another, strictly smaller upper bound $y' \in M$ such that $y' < y$. Construct the open ray $U_y = (y', \infty)$. The family of all such rays $\{U_y \mid y \in M\}$ forms an open cover for $M$.

For any $x \notin M$, the number $x$ is not an upper bound, meaning there exists an element $x' \in X$ such that $x < x'$. Construct the open ray $V_x = (-\infty, x')$. The family of all such rays $\{V_x \mid x \notin M\}$ forms an open cover for the complement $\mathbb{R} \setminus M$.

The union of these two families forms a universal open cover for the entire real line:
$$
\begin{gather} \mathcal{C} = {U_y}_{y \in M} \cup {V_x}_{x \notin M} \tag{3} \end{gather}
$$

Select an element $a \in X$ and an upper bound $b \in M$. The closed and bounded interval $[a, b]$ is entirely covered by $\mathcal{C}$. By the Borel-Lebesgue Principle, there exists a finite subcover for $[a, b]$. Let this finite subcover consist of $\{U_{y_1}, \dots, U_{y_k}\}$ and $\{V_{x_1}, \dots, V_{x_m}\}$.

Define $y^* = \min\{y'_1, \dots, y'_k\}$. Because the set is finite and each $y'_i \in M$, $y^*$ is a valid upper bound belonging to $M$. The union of the $U_y$ sets in the finite subcover is exactly the single open ray $(y^*, \infty)$. Define $x^* = \max\{x'_1, \dots, x'_m\}$. Because the set is finite and each $x'_j \in X$, $x^*$ is an element belonging to $X$. The union of the $V_x$ sets in the finite subcover is exactly the single open ray $(-\infty, x^*)$.

For the finite subcover $(-\infty, x^*) \cup (y^*, \infty)$ to completely cover the interval $[a, b]$, the interval must not fall into any gap between the two rays. The point $y^*$ resides within $[a, b]$ because $a \le y^* \le b$. However, $y^*$ is not contained within $(y^*, \infty)$. For $y^*$ to be covered, it must fall within $(-\infty, x^*)$, which strictly requires that $y^* < x^*$.

However, $y^*$ is an upper bound of $X$ (since $y^* \in M$) and $x^*$ is an element of $X$. By the fundamental definition of an upper bound, $x^* \le y^*$.

This yields a direct and irreconcilable contradiction ($y^* < x^*$ versus $x^* \le y^*$). Thus, the assumption that $X$ has no least upper bound must be false, establishing the Axiom of Completeness.
$$\textbf{Q.E.D}$$