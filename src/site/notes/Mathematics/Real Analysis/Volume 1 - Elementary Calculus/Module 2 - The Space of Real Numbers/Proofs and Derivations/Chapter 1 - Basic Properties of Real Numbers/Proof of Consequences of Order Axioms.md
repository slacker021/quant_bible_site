---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-1-basic-properties-of-real-numbers/proof-of-consequences-of-order-axioms/","dg-note-properties":{}}
---

The axiom of ordering asserts that 
$$
x < y \iff x \leq y \wedge x \neq y \tag{1}
$$
where $x$ and $y$ are real numbers. 

# Proposition 1
### Case 1
Suppose that $x < y$. By definition, $x \neq y$. The final condition required for this is that one of these must be true:
$$
x \leq y \text{ or } y \leq x \tag{2}
$$
Because $x \neq y$ and $x <y$, then $y \geq x$ cannot hold true. Therefore, $x < y$ is the only one that can hold true among the three options.

### Case 2
Suppose that $x = y$. By definition, $x \leq y$ and $y \leq x$. The final condition required for this to hold true is that $x < y$ and $y < x$ cannot hold true. Therefore, $x = y$ is the only one that holds true among the three options. 

### Case 3
Suppose that $x > y$. By definition, $x \neq y$. The final conditioned required for this to hold true is that 
$$
x \leq y \text{ or } y \leq x \tag{3} 
$$
It cannot be that $y \leq x$. Therefore, $x \geq y$ but $x \neq y$ means that $x > y$ is the only option. 

---
# Proposition 2
In addition to $x$ and $y$, let $z$ be another real number in the domain of discourse. 

### Assertion 1
Suppose that $x < y$ and $y \leq z$. By definition, $x \leq y$ but $x \neq y$. Additionally, the second statement means that $y < z$ or $y = z$. This leads to two cases:
1. If $y = z$, then the statement $x < y$ can be altered to $x < z$. 
2. If $y < z$ and $x < y$, the transitive nature of the ordering axioms would show that $x < z$. 

### Assertion 2
Suppose that $x \leq y$ and $y < z$. By definition, $y \leq z$ but $y \neq z$. Additionally, $x < y$ or $x = y$. This leads to two cases: 
1. If $x = y$, then $x$ can be substituted for $y$ in $y < z$. The result is that $x < z$. 
2. If $x < y$ and $y < z$, then the transitive nature of the ordering axioms would show that $x < z$. 
$$
\textbf{Q.E.D}
$$