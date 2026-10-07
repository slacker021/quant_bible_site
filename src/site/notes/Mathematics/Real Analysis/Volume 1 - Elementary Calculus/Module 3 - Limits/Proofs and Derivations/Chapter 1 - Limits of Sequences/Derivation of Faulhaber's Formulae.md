---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/derivation-of-faulhaber-s-formulae/","dg-note-properties":{}}
---

Let $S_{k}(n) = \sum_{i = 1}^n i^k$ denote the sum of the $k$-th powers of the first $n$ positive integers.

# General Derivation
The [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Binomial Theorem\|Binomial Theorem]] establishes that $(x+1)^{k+1}$ can be expanded: 
$$
(x+1)^{k+1} = \sum_{j=0}^{k+1} \binom{k+1}{j} x^j \tag{1}
$$
Subtracting $x^{k+1}$ from both sides yields: 
$$
(x+1)^{k+1} - x^{k+1} = \sum_{j=0}^{k} \binom{k+1}{j} x^j \tag{2}
$$
Now both sides of the equation can be summed from $x=1$ to $n:$
$$
\sum_{x=1}^n ((x+1)^k - x^{k+1}) = \sum_{x=1}^n \left( \sum_{j=0}^k \binom{k+1}{j} x^j \right) \tag{3}
$$
The left side of the inequality, which is referred to as a *telescoping series*, can be fully expanded to
$$
(2^{k+1} - 1^{k+1}) + (3^{k+1} - 2^{k+1}) + \dots + ((n+1)^{k+1} - n^{k+1}) = (n+1)^{k+1} - 1 \tag{4}
$$
While the right side of inequality can be rearranged by swapping the order of summation:
$$
\sum_{j = 0}^k \binom{k+1}{j} \left(  \sum_{x=1}^n x^j \right) = \sum_{j = 0}^k \binom{k+1}{j} S_{j(n)} \tag{5}
$$
Steps 4 and 5 can now be equated with one another:
$$
(x+1)^{k+1} - 1 = \sum_{j = 0}^k \binom{k+1}{j} S_{j(n)}
$$
And then isolate $S_{k}(n)$ to extract the $j=k$ term from the summation:
$$
(x+1)^{k+1} - 1 = \binom{k+1}{k} S_{k}(n) + \sum_{j = 0}^{k-1} \binom{k+1}{j} S_{j(n)} \tag{6}
$$

---
# Prelude: Recursive Induction
This identity provides a *recursive* method to determine the coefficients $S_{k}(n)$. Since $S_{0}(n) = n$, which is a polynomial of degree $1$, is found using $S_{0}(n)$, $S_{2}(n)$ is found using $S_{1}(n)$ and $S_{0}(n)$, and so on. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|principle of induction]], since the sum of polynomials of degree $d$ is a polynomial of degree $d+1$, it follows that $S_{k}(n)$ must be a polynomial in $n$ of degree $k+1$. 

Thus, the sum of the $k$-th powers is a polynomial of degree $k+1$ in $n$. 
$$
\textbf{Q.E.D}
$$



