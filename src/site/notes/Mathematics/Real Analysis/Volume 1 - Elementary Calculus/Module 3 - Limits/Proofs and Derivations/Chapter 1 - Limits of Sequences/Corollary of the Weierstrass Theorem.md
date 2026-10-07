---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/corollary-of-the-weierstrass-theorem/","dg-note-properties":{}}
---

# Corollary 1
Let the sequence $y_n = \sqrt[n]{n}$. For all $n \in \mathbb{N}$, $y_n \ge 1$. The inequality $y_n > y_{n+1}$ is equivalent to $n^{1/n} > (n+1)^{1/(n+1)}$. Raising both sides to the power of $n(n+1)$ yields
$$\begin{gather}
n^{n+1} > (n+1)^n  \\
n \cdot n^n > (n+1)^n \\
n > \left(\frac{n+1}{n}\right)^n = \left(1 + \frac{1}{n}\right)^n \tag{1}
\end{gather}$$

It was established during the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Derivation of Euler's Constant\|derivation of Euler's constant]] that the sequence $(1 + \frac{1}{n})^n$ is strictly increasing and bounded above by $3$. Therefore, for all $n \ge 3$, the inequality $n > \left(1 + \frac{1}{n}\right)^n$ is strictly true. Consequently, for $n \ge 3$, the sequence $y_n = \sqrt[n]{n}$ is strictly decreasing. Because $\{y_n\}$ forms a decreasing sequence bounded below by $1$, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem]] guarantees that it converges to a finite limit $L \ge 1$. Consider the subsequence of even indices, $y_{2n} = \sqrt[2n]{2n}$. Since the parent sequence converges to $L$, the subsequence must identically converge to $L$. By algebraic manipulation, 
$$y_{2n} = (2n)^{\frac{1}{2n}} = (2^{\frac{1}{2n}})(n^{\frac{1}{2n}}) = \sqrt{\sqrt[n]{2}} \cdot \sqrt{\sqrt[n]{n}} = \sqrt{\sqrt[n]{2}} \cdot \sqrt{y_n} \tag{2}$$
Taking the limit as $n \to \infty$ on both sides, and substituting the proven result from Part 2 ($\lim_{n \to \infty} \sqrt[n]{2} = 1$): 
$$L = \sqrt{1} \cdot \sqrt{L} = \sqrt{L} \tag{3}$$

Squaring both sides yields $L^2 = L$. Given the bound $L \ge 1$, it must be concluded that $L = 1$. Therefore, $\lim_{n \to \infty} \sqrt[n]{n} = 1$. 

---
# Corollary 2

### First Case
Let the sequence $x_n = \sqrt[n]{a}$. Because $a > 1$, it follows that $x_n > 1$ for all $n \in \mathbb{N}$. To show the sequence is monotonically decreasing, the terms $x_n = a^{1/n}$ and $x_{n+1} = a^{1/(n+1)}$ are compared. Since $a > 1$ and the exponent maintains the strict inequality $\frac{1}{n} > \frac{1}{n+1}$, it holds that $x_n > x_{n+1}$. Thus, $\{x_n\}$ is a strictly decreasing sequence bounded below by $1$. By the Weierstrass Theorem on Monotonic Sequences, $\{x_n\}$ converges to a definitive finite limit $L$, where $L \ge 1$. To find $L$, consider the subsequence of even indices, $x_{2n} = \sqrt[2n]{a}$. Since the parent sequence converges to $L$, any extracted subsequence must identically converge to $L$. By algebraic manipulation:  
$$x_{2n} = (a^{1/n})^{1/2} = \sqrt{x_n} \tag{4}$$
Taking the limit as $n \to \infty$ on both sides yields:  
$$L = \sqrt{L} \tag{5}$$
Squaring both sides gives $L^2 = L$, which factors to $L(L - 1) = 0$. Since $L \ge 1$, the only valid solution is $L = 1$. Thus, $\lim_{n \to \infty} \sqrt[n]{a} = 1$ for $a > 1$. 

### Second Case
In this case, the sequence is $x_n = \sqrt[n]{1} = 1$. This is an ultimately constant sequence, which strictly converges to $1$. This is proven by the fact that [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|constant sequences are convergent.]]

### Third Case
$0 < a < 1$ Let $b = \frac{1}{a}$. Because $0 < a < 1$, it definitively follows that $b > 1$. By the arithmetic properties of limits and the result from Case 1, the limit can be evaluated as
$$\lim_{n \to \infty} \sqrt[n]{a} = \lim_{n \to \infty} \frac{1}{\sqrt[n]{b}} = \frac{1}{\lim_{n \to \infty} \sqrt[n]{b}} = \frac{1}{1} = 1 \tag{6}$$
Thus, the limit evaluates to $1$ for all real numbers $a > 0$.
$$
\textbf{Q.E.D}
$$