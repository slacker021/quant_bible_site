---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-weierstrass-theorem-on-monotonic-sequences/","dg-note-properties":{}}
---

# Theorem 1
Let $\{x_n\}$ be a nondecreasing sequence of real numbers, meaning $x_1 \le x_2 \le \dots \le x_n \le x_{n+1} \le \dots$.

### Necessity
Assume the nondecreasing sequence $\{x_n\}$ converges to a finite real limit $L \in \mathbb{R}$. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|Theorem 4 of the Basic Properties of Limits]], every convergent sequence is bounded. Consequently, $\{x_n\}$ is bounded above.

### Sufficiency
Conversely, assume the nondecreasing sequence $\{x_n\}$ is bounded above. Define the nonempty set of all sequence terms $S := \{x_n \mid n \in \mathbb{N}\} \subset \mathbb{R}$. Because $S$ is nonempty and bounded above, the [[Proof of the Supremum Principle\|Supremum Principle]] (derived from the Axiom of Completeness) guarantees that $S$ possesses a unique finite supremum $L := \sup S \in \mathbb{R}$.

Let $\varepsilon > 0$ be arbitrary. Because $L = \sup S$ is the *least* upper bound of $S$, the strictly smaller quantity $L - \varepsilon < L$ cannot be an upper bound of $S$. Consequently, there exists at least one index $N \in \mathbb{N}$ such that
$$
\begin{gather}
x_N > L - \varepsilon \tag{1}
\end{gather}
$$
Because $\{x_n\}$ is nondecreasing, $x_n \ge x_N$ holds for all $n > N$. Combining this with step 1 by transitivity yields
$$
\begin{gather}
x_n \ge x_N > L - \varepsilon \quad \forall n > N \tag{2}
\end{gather}
$$
Simultaneously, because $L = \sup S$ is an upper bound for $S$, every term of the sequence satisfies $x_n \le L < L + \varepsilon$ for all $n \in \mathbb{N}$. Combining this upper bound with step 2 shows that for all $n > N$:
$$
\begin{gather}
L - \varepsilon < x_n \le L < L + \varepsilon \implies |x_n - L| < \varepsilon \tag{3}
\end{gather}
$$
Thus, $\{x_n\}$ converges to its supremum $L = \sup_{n \in \mathbb{N}} x_n$.

---
# Theorem 2
Let $\{y_n\}$ be a nonincreasing sequence of real numbers, meaning $y_1 \ge y_2 \ge \dots \ge y_n \ge y_{n+1} \ge \dots$.

### Necessity
Assume the nonincreasing sequence $\{y_n\}$ converges. By [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Basic Properties of Limits\|Theorem 4 of the Basic Properties of Limits]], $\{y_n\}$ is bounded, and is therefore bounded below.

### Sufficiency
Conversely, assume the nonincreasing sequence $\{y_n\}$ is bounded below by $m \in \mathbb{R}$, so $y_n \ge m$ for all $n \in \mathbb{N}$. Define the reflected sequence $z_n := -y_n$ for each $n \in \mathbb{N}$, and let $Y := \{y_n \mid n \in \mathbb{N}\}$ and $Z := \{-y_n \mid n \in \mathbb{N}\} = -Y$. Multiplying $y_n \ge y_{n+1} \ge m$ by $-1$ reverses the inequalities:
$$
\begin{gather}
z_n = -y_n \le -y_{n+1} = z_{n+1} \le -m \quad \forall n \in \mathbb{N} \tag{4}
\end{gather}
$$
Step 4 demonstrates that $\{z_n\}$ is a nondecreasing sequence bounded above by $-m$. By Theorem 1 established above, $\{z_n\}$ converges to its supremum $\lim_{n \to \infty} z_n = \sup Z = \sup(-Y)$.

By the reflection identity $\sup(-Y) = -\inf Y$ established in the [[Proof of the Infimum Principle\|Infimum Principle]] and the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of Arithmetic Operations Involving Limits\|scalar multiplication property of limits]],
$$
\begin{gather}
\lim_{n \to \infty} y_n = \lim_{n \to \infty} (-z_n) = -\lim_{n \to \infty} z_n = -\sup(-Y) = \inf Y = \inf_{n \in \mathbb{N}} y_n \tag{5}
\end{gather}
$$
Thus, $\{y_n\}$ converges to its infimum $\inf_{n \in \mathbb{N}} y_n$.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$
