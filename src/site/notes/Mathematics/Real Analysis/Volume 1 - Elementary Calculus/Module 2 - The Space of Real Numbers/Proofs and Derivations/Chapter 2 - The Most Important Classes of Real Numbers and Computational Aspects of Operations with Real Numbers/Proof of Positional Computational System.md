---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-positional-computational-system/","dg-note-properties":{}}
---

Let $q \in \mathbb{N}$ be a fixed base with $q > 1$, and let $x > 0$ be an arbitrary positive real number. Note that setting $h := q - 1 > 0$ in [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Bernoulli's Inequality\|Bernoulli's Inequality]] gives, for all $n \in \mathbb{N}$,
$$
\begin{gather}
q^n = (1 + (q - 1))^n \ge 1 + n(q - 1) \tag{1}
\end{gather}
$$
Furthermore, because $q > 1$, the exponential mapping $m \mapsto q^m$ is strictly increasing on $\mathbb{Z}$: for any $m, n \in \mathbb{Z}$ with $m < n$, it follows that $n - m \in \mathbb{N}$, so $q^{n-m} \ge q^1 > 1 \implies q^m < q^n$.

Now define the subset $E \subset \mathbb{Z}$ of integer exponents $m$ for which $q^m$ strictly exceeds $x$:
$$
\begin{gather}
E := \{m \in \mathbb{Z} \mid x < q^m\} \tag{2}
\end{gather}
$$

To verify that $E$ is nonempty, apply the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Principle of Archimedes\|Principle of Archimedes]] with step size $q - 1 > 0$ to find $n \in \mathbb{N}$ such that $n(q - 1) > x$. By step 1, $q^n \ge 1 + n(q - 1) > x$, so $n \in E \ne \emptyset$.

To verify that $E$ is bounded below in $\mathbb{Z}$, apply the same reasoning to the positive real number $1/x > 0$: there exists a natural number $M \in \mathbb{N}$ such that
$$
\begin{gather}
q^M > \frac{1}{x} \iff q^{-M} < x \tag{3}
\end{gather}
$$

Because $m \mapsto q^m$ is strictly increasing on $\mathbb{Z}$, any integer $m \in E$ must satisfy $q^{-M} < x < q^m \implies -M < m$. Thus, $E$ is a nonempty subset of $\mathbb{Z}$ bounded below by $-M$.

By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Bounds in the Natural Numbers and Integers\|Proposition 4 of Bounds in the Natural Numbers and Integers]], $E$ possesses a unique minimal element $k := \min E \in \mathbb{Z}$. Since $k \in E$, we have $x < q^k$; since $k$ is minimal in $E$, the predecessor $k - 1 \notin E$, meaning $q^{k-1} \le x$. Combining these inequalities yields
$$
\begin{gather}
q^{k-1} \le x < q^k \tag{4}
\end{gather}
$$
Setting $p := k - 1 \in \mathbb{Z}$ equivalently gives $q^p \le x < q^{p+1}$. Finally, to confirm uniqueness, suppose $m, n \in \mathbb{Z}$ both satisfy step 4 with $m < n$. Then $m \le n - 1$, which implies $q^m \le q^{n-1}$ and yields the impossible chain $q^{n-1} \le x < q^m \le q^{n-1}$. Therefore, $m = n$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$