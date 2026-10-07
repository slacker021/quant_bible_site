---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-isomorphism-and-categoricity-in-the-real-numbers/","dg-note-properties":{}}
---

Let $f: \mathbb{R} \to \mathbb{R}'$ be a field homomorphism. By definition of field identities, 
$$f(0) = 0' \quad \text{and} \quad f(1) = 1'. \tag{1}$$
For any natural number $n \in \mathbb{N}$, the additive homomorphism property requires:
$$f(n) = f\left(\sum_{k=1}^n 1\right) = \sum_{k=1}^n f(1) = \sum_{k=1}^n 1' =: n'.\tag{2}$$
For negative integers, the preservation of additive inverses implies $f(-n) = -f(n) = -n'$. Thus, $f$ maps $\mathbb{Z}$ onto $\mathbb{Z}'$.

For any rational number $r = m/n \in \mathbb{Q}$ where $m, n \in \mathbb{Z}$ and $n \ne 0$, 
$$f(m) = f\left(\frac{m}{n} \cdot n\right) = f\left(\frac{m}{n}\right) \cdot f(n) \implies f\left(\frac{m}{n}\right) = \frac{f(m)}{f(n)} = \frac{m'}{n'}. \tag{3}$$
Because $m/n > 0$ implies that $m$ and $n$ have identical signs, $m'/n' >' 0'$. Hence, $f\vert{}_{\mathbb{Q}}: \mathbb{Q} \to \mathbb{Q}'$ is a strictly order-preserving field isomorphism between the rational subfields.

Now, let $x \in \mathbb{R}$, which can be used to define the set of rational lower bounds:  
$$L_x = \{ r \in \mathbb{Q} \mid r \le x \}. \tag{4}$$
By the density of $\mathbb{Q}$ in $\mathbb{R}$, $x = \sup L_x$. Consider the image set under $f$:  

$$f(L_x) = \{ f(r) \in \mathbb{Q}' \mid r \in L_x \} \subset \mathbb{R}'. \tag{5}$$
By the Archimedean property in $\mathbb{R}$, there exists an integer $M$ such that $x < M$, meaning $r < M$ for all $r \in L_x$. Since $f$ preserves order on $\mathbb{Q}$, $f(r) \le' f(M) = M'$ for all $f(r) \in f(L_x)$. Thus, $f(L_x)$ is non-empty and bounded above in $\mathbb{R}'$.

By the axiom of completeness in $\mathbb{R}'$, the least upper bound exists:  

$$f(x) := \sup' f(L_x) \tag{6}$$
This extends $f$ to all of $\mathbb{R}$.

Thirdly, let $x,y \in \mathbb{R}$. Three important facts result from what has been established: 
- **Order:** If $x < y$, the density of rationals provides $r_1, r_2 \in \mathbb{Q}$ such that $x < r_1 < r_2 < y$. Therefore, $f(x) \le' f(r_1) <' f(r_2) \le' f(y)$, demonstrating strict monotonicity. Strict monotonicity directly implies that $f$ is injective.
- **Addition:** Because $L_{x+y}$ and $L_x + L_y$ are cofinal in $\mathbb{Q}$:  
$$f(x + y) = \sup' f(L_{x+y}) = \sup'(f(L_x) + f(L_y)) = \sup' f(L_x) + \sup' f(L_y) = f(x) + f(y) \tag{7}$$
- **Multiplication:** For positive elements $x, y > 0$, an identical supremum argument over products of positive rationals gives $f(x \cdot y) = f(x) \cdot f(y)$, which extends to all of $\mathbb{R}$ by signs. 

Finally, let $y' \in \mathbb{R}'$. Define $L_{y'} = \{ r \in \mathbb{Q} \mid f(r) \le' y' \}$. The set $L_{y'}$ is non-empty and bounded above in $\mathbb{R}$. Taking $x = \sup L_{y'} \in \mathbb{R}$ gives $f(x) = y'$, establishing surjectivity.

Uniqueness follows from the fact that any isomorphism must map $1 \mapsto 1'$, fixing the action on $\mathbb{Q}$. Because rational points are dense, preservation of order forces the mapping of every real number to be uniquely determined by the cut it induces.
$$\textbf{Q.E.D}$$

