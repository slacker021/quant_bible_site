---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-1-basic-properties-of-real-numbers/proof-of-the-consequences-of-the-connection-axioms/","dg-note-properties":{}}
---

Let $x$ and $y$ be real numbers. 

# Proposition 1
One of the axioms of multiplication assumes that $•$ is commutative:
$$
x \cdot y = y \cdot x \tag{1}
$$
If $x$ is any real number while $y$ is zero, then this can be represented as
$$
x \cdot 0 = 0 \cdot x \tag{2}
$$
Alternatively, $y$ can be any real number while $x$ is zero:
$$
y \cdot 0 = 0 \cdot y \tag{3}
$$
Another important rule to take note of is the *additive inverse* property of addition that zero takes, which is one of the axioms of addition. Zero reflects its position as the fulcrum between negative and positive values on the line of real numbers. Therefore, adding $x$ and $-x$ result in zero. 
Multiplication can be seen as *repeated addition*, where the expression $x \cdot y$ means to "add $y$ $x$ times.":
$$
x \cdot y = y_{1} + y_{2} \dots y_{x} \tag{4}
$$
Following from that explanation of multiplication, it suffices to say that $x \cdot 0$ means "add $x$ zero times", which yields zero:
$$
\begin{gather}
x \cdot 0 = 0  \\
y \cdot 0 = 0 \tag{5}
\end{gather}
$$
Therefore, steps 2 and 5 can be combined to mean that
$$
x \cdot 0 = 0 \cdot x = 0 \tag{7}
$$

---
# Proposition 2
Suppose that $x \cdot y = 0$. By proposition 1, Any real number multiplied by zero is merely zero. If $x$ and $y$ are both real numbers, then this leads to four cases:
1. If $x$ is zero, then $x \cdot y$ is zero. 
2. If $y$ is zero, then $x \cdot y$ is zero. 
3. If both $x$ and $y$ are zero, then $x \cdot y$ is zero.
4. If neither number is zero, then $x \cdot y$ cannot be zero. 

---
# Proposition 3
Beginning with a generalization:
$$
\begin{align}
(−y)x+yx &=(−y)x+yx \\
(−y)x+yx &=x(y−y) \\
(−y)x+yx &=x(0)\\
(−y)x+yx &=0 \\
(−y)x &=−yx\tag{8}
\end{align}
$$
Replacing $y$ with $1$ shows that
$$
\begin{align}
(−1)x+1 \cdot x &=(−1)x+1 \cdot x \\
(−1)x+1x &=1 \cdot (x−x) \\
(−1)x+1 \cdot x &=x \cdot (0) \\
(−1)x+(1) \cdot x &=0 \\
(−1)x &=−x \tag{9}
\end{align}
$$

---
# Proposition 4
Beginning with a generalization:
$$
\begin{align}
(-y)(-x) + (-yx) &= (-y)(-x) + (-y)x \\
(-y)(-x) + (-yx) &= (-y)(x-x) \\
(-y)(-x) + (-yx) &= (-y)(0) \\
(-y)(-x) + (-xy) &= 0  \\
(y)(-x) - xy &= 0 \\
(y)(-x) &= xy
\tag{10}
\end{align}
$$
Replacing $y$ with $1$ shows that
$$
\begin{align}
(-1)(-x) + (-1 \cdot x) &= (-1)(-x) + (-1)x \\
(-1)(-x) + (-1 \cdot x) &= (-1)(x-x) \\
(-1)(-x) + (-1 \cdot x) &= (-y)(0) \\
(-1)(-x) + (-1 \cdot x) &= 0  \\
(-1)(-x) - 1 \cdot x &= 0 \\ 
(-1)(-x) &= x \\
-x &= -x
\tag{11}
\end{align}
$$

---
# Proposition 5
Proposition 4 shows that any two negative numbers multiplied together yield a positive number:
$$
-x \cdot -y = xy \tag{12}
$$
Meanwhile, any number multiplied by the identity element $1$ is simply itself:
$$
x \cdot 1 = x \tag{13}
$$
Thus, the following statement:
$$
(-x)(-x) \tag{14}
$$
can be deconstructed to
$$
(-1)(x)(-1)(x)
$$
The commutative property of multiplication enables this to be rearranged to
$$
(-1)(-1) \cdot (x)(x) \tag{15}
$$
Which simplifies to
$$
1 \cdot x \cdot x = x \cdot x \tag{16}
$$
$$
\textbf{Q.E.D}
$$