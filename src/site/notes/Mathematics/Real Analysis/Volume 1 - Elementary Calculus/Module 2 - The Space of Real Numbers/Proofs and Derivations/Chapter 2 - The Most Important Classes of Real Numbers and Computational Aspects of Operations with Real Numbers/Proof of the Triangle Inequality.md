---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-triangle-inequality/","dg-note-properties":{}}
---

1. **Case 1 (Both $x$ and $y$ are non-negative: $x \ge 0$ and $y \ge 0$):**
   By the order axioms of $\mathbb{R}$, the sum satisfies $x + y \ge 0$. Applying the definition of absolute value yields $|x| = x$, $|y| = y$, and
   $$
   \begin{gather}
   |x + y| = x + y = |x| + |y| \tag{1}
   \end{gather}
   $$
   Thus, equality holds whenever both $x$ and $y$ are non-negative.

2. **Case 2 (Both $x$ and $y$ are non-positive: $x \le 0$ and $y \le 0$):**
   Here, $x + y \le 0$, so $|x| = -x$, $|y| = -y$, and
   $$
   \begin{gather}
   |x + y| = -(x + y) = (-x) + (-y) = |x| + |y| \tag{2}
   \end{gather}
   $$
   Thus, equality also holds whenever both $x$ and $y$ are non-positive.

3. **Case 3 (One number is strictly negative and the other is strictly positive):**
   Without loss of generality (by commutativity of addition), suppose $x < 0 < y$, so that $|x| = -x > 0$ and $|y| = y > 0$. By trichotomy on $x + y$, either $x + y \ge 0$ or $x + y < 0$:
   * If $x + y \ge 0$, then $\vert{}x + y\vert{} = x + y$. Since $x < 0$ and $\vert{}x\vert{} > 0$, it follows that $x < \vert{}x\vert{}$, which implies
     $$
     \begin{gather}
     |x + y| = x + y < y = |y| < |x| + |y| \tag{3}
     \end{gather}
     $$
   * If $x + y < 0$, then $\vert{}x + y\vert{} = -x - y$. Since $y > 0$ and $\vert{}y\vert{} > 0$, it follows that $-y < 0 < \vert{}y\vert{}$, which implies
     $$
     \begin{gather}
     |x + y| = -x - y < -x = |x| < |x| + |y| \tag{4}
     \end{gather}
     $$

Combining steps 1 through 4 confirms that $|x + y| \le |x| + |y|$ for all $x, y \in \mathbb{R}$, with equality holding if and only if $x$ and $y$ are both non-negative or both non-positive.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$