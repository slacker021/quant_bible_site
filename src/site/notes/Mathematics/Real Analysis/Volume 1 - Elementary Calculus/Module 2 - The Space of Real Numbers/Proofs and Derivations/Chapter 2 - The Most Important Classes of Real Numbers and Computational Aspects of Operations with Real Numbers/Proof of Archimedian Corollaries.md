---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-archimedian-corollaries/","dg-note-properties":{}}
---

# Proposition 1
By the principle of Archimedes, there's a $n \in \mathbb{Z}$ such that $1 < \varepsilon \cdot n$. Since $0 < 1$ and $0 < \varepsilon$, the result is $0 < n$. Therefore, $n \in \mathbb{N}$ and $0 < \frac{1}{n} < \varepsilon$. 

---
# Proposition 2
The relation $0 < x$ is impossible due to previous proposition. 

---
# Proposition 3
Taking account of the first proposition, choose $n \in \mathbb{N}$ such that $0 < \frac{1}{n} < b - a$. By the principle of Archimedes, a number $m \in \mathbb{Z}$ can be found that such that
$$
\frac{m-1}{n} \le a < \frac{m}{n} \tag{1}
$$
Then $\frac{m}{n} < b$, since otherwise there would be
$$
\frac{m-1}{n} \le a < b \le \frac{m}{n}, \tag{2}
$$
from which it would follow that $\frac{1}{n} \ge b - a$. Therefore, 
$$
r = \frac{m}{n} \in \mathbb{Q} \text{ and } a < \frac{m}{n} < b. \tag{3}
$$

---
# Proposition 4
The number $k$ just mentioned is denoted $[x]$ and is called the integer part of $x$. The quantity $\{x  \}: = x - [x]$ is the fractional part of $x$. Thus, $x = [x] + \{x  \}$, and $\{ x \} \ge 0$. 
$$
\textbf{Q.E.D}
$$

