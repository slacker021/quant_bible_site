---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-1-general-mathematical-concepts-and-notation/proofs-and-derivations/chapter-4/proof-of-proposition-1-of-useful-facts-about-functions/","dg-note-properties":{}}
---

# Proposition 1

### LHS ($\implies$)
Assume $A \subseteq B$ and let $y \in f(A)$ be an arbitrary element. By definition of the direct image under $f$, there exists at least one element $x \in A$ such that
$$f(x) = y \tag{1}$$
Since $A \subseteq B$,
$$x \in A \implies x \in B \tag{2}$$
Since $x \in B$ and $y = f(x)$, it follows from the definition of the direct image that
$$y \in f(B) \tag{3}$$
Since $y \in f(A) \implies y \in f(B)$, it can be concluded that
$$f(A) \subseteq f(B) \tag{4}$$

### RHS ($\impliedby$)
To demonstrate that $f(A) \subseteq f(B)$ does not imply $A \subseteq B$, it suffices to provide a counterexample. Let $X = \{1, 2\}$, $Y = \{0\}$, and let $f: X \to Y$ be the constant mapping $f(1) = 0$ and $f(2) = 0$. Now, suppose that $A = \{ 1 \}$ and $B = \{ 2 \}$. Evaluating the images yields
$$
f(A) = \{0\} \text{ and } f(B) = \{0\} \tag{5}
$$
Here, $f(A) = f(B)$, so $f(A) \subseteq f(B)$ holds trivially. However, $A = \{1\} \nsubseteq \{2\} = B$ because $1 \notin \{2\}$. herefore, $f(A) \subseteq f(B)$ does not imply $A \subseteq B$ in general. 

---
# Proposition 2
Assume $A \neq \emptyset$. Since $A \neq \emptyset$, there exists at least one element $x_0 \in A$. Since $f: X \to Y$ is a well-defined mapping, $f(x_0)$ exists and assigns $x_0$ to a unique element $y_0 \in Y$. By definition of the direct image
$$
f(A) = \{ f(x) \in Y \mid x \in A \} \tag{6}
$$
the element $y_0 = f(x_0)$ belongs to $f(A)$. Because $f(A)$ contains at least one element $y_0$, $f(A) \neq \emptyset$. 

---
# Proposition 3
Let $y \in f(A \cap B)$ be an arbitrary element. By definition of direct image, there exists an element $x \in A \cap B$ such that $f(x) = y$. By definition of set intersection,
$$x \in A \cap B \implies (x \in A) \wedge (x \in B \tag{7})$$
Since $x \in A$ and $y = f(x)$, $y \in f(A)$, and since $x \in B$ and $y = f(x)$, $y \in f(B)$. Combining these statements yields $(y \in f(A)) \land (y \in f(B))$, which by definition of set intersection implies:
$$y \in f(A) \cap f(B) \tag{8}$$
Therefore, 
$$f(A \cap B) \subseteq f(A) \cap f(B) \tag{9}$$

---
# Proposition 4

### LHS: $f(A \cup B) \subseteq f(A) \cup f(B)$
Let $y \in f(A \cup B)$ be an arbitrary element. - By definition of direct image, there exists an element $x \in A \cup B$ such that $f(x) = y$. By definition of set union,
$$x \in A \cup B \implies (x \in A) \lor (x \in B) \tag{10}$$
This leads to two cases: 
$$
\begin{gather}
\text{Case 1: Since } x \in A \text{ and } y = f(x), y \in f(A). \text{ By definition of set union, } y \in f(A) \cup f(B).  \\[2.5mm]
\text{Case 2: Since } x \in B \text{ and } y = f(x), y \in f(B). \text{By definition of set union, } y \in f(A) \cup f(B). \tag{11}
\end{gather}
$$
In both cases, 
$$y \in f(A) \cup f(B) \tag{12}$$
Therefore, 
$$f(A \cup B) \subseteq f(A) \cup f(B) \tag{13}$$

### RHS: $f(A \cup B) \supseteq f(A) \cup f(B)$
By definition of union, $A \subseteq A \cup B$. Applying fact 1, 
$$A \subseteq B \implies f(A) \subseteq f(B) \tag{14}$$
gives the result 
$$f(A) \subseteq f(A \cup B) \tag{15}$$
Combining these two subset inclusions yields:
$$f(A) \cup f(B) \subseteq f(A \cup B) \tag{16}$$

Combining both proofs establishes
$$ f(A \cup B) = f(A) \cup f(B) \tag{17}$$
$$\textbf{Q.E.D}$$