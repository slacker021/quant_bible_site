---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-properties-of-natural-numbers/","dg-note-properties":{}}
---

# Proposition 1
Fix an arbitrary natural number $m \in \mathbb{N}$, and define the subset $E_+ \subset \mathbb{N}$ consisting of all $n \in \mathbb{N}$ for which the sum $m + n$ belongs to $\mathbb{N}$:
$$\begin{gather} E_+ := \{n \in \mathbb{N} \mid (m + n) \in \mathbb{N}\} \tag{1} \end{gather}$$

Because $\mathbb{N}$ is an inductive set and $m \in \mathbb{N}$, the successor $m + 1$ belongs to $\mathbb{N}$, which confirms that $1 \in E_+$. Next, assume $n \in E_+$, meaning $(m + n) \in \mathbb{N}$. By the associativity of addition in $\mathbb{R}$ and the inductive property of $\mathbb{N}$,
$$\begin{gather} m + (n + 1) = (m + n) + 1 \in \mathbb{N} \tag{2} \end{gather}$$

Thus, $n \in E_+ \implies (n + 1) \in E_+$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|Principle of Induction]], $E_+ = \mathbb{N}$, establishing that $m + n \in \mathbb{N}$ for all $m, n \in \mathbb{N}$.

To establish closure under multiplication, fix $m \in \mathbb{N}$ and define the subset
$$\begin{gather} E_\cdot := \{n \in \mathbb{N} \mid (m \cdot n) \in \mathbb{N}\} \tag{3} \end{gather}$$

Since $m \cdot 1 = m \in \mathbb{N}$, the base element $1$ belongs to $E_\cdot$. Assume $n \in E_\cdot$, so that $m \cdot n \in \mathbb{N}$. By the distributive law of $\mathbb{R}$,
$$\begin{gather} m \cdot (n + 1) = m \cdot n + m \cdot 1 = (m \cdot n) + m \tag{4} \end{gather}$$

Since $m \cdot n \in \mathbb{N}$ and $m \in \mathbb{N}$, the additive closure proven in step 2 guarantees that $(m \cdot n) + m \in \mathbb{N}$. Hence, $(n + 1) \in E_\cdot$, and by the Principle of Induction, $E_\cdot = \mathbb{N}$.

---
# Proposition 2
Define the set $E \subset \mathbb{N}$ consisting of $1$ together with all natural numbers whose predecessors belong to $\mathbb{N}$:
$$\begin{gather} E := \{n \in \mathbb{N} \mid (n = 1) \vee ((n - 1) \in \mathbb{N})\} \tag{5} \end{gather}$$
By construction, $1 \in E$. Suppose $n \in E$. Since $n \in \mathbb{N}$, the identity $(n + 1) - 1 = n \in \mathbb{N}$ holds immediately, which demonstrates that $(n + 1)$ satisfies the second condition in step 5. Therefore, $(n + 1) \in E$. By the Principle of Induction, $E = \mathbb{N}$, proving that every $n \in \mathbb{N}$ with $n \ne 1$ satisfies $(n - 1) \in \mathbb{N}$.

---
# Proposition 3
First, consider the base case $n = 1$ by defining the set

$$\begin{gather} M := \{x \in \mathbb{N} \mid (x = 1) \vee (x \ge 2)\} \tag{6} \end{gather}$$

where $2 := 1 + 1$. By definition, $1 \in M$. If $x \in M$, then either $x = 1$ (in which case $x + 1 = 2 \in M$) or $x \ge 2$ (in which case $x + 1 > x \ge 2$, so $x + 1 \in M$). By the Principle of Induction, $M = \mathbb{N}$. Consequently, every natural number $x \in \mathbb{N}$ satisfies $x \ge 1$, and any $x \in \mathbb{N}$ with $x > 1$ (so $x \ne 1$) satisfies $x \ge 2 = 1 + 1$. Since $2 \in \{x \in \mathbb{N} \mid 1 < x\}$, it follows that $\min\{x \in \mathbb{N} \mid 1 < x\} = 2$.

Now, consider the subset $E \subset \mathbb{N}$ of all $n \in \mathbb{N}$ for which the proposition holds:
$$\begin{gather} E := \{n \in \mathbb{N} \mid \min\{x \in \mathbb{N} \mid n < x\} = n + 1\} \tag{7} \end{gather}$$

