---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-monotonicity-and-ordering-of-extrema/","dg-note-properties":{}}
---

# Proposition 1
Let $A$ and $B$ be nonempty bounded subsets of $\mathbb{R}$ satisfying $A \subset B$. Denote $M_B := \sup B$ and $m_B := \inf B$. By definition of the supremum and infimum of $B$,
$$
\begin{gather}
\forall b \in B \ (m_B \le b \le M_B) \tag{1}
\end{gather}
$$
Because $A \subset B$, every element $a \in A$ also belongs to $B$, which implies
$$
\begin{gather}
\forall a \in A \ (m_B \le a \le M_B) \tag{2}
\end{gather}
$$
Step 2 demonstrates that $M_B$ is an upper bound for $A$ and $m_B$ is a lower bound for $A$. Because $\sup A$ is the *least* upper bound of $A$ and $\inf A$ is the *greatest* lower bound of $A$, it follows that
$$
\begin{gather}
\sup A \le M_B = \sup B \quad \text{and} \quad \inf B = m_B \le \inf A \tag{3}
\end{gather}
$$

---
# Proposition 2
Let $X, Y \subset \mathbb{R}$ be nonempty sets such that
$$
\begin{gather}
\forall x \in X, \ \forall y \in Y \ (x \le y) \tag{4}
\end{gather}
$$

Fix an arbitrary element $y_0 \in Y$. By step 4, $x \le y_0$ for all $x \in X$, which means $y_0$ is an upper bound for the nonempty set $X$. Consequently, $\sup X$ exists in $\mathbb{R}$ and satisfies
$$
\begin{gather}
\sup X \le y_0 \tag{5}
\end{gather}
$$

Because $y_0 \in Y$ was chosen arbitrarily, step 5 holds for every $y_0 \in Y$. This proves that the real number $\sup X$ is a lower bound for the set $Y$. Since $\inf Y$ is the greatest lower bound of $Y$,
$$
\begin{gather}
\sup X \le \inf Y \tag{6}
\end{gather}
$$

---
# Proposition 3
Assume in addition to step 4 that either $X \cup Y = \mathbb{R}$ or for every $\varepsilon > 0$ there exist $x \in X$ and $y \in Y$ with $y - x < \varepsilon$. From step 6, there already is $\sup X \le \inf Y$. Suppose, for the sake of contradiction, that strict inequality holds:
$$
\begin{gather}
\sup X < \inf Y \tag{7}
\end{gather}
$$
1. **If $X \cup Y = \mathbb{R}$:** Define the midpoint $c := \frac{\sup X + \inf Y}{2} \in \mathbb{R}$, which satisfies $\sup X < c < \inf Y$. Because $c > \sup X$, there is a $c \notin X$; because $c < \inf Y$, there is a have $c \notin Y$. Thus $c \notin X \cup Y = \mathbb{R}$, a contradiction.
2. **If $\forall \varepsilon > 0 \ \exists x \in X, y \in Y \ (y - x < \varepsilon)$:** Set $\varepsilon := \inf Y - \sup X > 0$. For any $x \in X$ and $y \in Y$, there is a $x \le \sup X$ and $\inf Y \le y$, which implies
   $$
   \begin{gather}
   y - x \ge \inf Y - \sup X = \varepsilon \tag{8}
   \end{gather}
   $$
   contradicting the existence of $x \in X, y \in Y$ with $y - x < \varepsilon$.
In both cases, the assumption $\sup X < \inf Y$ is untenable, forcing
$$
\begin{gather}
\sup X = \inf Y \tag{9}
\end{gather}
$$
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$