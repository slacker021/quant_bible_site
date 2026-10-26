---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-the-existence-of-transcendental-numbers/","dg-note-properties":{}}
---

A real number $x \in \mathbb{R}$ is called a *real algebraic number* if it is a root of a non-constant polynomial equation in one variable with integer coefficients. Any such polynomial $P(x)$ of degree $n \in \mathbb{N}$ takes the form
$$
\begin{gather}
P(x) = a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0 = 0 \tag{1}
\end{gather}
$$
where $a_0, a_1, \dots, a_n \in \mathbb{Z}$ and the leading coefficient satisfies $a_n \in \mathbb{Z} \setminus \{0\}$.

First, observe by induction on $k \in \mathbb{N}$ that for any countable set $X$ and any at most countable set $Y$, the Cartesian product $X \times Y = \bigcup_{x \in X} (\{x\} \times Y)$ is a countable union of sets $\{x\} \times Y$ each equipotent to $Y$, and is therefore at most countable by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of Proposition 2 for Countable Sets\|Proposition on the Union of Countable Sets]] (and countable whenever $Y$ is countable). Since $\mathbb{Z}$ and $\mathbb{Z} \setminus \{0\}$ are countable, it follows by induction on $n \in \mathbb{N}$ that the Cartesian product $(\mathbb{Z} \setminus \{0\}) \times \mathbb{Z}^n$ is countable for every $n \in \mathbb{N}$.

For each fixed degree $n \in \mathbb{N}$, let $\mathcal{P}_n$ denote the set of all polynomials of degree $n$ with integer coefficients. Because each polynomial $P \in \mathcal{P}_n$ in step 1 is uniquely determined by its $(n + 1)$-tuple of coefficients $(a_n, a_{n-1}, \dots, a_0) \in (\mathbb{Z} \setminus \{0\}) \times \mathbb{Z}^n$, the set $\mathcal{P}_n$ is equipotent to $(\mathbb{Z} \setminus \{0\}) \times \mathbb{Z}^n$ and is therefore countable. Consequently, the collection of all non-constant integer-coefficient polynomials
$$
\begin{gather}
\mathcal{P} := \bigcup_{n=1}^\infty \mathcal{P}_n \tag{2}
\end{gather}
$$
is a countable union of countable sets, which by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of Proposition 2 for Countable Sets\|Proposition on the Union of Countable Sets]] is countable.

For each polynomial $P \in \mathcal{P}$ of degree $n \in \mathbb{N}$, let $R(P) := \{ x \in \mathbb{R} \mid P(x) = 0 \}$ denote its set of real roots. Because a polynomial of degree $n \ge 1$ over a field possesses at most $n$ distinct roots (by polynomial factor division), every root set $R(P)$ is finite ($|R(P)| \le n$) and therefore at most countable. The set of all real algebraic numbers $\mathbb{A} \subset \mathbb{R}$ is the union of the real root sets over all $P \in \mathcal{P}$:
$$
\begin{gather}
\mathbb{A} = \bigcup_{P \in \mathcal{P}} R(P) \tag{3}
\end{gather}
$$
Step 3 expresses $\mathbb{A}$ as the union of a countable family of finite (hence at most countable) sets, which implies that $\mathbb{A}$ is at most countable. Moreover, for every rational number $r = p/q \in \mathbb{Q}$ (with $p \in \mathbb{Z}$ and $q \in \mathbb{N}$), $r$ is the unique root of the degree-$1$ polynomial $P(x) = qx - p \in \mathcal{P}_1$, so $\mathbb{Q} \subset \mathbb{A}$. Since $\mathbb{Q}$ is infinite, $\mathbb{A}$ is infinite and therefore countably infinite.

A real number is called *transcendental* if it is not algebraic. The set of real transcendental numbers $\mathbb{T}$ is the complement of $\mathbb{A}$ in $\mathbb{R}$, yielding the disjoint partition:
$$
\begin{gather}
\mathbb{T} := \mathbb{R} \setminus \mathbb{A} \iff \mathbb{R} = \mathbb{A} \cup \mathbb{T} \tag{4}
\end{gather}
$$
If $\mathbb{T}$ were at most countable, then step 4 would express $\mathbb{R}$ as the union of two at most countable sets, forcing $\mathbb{R}$ to be countable and contradicting [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 4 - The Cardinality of the Continuum/Proof of the Uncountability of the Real Numbers\|Cantor's Theorem]]. Thus, $\mathbb{T}$ is uncountable (and in particular nonempty). Furthermore, because $\mathbb{T}$ is uncountable, it contains a countably infinite subset $S = \{t_1, t_2, t_3, \dots\} \subset \mathbb{T}$ (obtained by selecting elements inductively since $\mathbb{T} \setminus \{t_1, \dots, t_k\}$ is never empty), and enumerating $\mathbb{A} = \{a_1, a_2, a_3, \dots\}$ allows one to define a bijection $h: \mathbb{R} \to \mathbb{T}$ by setting $h(a_n) := t_{2n-1}$, $h(t_n) := t_{2n}$, and $h(x) := x$ for all $x \in \mathbb{T} \setminus S$. Therefore, the set of real transcendental numbers $\mathbb{T}$ has the cardinality of the continuum $\mathfrak{c}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
