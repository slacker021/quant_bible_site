---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/proofs-and-derivations/module-1-some-general-mathematical-concepts-and-notation/chapter-3/proof-of-theorem-1/","dg-note-properties":{}}
---

Assume $(x = u) \land (y = v)$. Substituting $u$ for $x$ and $v$ for $y$ into the definition of $(x,y)$ yields
$$(x,y) = \{\{x\}, \{x,y\}\} = \{\{u\}, \{u,v\}\} \tag{1}$$
By definition of the ordered pair $(u,v)$, 
$$\{\{u\}, \{u,v\}\} = (u,v) \tag{2}$$
Therefore, 
$$
(x=u) \land (y=v) \implies (x,y) = (u,v) \tag{3}
$$

Assume $(x,y) = (u,v)$, which implies the set equality
$$\{\{x\}, \{x,y\}\} = \{\{u\}, \{u,v\}\} \tag{4}$$
Which implies two cases: 
- **Case 1 ($x = y$):**
    If $x = y$, the set reduces to $\{\{x\}, \{x,x\}\} = \{\{x\}\}$.
    Equality with $\{\{u\}, \{u,v\}\}$ requires that $\{\{u\}, \{u,v\}\} = \{\{x\}\}$.
    By the Axiom of Extensionality, $\{u\} = \{x\}$ and $\{u,v\} = \{x\}$, which implies $u = x$ and $v = x$.
    Since $x = y$, it follows that $x = u$ and $y = v$.
- **Case 2 ($x \neq y$):**
    If $x \neq y$, the set $\{\{x\}, \{x,y\}\}$ contains two distinct elements: a singleton set $\{x\}$ and a doubleton set $\{x,y\}$.
    For the equality $\{\{x\}, \{x,y\}\} = \{\{u\}, \{u,v\}\}$ to hold:
    1. The unique singleton element of the LHS must equal the unique singleton element of the RHS: $$\{x\} = \{u\} \implies x = u \tag{5}$$
    2. The unique doubleton element of the LHS must equal the unique doubleton element of the RHS:
	$$\{x,y\} = \{u,v\} \tag{6}$$
Substituting $x = u$ gives $\{x,y\} = \{x,v\}$. Since $y \in \{x,y\}$, it must be that $y \in \{x,v\}$. Because $x \neq y$, $y$ cannot equal $x$, forcing $y = v$.
$$\textbf{Q.E.D}$$