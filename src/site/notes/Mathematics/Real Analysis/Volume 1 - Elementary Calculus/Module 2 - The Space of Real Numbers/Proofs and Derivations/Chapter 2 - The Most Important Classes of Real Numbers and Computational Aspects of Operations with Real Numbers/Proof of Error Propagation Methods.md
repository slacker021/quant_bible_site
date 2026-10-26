---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-error-propagation-methods/","dg-note-properties":{}}
---

Let $x, y \in \mathbb{R}$ be exact quantities and $\tilde{x}, \tilde{y} \in \mathbb{R}$ be their respective approximations. Define the signed deviations $\alpha := x - \tilde{x}$ and $\beta := y - \tilde{y}$, so that

$$
\begin{gather}
x = \tilde{x} + \alpha \quad \text{and} \quad y = \tilde{y} + \beta \\[2mm]
|\alpha| = |x - \tilde{x}| = \Delta(\tilde{x}) \quad \text{and} \quad |\beta| = |y - \tilde{y}| = \Delta(\tilde{y}) \tag{1}
\end{gather}
$$

---
# Error of a Sum or Difference
For the sum or difference $\tilde{x} \pm \tilde{y}$ approximating $x \pm y$, applying the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|Triangle Inequality]] to step 1 yields
$$
\begin{gather}
\Delta(\tilde{x} \pm \tilde{y}) = |(x \pm y) - (\tilde{x} \pm \tilde{y})| = |\alpha \pm \beta| \le |\alpha| + |\beta| = \Delta(\tilde{x}) + \Delta(\tilde{y}) \tag{2}
\end{gather}
$$

---
# Error of a Product
For the product $\tilde{x} \cdot \tilde{y}$ approximating $x \cdot y$, expanding $x y = (\tilde{x} + \alpha)(\tilde{y} + \beta)$ and applying the Triangle Inequality and multiplicative property of absolute values gives
$$
\begin{gather}
\Delta(\tilde{x} \cdot \tilde{y}) = |x y - \tilde{x} \tilde{y}| = |(\tilde{x} + \alpha)(\tilde{y} + \beta) - \tilde{x} \tilde{y}| = |\tilde{x}\beta + \tilde{y}\alpha + \alpha\beta| \\[2mm]
\le |\tilde{x}||\beta| + |\tilde{y}||\alpha| + |\alpha||\beta| = |\tilde{x}|\Delta(\tilde{y}) + |\tilde{y}|\Delta(\tilde{x}) + \Delta(\tilde{x})\Delta(\tilde{y}) \tag{3}
\end{gather}
$$

---
# Error of a Quotient
Assume $\tilde{y} \ne 0$ and $\delta(\tilde{y}) = \frac{|\beta|}{|\tilde{y}|} < 1$. First, observe by the reverse triangle inequality that
$$
\begin{gather}
\left|1 + \frac{\beta}{\tilde{y}}\right| \ge 1 - \left|\frac{\beta}{\tilde{y}}\right| = 1 - \delta(\tilde{y}) > 0 \tag{4}
\end{gather}
$$

which ensures $y = \tilde{y}(1 + \beta/\tilde{y}) \ne 0$ and $\left|1 + \frac{\beta}{\tilde{y}}\right|^{-1} \le \frac{1}{1 - \delta(\tilde{y})}$. Expressing the exact quotient error over a common denominator and applying step 4 yields
$$
\begin{gather}
\Delta\left(\frac{\tilde{x}}{\tilde{y}}\right) = \left|\frac{x}{y} - \frac{\tilde{x}}{\tilde{y}}\right| = \left|\frac{x\tilde{y} - y\tilde{x}}{y\tilde{y}}\right| = \left|\frac{(\tilde{x} + \alpha)\tilde{y} - (\tilde{y} + \beta)\tilde{x}}{\tilde{y}^2 \left(1 + \frac{\beta}{\tilde{y}}\right)}\right| \\[2mm]
= \frac{|\alpha\tilde{y} - \beta\tilde{x}|}{\tilde{y}^2} \cdot \left|\frac{1}{1 + \frac{\beta}{\tilde{y}}}\right| \le \frac{|\tilde{x}||\beta| + |\tilde{y}||\alpha|}{\tilde{y}^2 (1 - \delta(\tilde{y}))} = \frac{|\tilde{x}|\Delta(\tilde{y}) + |\tilde{y}|\Delta(\tilde{x})}{\tilde{y}^2 (1 - \delta(\tilde{y}))} \tag{5}
\end{gather}
$$
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$