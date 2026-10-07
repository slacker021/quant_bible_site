---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-1-basic-properties-of-real-numbers/proof-of-consequences-of-order-with-addition-and-multiplication/","dg-note-properties":{}}
---

Let $x,y,w,z$ be real numbers. 

# Proposition 1
Let $x < y$. By definition of strict inequality, as seen in axioms 1 and 3 of the principle of ordering:
$$
(x < y) \implies (x \leq y) \implies (x + z) \leq (y + z) \tag{1}
$$
It remains to be verified that $x + z \neq y + z$. Indeed, 
$$
\left((x + z) = (y + z) \right) \implies (x = (y + z) - z = y + (z - z) = y) \tag{2}
$$
Step 2 contradicts the assumption that $x < y$. Therefore, the assumption must be true. 

---
# Proposition 2
Let $0 < x$, which implies that $x$ is negative. It was shown in a previous [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of the Consequences of the Connection Axioms\|proof]] that negating a negative number makes it positive. Therefore, negating the premise would alter both the inequality and value of $x$—yielding the conclusion that $0 > -x$. 

---
# Proposition 3
Let $x \leq y$ and $z \leq w$. By definition, 
$$
\begin{gather}
x \leq y \iff (x = y) \lor (x < y) \\
z \leq w \iff (z = w) \lor (z < w) \tag{3}
\end{gather}
$$
This leads to four cases:
1. If $x = y$ and $z = w$, then $x + z = y + w$. This is a condition that satisfies the conclusion that $x + z \leq y + w$. 
2. If $x = y$ but $z < w$, then $x + z < y + w$. This is a condition that satisfies the conclusion that $x + z \leq y + w$. 
3. If $x < y$ but $z = w$, then $x + z < y + w$. This is a condition that satisfies the conclusion that $x + z \leq y + w$.  
4. If $x < y$ and $z < w$, then $x + z < y + w$. This is a condition that satisfies the conclusion that $x + z \leq y + w$.  
In all cases, the conclusion $x + z \leq y + w$ holds true. Therefore, 
$$
(x \leq y) \wedge (z \leq w) \implies (x + z) \leq (y + w) \tag{4}
$$

---
# Proposition 4
Let $x \leq y$ but $z < w$. By definition, 
$$
\begin{gather}
x \leq y \iff x < y \lor x = y \\
z < w \iff z \leq w \wedge z  \neq w \tag{5}
\end{gather}
$$
This leads to two cases: 
1. If $x < y$, then case 4 of proposition 3 would show that $x + z < y + w$. 
2. If $x = y$, then case 2 of proposition 4 would show that $x + z < y + w$. 
In both cases, the conclusion $x + z < y + w$ holds true. Therefore, 
$$
(x \le y) \wedge (z < w) \implies (x + z < y + w) \tag{6}
$$

---
# Proposition 5
Let $0 < x$ and $0 < y$. There are three possibilities: 
1. If $x \cdot y = 0$, then $x$ or $y$ must be zero. However, this cannot be because of the premise. 
2. If $x \cdot y < 0$, then $x$ or $y$ must be negative. However, this cannot be because of the premise. 
3. If $x \cdot y > 0$, then this leads to two cases for this possibility: 
	1. If $x$ and $y$ are both negative numbers, then their product is a positive number. However, this cannot be because of the premise. 
	2. If $x$ and $y$ are both positive numbers, then their product is a positive number. This holds as per the premise. 
Therefore, 
$$
0 < x \wedge 0 < y \implies  (0 < xy) \tag{7}
$$
>[!info]+ Remark: Law of Trichotomy
>The three possibilities mentioned form the *Law of Trichotomy*. 

---
# Proposition 6
Let $x < 0$ and $y < 0$. The first subcase of case 3 in proposition 5 shows that the product of two negative numbers is positive. The premise implies that $x$ and $y$ are both negative numbers. Therefore, 
$$0 < x \wedge 0 < y \implies  (0 < xy) \tag{8}$$
---
# Proposition 7
Let $x < 0$ and $0 < y$. The second possibility of the Law of Trichotomy states that the product of a negative and positive number is negative. $x < 0$ implies that $x$ is negative and $0 < y$ implies that $y$ is positive. Therefore, $xy$ must be negative and hence, less than zero. 

