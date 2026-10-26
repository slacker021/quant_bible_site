---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-properties-of-order-preserving-homomorphisms/","dg-note-properties":{}}
---

Let $(\mathbb{R}, +, \cdot, \le)$ and $(\mathbb{R}', +', \cdot', \le')$ be complete linearly ordered fields, and let $f: \mathbb{R} \to \mathbb{R}'$ be a non-trivial order-preserving ring homomorphism, meaning that $f$ is not identically $0'$ and satisfies for all $x, y \in \mathbb{R}$:
$$
\begin{gather}
f(x + y) = f(x) +' f(y), \quad f(x \cdot y) = f(x) \cdot' f(y), \quad \text{and} \quad (x \le y \implies f(x) \le' f(y)) \tag{1}
\end{gather}
$$

# Preservation of Additive and Multiplicative Identities
Because $0 + 0 = 0$ in $\mathbb{R}$, applying the additive property of $f$ yields
$$
\begin{gather}
f(0) = f(0 + 0) = f(0) +' f(0) \implies f(0) = 0' \tag{2}
\end{gather}
$$
after adding the additive inverse $-f(0)$ in $\mathbb{R}'$ to both sides. Similarly, for any $x \in \mathbb{R}$,
$$
\begin{gather}
0' = f(0) = f(x + (-x)) = f(x) +' f(-x) \implies f(-x) = -f(x) \tag{3}
\end{gather}
$$

Next, because $1 \cdot 1 = 1$ in $\mathbb{R}$, the multiplicative property of $f$ gives
$$
\begin{gather}
f(1) = f(1 \cdot 1) = f(1) \cdot' f(1) \implies f(1) \cdot' (f(1) -' 1') = 0' \tag{4}
\end{gather}
$$

In the field $\mathbb{R}'$, a product vanishes if and only if at least one factor is $0'$, so either $f(1) = 0'$ or $f(1) = 1'$. If $f(1) = 0'$, then for every $x \in \mathbb{R}$ we would have $f(x) = f(x \cdot 1) = f(x) \cdot' f(1) = f(x) \cdot' 0' = 0'$, contradicting the premise that $f$ is non-trivial. Therefore,
$$
\begin{gather}
f(1) = 1' \tag{5}
\end{gather}
$$

---
# Action on Integers and Rational Numbers
For any natural number $n \in \mathbb{N}$, induction on $n$ using step 1 and step 5 yields
$$
\begin{gather}
f(n) = f(\underbrace{1 + \dots + 1}_{n \text{ terms}}) = \underbrace{f(1) +' \dots +' f(1)}_{n \text{ terms}} = \underbrace{1' +' \dots +' 1'}_{n \text{ terms}} =: n' \in \mathbb{N}' \tag{6}
\end{gather}
$$

Since $1' >' 0'$ in the ordered field $\mathbb{R}'$, every $n \in \mathbb{N}$ satisfies $f(n) = n' >' 0'$, and by step 3, $f(-n) = -n'$ for all $-n \in -\mathbb{N}$. Thus, $f$ maps $\mathbb{Z}$ bijectively onto $\mathbb{Z}'$.

Now let $r = m/n \in \mathbb{Q}$ be any rational number with $m \in \mathbb{Z}$ and $n \in \mathbb{N}$. Because $n \ge 1$, we have $f(n) = n' >' 0'$, so $f(n) \ne 0'$ and $(f(n))^{-1}$ exists in $\mathbb{R}'$. Applying $f$ to the identity $m = \frac{m}{n} \cdot n$ gives
$$
\begin{gather}
f(m) = f\left(\frac{m}{n} \cdot n\right) = f\left(\frac{m}{n}\right) \cdot' f(n) \implies f\left(\frac{m}{n}\right) = f(m) \cdot' (f(n))^{-1} = \frac{m'}{n'} \in \mathbb{Q}' \tag{7}
\end{gather}
$$

If $r = m/n > 0$ (with $n \in \mathbb{N}$), then $m \in \mathbb{N}$, so $m' >' 0'$ and $n' >' 0'$, which implies $f(r) = m'/n' >' 0'$. Consequently, for any $r_1, r_2 \in \mathbb{Q}$ with $r_1 < r_2$, we have $r_2 - r_1 > 0$ in $\mathbb{Q}$, which yields
$$
\begin{gather}
f(r_2) -' f(r_1) = f(r_2 - r_1) >' 0' \iff f(r_1) <' f(r_2) \tag{8}
\end{gather}
$$

Thus, the restriction $f|_{\mathbb{Q}}: \mathbb{Q} \to \mathbb{Q}'$ is a strictly order-preserving field isomorphism from $\mathbb{Q}$ onto the rational subfield $\mathbb{Q}' \subset \mathbb{R}'$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$