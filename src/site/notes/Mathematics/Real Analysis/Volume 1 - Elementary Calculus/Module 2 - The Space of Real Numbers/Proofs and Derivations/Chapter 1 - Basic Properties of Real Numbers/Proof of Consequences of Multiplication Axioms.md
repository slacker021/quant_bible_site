---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-1-basic-properties-of-real-numbers/proof-of-consequences-of-multiplication-axioms/","dg-note-properties":{}}
---

The proofs for these propositions merely repeat the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Addition Axioms\|proofs for the consequences of the addition axioms]], except for a change in the symbol and name of the operation. 

# Proposition 1
In less complicated terms, any number multiplied by $1$ is itself. With that said, let $1_{1}$ and $1_{2}$ both be multiplicative units in $\mathbb{R}$. By the axiom of the identity element in multiplication,  
$$
\begin{gather}
1_{1} = 1_{1} \cdot 1_{2} = 1_{2} \cdot 1_{1} = 1_{2} \tag{1}
\end{gather}
$$

---
# Proposition 2
If $x_{1}$ and $x_{2}$ are both reciproals of $x \in \mathbb{R}$, then the axiom of the reciprocal in the multiplication shows that
$$
\begin{gather}
x_{1} = x_{1} \cdot x = x_{1} \cdot (x_{2} \cdot x) \tag{2}
\end{gather}
$$
where the commutative property of multiplication would show that
$$
\begin{gather}
x_{1} = x_{1} \cdot x = x_{1} \cdot (x_{2} \cdot x) = (x_{1} \cdot x) \cdot x_{2} = x_{2} \tag{3}
\end{gather}
$$ 

---
# Proposition 3
Let $a \cdot x = b$ be an equation, where $a,b,x \in \mathbb{R}$ but $a \neq 0$. By the axiom of the identity element in multiplication, 
$a$ has a reciprocal $\frac{1}{a}$. Multiplying both sides by the reciprocal of $a$ yields
$$
\frac{1}{a} \cdot \left( a \cdot x \right) = \frac{1}{a} \left( b \right) \implies x = \frac{b}{a} \tag{4} 
$$
While the proof can actually end here, this may be rewritten as
$$
x = b \cdot a^{-1} \tag{5}
$$
$$
\textbf{Q.E.D}
$$