---
# Proposition 8
Let $x < y$ and $0 < z$. By definition,
$$
\begin{gather}
x < y \iff x \le y \wedge x \ne y \\
0 < z \iff 0 \le y \wedge 0 \ne z \tag{9}
\end{gather}
$$
Additionally, assume the following: 
1. $z > 0 \iff -z < 0$, which is proven true by proposition 2. 
2. $(-a)b = -(ab)$, which is proven true by proposition 7. 
3. $0 \cdot b = 0$, which is a [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of the Consequences of the Connection Axioms\|consequence of the connection axioms]] that is proven true. 
With these facts established, the following chain of implications shows that
$$
\begin{gather}
x(−z)<y(−z)⟹ \\
−xz<−yz⟹ \\
−xz+xz<−yz+xz⟹ \\
0<−yz+xz⟹ \\
yz<xz \tag{10}
\end{gather}
$$

---
# Proposition 9
Let $x < y$ and $z < 0$. By definition, 
$$
\begin{gather}
x < y \iff x \le y \wedge x \ne y \\
z < 0 \iff z \le 0 \wedge z \ne 0 \tag{11}
\end{gather}
$$
Additionally, assume the following:
1. $z > 0 \iff -z < 0$, which is proven true by proposition 2. 
2. $(-a)b = -(ab)$, which is proven true by proposition 7. 
3. $0 \cdot b = 0$, which is a [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of the Consequences of the Connection Axioms\|consequence of the connection axioms]] that is proven true. 
With these facts established, the following chain of implications shows that
$$
\begin{gather}
(x)(-z) > y(-z) \implies \\
-xz > -yz \implies  \\
-xz + yz > -yz + yz \implies \\
-xz + yz > 0 \implies \\
-xz > -yz \implies \\
xz < yz 
\end{gather}
$$

---
# Proposition 10 
Assume that $x > 0$. By proposition 2, this results in $-x < 0$. Combining both results leads to a combined inequality of 
$$
-x < 0 < x \tag{12}
$$
Substituting $1$ for $x$ shows that 
$$
-1 < 0 < 1 \tag{13}
$$

---
# Proposition 11
Let $0 < x$. Multiplying both sides by $1/x$ shows that 
$$
\frac{1}{x} \cdot 1 > \frac{1}{x} \cdot 0 \implies \frac{1}{x} > \frac{1}{x} \cdot 0 \tag{14}
$$
The third assumption of proposition 9 shows that any number multiplied by zero results in a product of zero, as well as the fact that $x$ being greater than zero implies it's positive. Therefore, 
$$
\frac{1}{x} > \frac{1}{x} \cdot 0 \implies \frac{1}{x} > 0 \tag{15}
$$

---
# Proposition 12
Assume $0 < x$ and $x < y$. By definition, 
$$
\begin{gather}
0 < x \iff 0 \le x \wedge 0 \ne x \\
x < y \iff x \le y \wedge x \ne y \tag{16}
\end{gather}
$$
Given that $x$ is positive and the transitive nature of the ordering axioms, $0 \le y$ but $0 \ne y$. If $0 < y$ and with proposition 11, it can be shown that
$$
0 < \frac{1}{y} \tag{17}
$$
Moving onto the second statement of step 16, $x^{-1} > 0$ can be multiplied by $x^{-1}$ without changing the inequality sign: 
$$
\begin{gather}
x \cdot x^{-1} < y \cdot x^{-1} \implies \\
1 < y \cdot x^{-1} \tag{18}
\end{gather}
$$
Since $y^{-1} > 0$, both sides of the inequality at step 18 can be multiplied by $y^{-1}$ without changing the sign: 
$$
1 \cdot y^{-1} < (y \cdot x^{-1}) \cdot y^{-1} \tag{19}
$$
The associative and commutative properties of multiplication would show that 
$$
\begin{gather}
y^{-1} < (y \cdot y^{-1}) \cdot x^{-1} \\
y^{-1} < 1 \cdot x^{-1} \\
y^{-1} < x^{-1} \tag{20}
\end{gather}
$$
Both results can be combined to give the final desired result of: 
$$
0 < \frac{1}{y} < \frac{1}{x} \tag{21}
$$
$$
\textbf{Q.E.D}
$$

