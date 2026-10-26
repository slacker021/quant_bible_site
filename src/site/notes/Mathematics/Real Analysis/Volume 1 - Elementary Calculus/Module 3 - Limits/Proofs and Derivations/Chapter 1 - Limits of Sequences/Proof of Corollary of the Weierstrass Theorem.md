---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-corollary-of-the-weierstrass-theorem/","dg-note-properties":{}}
---

# Corollary 1
Consider the sequence $y_n := \sqrt[n]{n} = n^{1/n}$ for $n \in \mathbb{N}$. Since $n \ge 1$ for all $n \in \mathbb{N}$, it follows that $y_n \ge 1$, meaning $\{y_n\}$ is bounded below by $1$.

It is established in the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Derivation of Euler's Constant\|derivation of Euler's number]] that the sequence $\left\{\left(1 + \frac{1}{n}\right)^n\right\}$ is strictly increasing and bounded above by $3$:
$$
\begin{gather}
\left(1 + \frac{1}{n}\right)^n < 3 \quad \forall n \in \mathbb{N} \tag{1}
\end{gather}
$$
Consequently, for every natural number $n \ge 3$, step 1 implies
$$
\begin{gather}
n \ge 3 > \left(1 + \frac{1}{n}\right)^n = \left(\frac{n + 1}{n}\right)^n = \frac{(n + 1)^n}{n^n} \tag{2}
\end{gather}
$$
Multiplying both sides of step 2 by $n^n > 0$ and taking the $n(n + 1)$-th root of both positive sides yields
$$
\begin{gather}
n^{n+1} > (n + 1)^n \iff n^{\frac{1}{n}} > (n + 1)^{\frac{1}{n+1}} \iff y_n > y_{n+1} \quad \forall n \ge 3 \tag{3}
\end{gather}
$$
Thus, for $n \ge 3$, the sequence $\{y_n\}$ is strictly decreasing and bounded below by $1$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], $\{y_n\}$ converges to a finite limit $L \ge 1$.

To determine $L$, consider the subsequence of even-indexed terms $y_{2n} = \sqrt[2n]{2n}$. Because the parent sequence $\{y_n\}$ converges to $L$, every subsequence of $\{y_n\}$ also converges to $L$. Rewriting $y_{2n}$ algebraically gives
$$
\begin{gather}
y_{2n} = (2n)^{\frac{1}{2n}} = 2^{\frac{1}{2n}} \cdot n^{\frac{1}{2n}} = \sqrt{\sqrt[n]{2}} \cdot \sqrt{\sqrt[n]{n}} = \sqrt{\sqrt[n]{2}} \cdot \sqrt{y_n} \tag{4}
\end{gather}
$$
Passing to the limit as $n \to \infty$ on both sides of step 4 and applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|arithmetic properties of limits]] together with the result $\lim_{n \to \infty} \sqrt[n]{2} = 1$ (established independently in Corollary 2 below) yields
$$
\begin{gather}
L = \sqrt{1} \cdot \sqrt{L} = \sqrt{L} \tag{5}
\end{gather}
$$
Squaring both sides of step 5 produces $L^2 = L \iff L(L - 1) = 0$. Since $L \ge 1$, it follows that $L = 1$, proving that $\lim_{n \to \infty} \sqrt[n]{n} = 1$.

---
# Corollary 2
Let $a > 0$ be an arbitrary positive real constant, and consider the sequence $x_n := \sqrt[n]{a} = a^{1/n}$. By trichotomy on $a > 0$, there are three exhaustive cases:

### First Case
Suppose $a > 1$. Then $x_n = a^{1/n} > 1$ for all $n \in \mathbb{N}$. Moreover, because $a > 1$ and the exponents satisfy $\frac{1}{n} > \frac{1}{n+1}$, the strict monotonicity of rational powers with base $a > 1$ guarantees that
$$
\begin{gather}
x_n = a^{\frac{1}{n}} > a^{\frac{1}{n+1}} = x_{n+1} \quad \forall n \in \mathbb{N} \tag{6}
\end{gather}
$$
Thus, $\{x_n\}$ is a strictly decreasing sequence bounded below by $1$. By the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Weierstrass Theorem on Monotonic Sequences\|Weierstrass Theorem on Monotonic Sequences]], $\{x_n\}$ converges to a finite limit $L \ge 1$. Extracting the even-indexed subsequence $x_{2n} = \sqrt[2n]{a}$, which must also converge to $L$, yields
$$
\begin{gather}
x_{2n} = \left(a^{\frac{1}{n}}\right)^{\frac{1}{2}} = \sqrt{x_n} \tag{7}
\end{gather}
$$
Taking the limit as $n \to \infty$ on both sides of step 7 gives
$$
\begin{gather}
L = \sqrt{L} \implies L^2 = L \implies L(L - 1) = 0 \tag{8}
\end{gather}
$$
Since $L \ge 1$, the unique valid root is $L = 1$. Thus, $\lim_{n \to \infty} \sqrt[n]{a} = 1$ for all $a > 1$.

### Second Case
Suppose $a = 1$. Then $x_n = \sqrt[n]{1} = 1$ for all $n \in \mathbb{N}$. Because $\{x_n\}$ is a constant sequence, the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|basic properties of limits]] guarantee that $\lim_{n \to \infty} \sqrt[n]{1} = 1$.

### Third Case
Suppose $0 < a < 1$, and define $b := \frac{1}{a} > 1$. By the First Case applied to $b > 1$, it holds that $\lim_{n \to \infty} \sqrt[n]{b} = 1 \neq 0$. Applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|quotient rule for limits]] yields
$$
\begin{gather}
\lim_{n \to \infty} \sqrt[n]{a} = \lim_{n \to \infty} \frac{1}{\sqrt[n]{b}} = \frac{1}{\lim_{n \to \infty} \sqrt[n]{b}} = \frac{1}{1} = 1 \tag{9}
\end{gather}
$$
Combining all three cases establishes that $\lim_{n \to \infty} \sqrt[n]{a} = 1$ for every $a > 0$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
