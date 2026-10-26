---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-dedekind-s-cut-theorem-and-complete-equivalence/","dg-note-properties":{}}
---

Let $\mathbb{F}$ be a linearly ordered field. It must be shown that the Least Upper Bound Axiom (every nonempty subset bounded above has a supremum) is logically equivalent to Dedekind's Cut Principle (every partition of $\mathbb{F}$ into nonempty disjoint sets $X, Y$ with $x \le y$ for all $x \in X, y \in Y$ admits a unique cut element $c \in \mathbb{F}$ satisfying $x \le c \le y$, so that either $c = \max X$ or $c = \min Y$).

---
# Forward Implication: Least Upper Bound Axiom Implies Dedekind's Cut Principle
Assume the Least Upper Bound Axiom holds in $\mathbb{F}$. Let $X, Y \subset \mathbb{F}$ form a Dedekind cut:
$$
\begin{gather}
X \cup Y = \mathbb{F}, \quad X \cap Y = \emptyset, \quad X \ne \emptyset, \quad Y \ne \emptyset \\[2mm]
\forall x \in X, \ \forall y \in Y \ (x \le y) \tag{1}
\end{gather}
$$

Pick any element $y_0 \in Y$. By step 1, $x \le y_0$ for all $x \in X$, meaning $X$ is nonempty and bounded above by $y_0$. By the Least Upper Bound Axiom, $X$ possesses a supremum $c := \sup X \in \mathbb{F}$. By definition of $\sup X$,
$$
\begin{gather}
\forall x \in X \ (x \le c) \tag{2}
\end{gather}
$$

Furthermore, because every $y \in Y$ is an upper bound for $X$ and $c = \sup X$ is the *least* upper bound of $X$,
$$
\begin{gather}
\forall y \in Y \ (c \le y) \tag{3}
\end{gather}
$$

Combining steps 2 and 3 yields $x \le c \le y$ for all $x \in X$ and $y \in Y$. Because $X \cup Y = \mathbb{F}$ and $X \cap Y = \emptyset$, the element $c$ belongs to exactly one of the two sets:
* If $c \in X$, then step 2 implies $c = \max X$.
* If $c \in Y$, then step 3 implies $c = \min Y$.

To verify uniqueness of $c$, suppose $c_1, c_2 \in \mathbb{F}$ both satisfy $x \le c_i \le y$ for all $x \in X, y \in Y$ with $c_1 < c_2$. Then the midpoint $m := \frac{c_1 + c_2}{2} \in \mathbb{F}$ satisfies $c_1 < m < c_2$, meaning $m$ cannot belong to $X$ (since $x \le c_1 < m$) and cannot belong to $Y$ (since $m < c_2 \le y$), contradicting $X \cup Y = \mathbb{F}$. Thus, $c_1 = c_2$.

---
# Reverse Implication: Dedekind's Cut Principle Implies the Least Upper Bound Axiom
Assume Dedekind's Cut Principle holds in $\mathbb{F}$. Let $A \subset \mathbb{F}$ be an arbitrary nonempty subset that is bounded above by some element $b_0 \in \mathbb{F}$. Define $Y$ as the set of all strict upper bounds of $A$, and let $X$ be its complement in $\mathbb{F}$:
$$
\begin{gather}
Y := \{y \in \mathbb{F} \mid \forall a \in A \ (a < y)\} \\[2mm]
X := \mathbb{F} \setminus Y = \{x \in \mathbb{F} \mid \exists a \in A \text{ such that } x \le a\} \tag{4}
\end{gather}
$$

Verify that $(X, Y)$ forms a valid Dedekind cut of $\mathbb{F}$:
1. **Non-emptiness:** Since $A \ne \emptyset$, any $a_0 \in A$ satisfies $a_0 \le a_0$, so $A \subset X$ and $X \ne \emptyset$. Since $b_0$ is an upper bound for $A$, every $a \in A$ satisfies $a \le b_0 < b_0 + 1$, so $(b_0 + 1) \in Y$ and $Y \ne \emptyset$.
2. **Disjoint Partition and Ordering:** By construction, $X \cup Y = \mathbb{F}$ and $X \cap Y = \emptyset$. For any $x \in X$ and $y \in Y$, there exists $a \in A$ such that $x \le a$, while $a < y$ by definition of $Y$; by transitivity, $x < y$.

By Dedekind's Cut Principle, there exists a unique element $c \in \mathbb{F}$ such that
$$
\begin{gather}
x \le c \le y \quad \forall x \in X, \ \forall y \in Y \tag{5}
\end{gather}
$$
Because $A \subset X$, step 5 guarantees that $a \le c$ for all $a \in A$, so $c$ is an upper bound for $A$. Now let $u \in \mathbb{F}$ be any upper bound for $A$. For every $\varepsilon > 0$ in $\mathbb{F}$, the element $u + \varepsilon$ satisfies $a \le u < u + \varepsilon$ for all $a \in A$, meaning $(u + \varepsilon) \in Y$. By step 5, $c \le u + \varepsilon$ for all $\varepsilon > 0$, which forces $c \le u$ (for if $c > u$, setting $\varepsilon = \frac{c - u}{2} > 0$ would yield $c \le \frac{c + u}{2} < c$, a contradiction). Therefore, $c = \sup A$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$