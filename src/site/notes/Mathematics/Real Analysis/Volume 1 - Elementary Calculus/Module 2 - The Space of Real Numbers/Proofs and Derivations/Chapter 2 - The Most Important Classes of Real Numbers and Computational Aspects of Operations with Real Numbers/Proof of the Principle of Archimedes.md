---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-principle-of-archimedes/","dg-note-properties":{}}
---

Let $h > 0$ be a fixed positive real number and $x \in \mathbb{R}$ be an arbitrary real number. Dividing the target inequality $(k - 1)h \le x < kh$ by $h > 0$ yields the equivalent condition
$$
\begin{gather}
k - 1 \le \frac{x}{h} < k \tag{1}
\end{gather}
$$

Define the subset $E \subset \mathbb{Z}$ of all integers strictly exceeding the ratio $x/h$:
$$
\begin{gather}
E := \left\{ n \in \mathbb{Z} \ \middle| \ \frac{x}{h} < n \right\} \tag{2}
\end{gather}
$$

By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Bounds in the Natural Numbers and Integers\|Proposition 5 of Bounds in the Natural Numbers and Integers]], the set of integers $\mathbb{Z}$ is not bounded above in $\mathbb{R}$, which guarantees that $x/h$ is not an upper bound for $\mathbb{Z}$ and therefore $E$ is nonempty. Simultaneously, by definition of $E$, every element $n \in E$ satisfies $n > x/h$, meaning $E$ is bounded below in $\mathbb{R}$ by $x/h$.

By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Bounds in the Natural Numbers and Integers\|Proposition 4 of Bounds in the Natural Numbers and Integers]], every nonempty subset of $\mathbb{Z}$ that is bounded below possesses a unique minimal element. Let $k := \min E \in \mathbb{Z}$. Because $k \in E$, it cannot be that $x/h < k$, and because $k$ is the minimal element of $E$, the preceding integer $k - 1 \in \mathbb{Z}$ cannot belong to $E$, forcing $k - 1 \le x/h$. Thus,
$$
\begin{gather}
k - 1 \le \frac{x}{h} < k \iff (k - 1)h \le x < kh \tag{3}
\end{gather}
$$

Finally, to verify uniqueness, suppose $k_1, k_2 \in \mathbb{Z}$ both satisfy step 3. Then $k_1 - 1 \le x/h < k_2$ implies $k_1 - 1 < k_2 \implies k_1 \le k_2$, and symmetrically $k_2 - 1 \le x/h < k_1$ implies $k_2 \le k_1$, which forces $k_1 = k_2$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$