From the base case above, $1 \in E$. Assume $n \in E$, and let $x \in \mathbb{N}$ satisfy $n + 1 < x$. Because $n \ge 1$, the inequality $x > n + 1 \ge 2 > 1$ ensures $x \ne 1$. By Proposition 2, $y := x - 1$ belongs to $\mathbb{N}$, and subtracting $1$ from $n + 1 < x$ yields $n < y$. Because $n \in E$, the element $y$ belongs to $\{y \in \mathbb{N} \mid n < y\}$, which has minimal element $n + 1$:
$$\begin{gather} y = x - 1 \ge n + 1 \implies x \ge (n + 1) + 1 = n + 2 \tag{8} \end{gather}$$

Since $n + 2 \in \{x \in \mathbb{N} \mid n + 1 < x\}$ and every element $x$ of this set satisfies $x \ge n + 2$, it follows that $\min\{x \in \mathbb{N} \mid n + 1 < x\} = n + 2$. Thus, $(n + 1) \in E$, and by the Principle of Mathematical Induction, $E = \mathbb{N}$.

---
# Proposition 4
Let $m, n \in \mathbb{N}$ satisfy $n < m$. Then $m$ is an element of the set $\{x \in \mathbb{N} \mid n < x\}$. By Proposition 3, the minimal element of this set is $n + 1$. Because every element of a set is greater than or equal to the set's minimal element,

$$\begin{gather} n + 1 = \min\{x \in \mathbb{N} \mid n < x\} \le m \tag{9} \end{gather}$$

---
# Proposition 5
Suppose, for the sake of contradiction, that for some $n \in \mathbb{N}$ there exists a natural number $x \in \mathbb{N}$ lying strictly between $n$ and $n + 1$:
$$\begin{gather} n < x < n + 1 \tag{10} \end{gather}$$

Applying Proposition 4 to the left-hand inequality $n < x$ (with $x, n \in \mathbb{N}$) dictates that $n + 1 \le x$, which directly contradicts the right-hand inequality $x < n + 1$ in step 10. Thus, no natural number lies strictly between $n$ and $n + 1$, confirming that $n + 1$ is the immediate successor of $n$.

---
# Proposition 6
Let $n \in \mathbb{N}$ with $n \ne 1$. By Proposition 2, the predecessor $m := n - 1$ belongs to $\mathbb{N}$. Suppose there exists $x \in \mathbb{N}$ such that

$$\begin{gather} n - 1 < x < n \iff m < x < m + 1 \tag{11} \end{gather}$$

By Proposition 5, no natural number $x \in \mathbb{N}$ can satisfy $m < x < m + 1$. Consequently, no natural number lies strictly between $n - 1$ and $n$, proving that $n - 1$ is the immediate predecessor of $n$ in $\mathbb{N}$.

---
# Proposition 7
Let $M \subset \mathbb{N}$ be a nonempty subset of natural numbers. If $1 \in M$, then because $1 \le x$ for all $x \in \mathbb{N}$ (established in the proof of Proposition 3), $1$ is the minimal element of $M$ ($\min M = 1$).

Suppose instead that $1 \notin M$, and consider the complement $E := \mathbb{N} \setminus M$, which consequently contains $1$. Assume, for the sake of contradiction, that for every $n \in E$, its successor $n + 1$ also belongs to $E$. Then $E \subset \mathbb{N}$ satisfies $1 \in E$ and $(n \in E \implies (n + 1) \in E)$, which by the Principle of Mathematical Induction forces $E = \mathbb{N}$. However, $E = \mathbb{N}$ implies $M = \mathbb{N} \setminus E = \emptyset$, contradicting the premise that $M$ is nonempty.

Therefore, there must be at least one element $n \in E$ such that $(n + 1) \notin E$, meaning $(n + 1) \in M$. In fact, define the set of all natural numbers $k$ whose predecessors up to $k$ all reside in $E$:
$$\begin{gather} S := \{k \in \mathbb{N} \mid \forall x \in \mathbb{N} \ (x \le k \implies x \in E)\} \tag{12} \end{gather}$$

Since $1 \in E$ and no natural number is smaller than $1$, $1 \in S$. If $S$ were inductive, then $S = \mathbb{N}$, which would again force $E = \mathbb{N}$ and $M = \emptyset$. Thus, there exists $n \in S$ such that $(n + 1) \notin S$. Because $n \in S$, every $x \in \mathbb{N}$ with $x \le n$ belongs to $E = \mathbb{N} \setminus M$, so no element of $M$ can satisfy $x \le n$. Meanwhile, because $(n + 1) \notin S$, it must be that $(n + 1) \notin E$, so $(n + 1) \in M$. Since every $x \in M$ fails $x \le n$ (meaning $x > n$), Proposition 4 guarantees $x \ge n + 1$ for all $x \in M$. Thus, $\min M = n + 1$.
$$\begin{gather} \textbf{Q.E.D} \end{gather}$$