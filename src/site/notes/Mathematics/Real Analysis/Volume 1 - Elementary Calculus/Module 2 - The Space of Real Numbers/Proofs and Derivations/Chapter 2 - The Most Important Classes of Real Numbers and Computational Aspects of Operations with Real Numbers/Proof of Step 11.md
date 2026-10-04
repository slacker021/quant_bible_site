---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-step-11/","dg-note-properties":{}}
---

Let $x$ be the sum of the sequence of $\alpha_{i}q^{i}$ and $x'$ be the sum of the sequence $\alpha'_{i}q^i$, where $i \in \mathbb{Z}$. Furthermore, assume that the symbols are different, meaning there's some index $k$ such that $\alpha_{k} \ne \alpha'_{k}$ and for all $j > k$, $\alpha_{j} = \alpha'_{j}$. Now, consider the difference $|x - x'|:$
$$
|x - x'| = (\alpha_{-1} - \alpha_{-1}')q^{-1} + \dots (\alpha_{-i} - \alpha'_{-i})q^{-i} \tag{1}
$$
Note that $i$ is meant to go up to negative infinity $-\infty$, where each value of $i$ is a negative nonzero integer. Thus, the first index of $-i$ is $-1$. 

Since $\alpha_{j} = \alpha'_{j}$ for all $j > k$, those terms vanish. This leaves the sum starting from the first differing digit $k$: 
$$
|x - x'| = \left|(\alpha_{k} - \alpha'_{{k}})q^k + [(\alpha_{-1} - \alpha'_{-1})q^{-1} + \dots + (a_{-k-1} - a'_{-k-1})q^{-k-1}  ] \right| \tag{2}
$$
Applying the inequality, which is seen in step 11 of the fact this proof points to, it has to be shown that $|x - x'| > 0$. This can be done with the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]]:
$$
|x - x'| \ge |\alpha_{k} - a'_{k}|q^{k} - |(\alpha_{-1} - \alpha'_{-1})q^{-1} + \dots + (\alpha_{-k-1} - \alpha'_{-k-1})q^{-k-1} | \tag{3}
$$
In standard $q$-adic system, the digits are bounded: $|\alpha_{-k-i} - \alpha'_{-k-i}| \le q - 1$. The tail of the sequence sums, where $(i < k)$, is a *geometric* sum of the sequences: 
$$
\begin{gather}
| (\alpha_{-1} - \alpha_{-1})q^{-1} + \dots + (\alpha_{-k-i} - a_{-k-i})q^{-k-i}| \le (q - 1) \cdot [(q^{k-2} + \dots q^{k - n - 1})] = (q-1) \cdot \left( \frac{q^{k-1}}{1 - 1/q} \right)  \\
= (q - 1) \cdot \frac{q^{k-1}}{(q-1)/q} = q^{k} \tag{4}
\end{gather}
$$
In many numerical systems, such as decimal, a number such as $0.4999\dots$ would be considered to equal $5000\dots$ This happens because the sum of the tail exactly reaches the value of the next digit. However, step 11 shows that a sequence $\{r_{n} \}$ converges to some value $x$ if it satisfies a specific rate of convergence. If two sequences $\{ r_{n}\}$ and $\{r'_{n} \}$ are distinct in their positional behavior, which means that they converge to different values $x$ and $x'$, then their symbols $\alpha$ and $\alpha'$ distinct. 

In conclusion, for any $k$, the value of the $k$-th digit is uniquely determined by the value of the number $x$ within an interval of width $q^k$. If $x \ne x'$, then there must be a $k$ such that $x$ and $x'$ fall into different "bins" defined by the positional power of $q$. Thus, different sequences of approximations $\{ r_{n} \}$ that satisfy the convergence criteria of the system will map to unique symbols $\alpha_{p}\dots a_{0},\dots$, which ensures a one-to-one correspondence between the unique real numbers and their unique representations. Note that this excludes the standard cases of repeating $q - 1$ tails. 
$$
\textbf{Q.E.D}
$$