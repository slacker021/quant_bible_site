---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-binomial-theorem/","dg-note-properties":{}}
---

# Prelude: Pascal's Rule
To more easily demonstrate the validity of this theorem, a smaller and less important fact must first be demonstrated: *Pascal's Rule*. The formation of this rule begins by defining and expressing its binomial coefficient: 
$$\binom{n}{k} + \binom{n}{k-1} = \frac{n!}{k!(n-k)!} + \frac{n!}{(k-1)!(n-k+1)!} \tag{1}$$
To combine the fractions, a common denominator of $k!(n-k+1)!$ is required. The first fraction is multiplied by $\frac{n-k+1}{n-k+1}$ and the second by $\frac{k}{k}$, yielding
$$\frac{n!(n-k+1)}{k!(n-k+1)!} + \frac{n! \cdot k}{k!(n-k+1)!} = \frac{n!(n-k+1+k)}{k!(n-k+1)!} \tag{2}$$
This numerator can be simplified to
$$\frac{n!(n+1)}{k!(n+1-k)!} = \frac{(n+1)!}{k!(n+1-k)!} = \binom{n+1}{k} \tag{3}$$
This concludes this lemma. 

# Binomial Theorem

### Base Case
Let $n = 1$, which leads to the left side of the equation evaluating to
$$(x+y)^1 = x + y \tag{4}$$
Evaluating the summation on the right side for $n=1$:  
$$\sum_{k=0}^1 \binom{1}{k} x^{1-k} y^k = \binom{1}{0} x^1 y^0 + \binom{1}{1} x^0 y^1 = x + y \tag{5}$$
Since both sides are equivalent, the base case holds true.

### Inductive Hypothesis
Assume the theorem holds for an arbitrary natural number $n = m$: 
$$(x + y)^m = \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k \tag{6}$$

The expression $(x + y)^{m+1}$ can be factored as
$$(x + y)^{m+1} = (x + y) (x + y)^m \tag{7}$$
Substituting the inductive hypothesis gives
$$(x + y)^{m+1} = (x + y) \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k \tag{8}$$
Distributing the terms $x$ and $y$ across the summation yields:  
$$\begin{gather}
(x + y)^{m+1} = x \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k + y \sum_{k=0}^m \binom{m}{k} x^{m-k} y^k \\
(x + y)^{m+1} = \sum_{k=0}^m \binom{m}{k} x^{m-k+1} y^k + \sum_{k=0}^m \binom{m}{k} x^{m-k} y^{k+1} \tag{9}
\end{gather}$$

To align the exponents of $x$ and $y$ for combination, the index of the second summation is shifted by letting $j = k + 1$, meaning $k = j - 1$. As $k$ ranges from $0$ to $m$, $j$ ranges from $1$ to $m+1$: 
$$\sum_{k=0}^m \binom{m}{k} x^{m-k} y^{k+1} = \sum_{j=1}^{m+1} \binom{m}{j-1} x^{m-(j-1)} y^j = \sum_{j=1}^{m+1} \binom{m}{j-1} x^{m-j+1} y^j \tag{10}$$
Renaming the dummy variable $j$ back to $k$:  
$$\sum_{k=1}^{m+1} \binom{m}{k-1} x^{m-k+1} y^k \tag{11}$$
Substituting this shifted summation back into the expansion:  
$$(x + y)^{m+1} = \sum_{k=0}^m \binom{m}{k} x^{m-k+1} y^k + \sum_{k=1}^{m+1} \binom{m}{k-1} x^{m-k+1} y^k \tag{12}$$
Extracting the $k=0$ term from the first sum and the $k=m+1$ term from the second sum allows the remaining terms to be grouped under a single summation from $k=1$ to $m$:  
$$(x + y)^{m+1} = \binom{m}{0} x^{m+1} y^0 + \sum_{k=1}^m \left[ \binom{m}{k} + \binom{m}{k-1} \right] x^{m-k+1} y^k + \binom{m}{m} x^0 y^{m+1} \tag{13}$$
Applying the proven Pascal's Rule to the terms inside the bracket:  
$$\binom{m}{k} + \binom{m}{k-1} = \binom{m+1}{k} \tag{14}$$
Additionally, noting that $\binom{m}{0} = 1 = \binom{m+1}{0}$ and $\binom{m}{m} = 1 = \binom{m+1}{m+1}$, the expression simplifies to
$$(x + y)^{m+1} = \binom{m+1}{0} x^{m+1} y^0 + \sum_{k=1}^m \binom{m+1}{k} x^{(m+1)-k} y^k + \binom{m+1}{m+1} x^0 y^{m+1} \tag{15}$$
This perfectly condenses into a single continuous summation covering all bounds:  
$$(x + y)^{m+1} = \sum_{k=0}^{m+1} \binom{m+1}{k} x^{(m+1)-k} y^k \tag{16}$$
Thus, the $(m+1)$ step is structurally identical to the $m$ step, proving the theorem for all $n \in \mathbb{N}$ by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|Principle of Induction]]. 
$$
\textbf{Q.E.D}
$$

