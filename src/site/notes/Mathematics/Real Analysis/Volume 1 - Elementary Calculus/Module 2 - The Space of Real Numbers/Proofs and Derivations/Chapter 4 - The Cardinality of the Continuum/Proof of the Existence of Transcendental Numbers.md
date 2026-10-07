---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-4-the-cardinality-of-the-continuum/proof-of-the-existence-of-transcendental-numbers/","dg-note-properties":{}}
---

An algebraic number is defined as any real (or *complex*) number that is a root of a non-zero polynomial equation in one variable with integer coefficients. Such a polynomial of degree $n$ takes the form:
$$
\begin{gather} P(x) = a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0 = 0,  \tag{1} \end{gather}
$$
where $a_i \in \mathbb{Z}$ for $0 \le i \le n$, and $a_n \neq 0$.

For a fixed degree $n$, a polynomial is entirely determined by its $n+1$ integer coefficients $(a_n, a_{n-1}, \dots, a_0)$. This sequence of coefficients can be viewed as an element of the Cartesian product $\mathbb{Z}^{n+1}$. Since the set of integers $\mathbb{Z}$ is countable, the finite Cartesian product $\mathbb{Z}^{n+1}$ is also countable.

The set of all polynomials with integer coefficients, $\mathbb{Z}[x]$, is the union of the sets of polynomials of degree $n$ for all $n \in \mathbb{N}$. Because a countable union of countable sets is countable, the entire set of integer-coefficient polynomials is countable.

By the Fundamental Theorem of Algebra, any polynomial of degree $n$ has at most $n$ distinct roots. Let $R(P)$ denote the finite set of roots for a given polynomial $P$. The set of all algebraic numbers is the union of the roots of all possible polynomials:
$$
\begin{gather} \mathbb{A} = \bigcup_{P \in \mathbb{Z}[x]} R(P) \tag{2} \end{gather}
$$
The equation of step 2 represents the union of a countable family of finite sets. By the established closure properties of countable operations, this union $\mathbb{A}$ is a countable set.

A transcendental number is defined as any real number that is not algebraic. Thus, the set of transcendental numbers, denoted $\mathbb{T}$, is the complement of $\mathbb{A}$ in $\mathbb{R}$:
$$
\begin{gather} \mathbb{T} = \mathbb{R} \setminus \mathbb{A} \implies \mathbb{R} = \mathbb{A} \cup \mathbb{T} \tag{3} \end{gather}
$$
It is a proven fact that the set of all real numbers $\mathbb{R}$ is uncountable. If the set of transcendental numbers $\mathbb{T}$ were countable, the union $\mathbb{A} \cup \mathbb{T}$ would be the union of two countable sets, which would necessitate that $\mathbb{R}$ is countable. This poses a direct contradiction.

Therefore, to preserve the uncountability of $\mathbb{R}$ against the countability of $\mathbb{A}$, the set of transcendental numbers $\mathbb{T}$ must be uncountable. This proves not only the existence of transcendental numbers but also that the overwhelming majority of real numbers are transcendental.
$$\textbf{Q.E.D}$$