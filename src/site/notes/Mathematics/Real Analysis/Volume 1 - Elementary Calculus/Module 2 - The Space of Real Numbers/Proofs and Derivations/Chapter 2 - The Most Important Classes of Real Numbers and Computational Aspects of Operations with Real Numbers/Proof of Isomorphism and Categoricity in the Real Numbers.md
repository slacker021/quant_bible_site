---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-isomorphism-and-categoricity-in-the-real-numbers/","dg-note-properties":{}}
---

Let $(\mathbb{R}, +, \cdot, \le)$ and $(\mathbb{R}', +', \cdot', \le')$ be two complete linearly ordered fields with additive identities $0, 0'$ and multiplicative identities $1, 1'$.

# Construction of the Canonical Rational Isomorphism
In $\mathbb{R}$ and $\mathbb{R}'$, let $\mathbb{N}$ and $\mathbb{N}'$ denote the smallest inductive sets containing $1$ and $1'$, respectively. Define the mapping $f_{\mathbb{Z}}: \mathbb{Z} \to \mathbb{Z}'$ by setting $f_{\mathbb{Z}}(0) := 0'$, and for $n \in \mathbb{N}$,

$$
\begin{gather}
f_{\mathbb{Z}}(n) := \underbrace{1' +' 1' +' \dots +' 1'}_{n \text{ terms}} =: n' \quad \text{and} \quad f_{\mathbb{Z}}(-n) := -n' \tag{1}
\end{gather}
$$

By induction on $\mathbb{N}$, $f_{\mathbb{Z}}$ is a strictly order-preserving ring isomorphism between $\mathbb{Z}$ and $\mathbb{Z}'$. Extending $f_{\mathbb{Z}}$ to the rational subfield $\mathbb{Q} \subset \mathbb{R}$ via
$$
\begin{gather}
f_{\mathbb{Q}}\left(\frac{m}{n}\right) := f_{\mathbb{Z}}(m) \cdot' (f_{\mathbb{Z}}(n))^{-1} = \frac{m'}{n'} \quad (m, n \in \mathbb{Z}, \ n \ne 0) \tag{2}
\end{gather}
$$

yields a well-defined, bijective, order-preserving field isomorphism $f_{\mathbb{Q}}: \mathbb{Q} \to \mathbb{Q}'$.

---
# Extension to the Real Continuum via Dedekind Cuts
For any real number $x \in \mathbb{R}$, define its set of rational lower bounds:

$$
\begin{gather}
L_x := \{r \in \mathbb{Q} \mid r \le x\} \tag{3}
\end{gather}
$$

By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Archimedian Corollaries\|Archimedean property and density of rationals]] in $\mathbb{R}$, the set $L_x$ is nonempty, bounded above by some integer $M > x$, and satisfies $x = \sup L_x$. Consider the image of $L_x$ under $f_{\mathbb{Q}}$ in $\mathbb{R}'$:

$$
\begin{gather}
f_{\mathbb{Q}}(L_x) := \{f_{\mathbb{Q}}(r) \in \mathbb{Q}' \mid r \in L_x\} \subset \mathbb{R}' \tag{4}
\end{gather}
$$

Because $f_{\mathbb{Q}}$ preserves order on $\mathbb{Q}$ and $r \le x < M$ for all $r \in L_x$, every element of $f_{\mathbb{Q}}(L_x)$ is bounded above in $\mathbb{R}'$ by $f_{\mathbb{Q}}(M) = M'$. By the Least Upper Bound Axiom in $\mathbb{R}'$, the supremum exists in $\mathbb{R}'$, allowing the definition of $f: \mathbb{R} \to \mathbb{R}'$ via

$$
\begin{gather}
f(x) := \sup' f_{\mathbb{Q}}(L_x) \tag{5}
\end{gather}
$$

For $x \in \mathbb{Q}$, we have $\max L_x = x$, so $f(x) = f_{\mathbb{Q}}(x)$, confirming that $f$ extends $f_{\mathbb{Q}}$.

---
# Verification of Isomorphism Properties and Uniqueness
Let $x, y \in \mathbb{R}$:
1. **Strict Monotonicity and Injectivity:** If $x < y$, the density of $\mathbb{Q}$ in $\mathbb{R}$ provides $r_1, r_2 \in \mathbb{Q}$ such that $x < r_1 < r_2 < y$. For every $r \in L_x$,  $r < r_1$, so $f_{\mathbb{Q}}(r) \le' f_{\mathbb{Q}}(r_1)$, whereas $r_2 \in L_y$. Consequently,
   $$
   \begin{gather}
   f(x) = \sup' f_{\mathbb{Q}}(L_x) \le' f_{\mathbb{Q}}(r_1) <' f_{\mathbb{Q}}(r_2) \le' \sup' f_{\mathbb{Q}}(L_y) = f(y) \tag{6}
   \end{gather}
   $$
   Thus, $x < y \implies f(x) <' f(y)$, which immediately implies injectivity.
2. **Surjectivity:** For any $y' \in \mathbb{R}'$, define $A := \{r \in \mathbb{Q} \mid f_{\mathbb{Q}}(r) \le' y'\}$. By the Archimedean property in $\mathbb{R}'$ and the order isomorphism of $f_{\mathbb{Q}}$, $A$ is nonempty and bounded above in $\mathbb{R}$. Setting $x := \sup A \in \mathbb{R}$ ensures $f(x) = y'$.
3. **Preservation of Addition and Multiplication:** By the density of $\mathbb{Q}$, the Minkowski sum $L_x + L_y$ satisfies $\sup(L_x + L_y) = x + y = \sup L_{x+y}$: 
   $$
   \begin{gather}
   f(x + y) = \sup' f_{\mathbb{Q}}(L_x + L_y) = \sup'(f_{\mathbb{Q}}(L_x) +' f_{\mathbb{Q}}(L_y)) = \sup' f_{\mathbb{Q}}(L_x) +' \sup' f_{\mathbb{Q}}(L_y) = f(x) +' f(y) \tag{7}
   \end{gather}
   $$
   Similarly, for $x, y > 0$, taking positive rational lower bounds $L_x^+ := \{r \in \mathbb{Q}_+ \mid r \le x\}$ yields $f(x \cdot y) = \sup'(f_{\mathbb{Q}}(L_x^+) \cdot' f_{\mathbb{Q}}(L_y^+)) = f(x) \cdot' f(y)$, which extends to all $x, y \in \mathbb{R}$ by sign symmetry.
4. **Uniqueness:** By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Properties of Order-Preserving Homomorphisms\|Properties of Order-Preserving Field Homomorphisms]], any order-preserving field isomorphism $g: \mathbb{R} \to \mathbb{R}'$ must coincide with $f_{\mathbb{Q}}$ on $\mathbb{Q}$. Because $g$ is an order isomorphism, it preserves suprema, forcing $g(x) = g(\sup L_x) = \sup' g(L_x) = \sup' f_{\mathbb{Q}}(L_x) = f(x)$ for all $x \in \mathbb{R}$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$