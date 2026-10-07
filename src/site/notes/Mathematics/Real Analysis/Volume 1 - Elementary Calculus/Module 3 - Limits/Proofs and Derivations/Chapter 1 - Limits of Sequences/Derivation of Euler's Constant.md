---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/derivation-of-euler-s-constant/","dg-note-properties":{}}
---

To prove that this limit exists as a finite real number, it suffices to show that the sequence $x_n = (1 + \frac{1}{n})^n$ is strictly increasing and bounded above, thereby converging by virtue of the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem]].

Applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Binomial Theorem\|Binomial Theorem]] to expand the expression yields:  
$$x_n = \sum_{k=0}^n \binom{n}{k} \left(\frac{1}{n}\right)^k = 1 + 1 + \sum_{k=2}^n \frac{n(n-1)\dots(n-k+1)}{k! n^k} \tag{1}$$

This can be factored into
$$x_n = 2 + \sum_{k=2}^n \frac{1}{k!} \left(1 - \frac{1}{n}\right) \left(1 - \frac{2}{n}\right) \dots \left(1 - \frac{k-1}{n}\right) \tag{2}$$
Consider the subsequent term $x_{n+1}$
$$x_{n+1} = 2 + \sum_{k=2}^{n+1} \frac{1}{k!} \left(1 - \frac{1}{n+1}\right) \left(1 - \frac{2}{n+1}\right) \dots \left(1 - \frac{k-1}{n+1}\right) \tag{3}$$
By comparing the components, it is observed that for every $k \le n$, the term $(1 - \frac{j}{n})$ is strictly less than $(1 - \frac{j}{n+1})$. Furthermore, $x_{n+1}$ contains an additional positive term for $k = n+1$. Thus, every element of the sum grows larger, and a new positive element is added, making $x_n < x_{n+1}$ for all $n \in \mathbb{N}$. The sequence is strictly increasing.

Returning to the expanded form of $x_n$, since each term of the form $(1 - \frac{j}{n})$ is strictly less than $1$, the sequence can be bounded by removing these fractional modifiers:  
$$x_n \le 2 + \sum_{k=2}^n \frac{1}{k!} \tag{4}$$
It is a known arithmetic fact that for $k \ge 2$, $k! \ge 2^{k-1}$. Substituting this inequality generates a bounding geometric series:
$$x_n \le 2 + \sum_{k=2}^n \frac{1}{2^{k-1}} \tag{5}$$
The sum of this finite geometric series strictly converges: 
$$\sum_{k=2}^n \frac{1}{2^{k-1}} = \frac{1}{2} + \frac{1}{4} + \dots + \frac{1}{2^{n-1}} = 1 - \frac{1}{2^{n-1}} < 1 \tag{6}$$

Substituting this back into the inequality yields
$$x_n < 2 + 1 = 3 \tag{7}$$
The sequence $\{x_n\}$ is strictly increasing and bounded above by $3$. Therefore, by the Weierstrass Theorem on Monotonic Sequences, the sequence must converge to a definitive finite limit, which is denoted as $e$. 
$$
\textbf{Q.E.D}
$$
