---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-error-propagation-methods/","dg-note-properties":{}}
---

Let $x = \tilde{x} + \alpha$ and $y = \tilde{y} + \beta$. Then 
$$
\begin{gather}
\Delta(\tilde{x} + \tilde{y}) = |(x + y) - (\tilde{x} + \tilde{y})| = |\alpha| + |\beta| = \Delta(\tilde{x}) + \Delta(\tilde{y}),  \\[2.5mm]
\Delta(\tilde{x} \cdot \tilde{y}) = |xy - \tilde{x} \cdot \tilde{y}| = |(\tilde{x} + \alpha)(\tilde{y} + \beta)  - \tilde{x} \cdot \tilde{y}| =  \\
|\tilde{x} \beta + \tilde{y} \alpha + \alpha \beta| \le |\tilde{x}||\beta| + |\tilde{y}||\alpha| + |\alpha \beta| =  \\
|\tilde{x}|\Delta(\tilde{y}) + |\tilde{y}|\Delta(\tilde{x}) + \Delta(\tilde{x}) \cdot \Delta(\tilde{y}) \\[2.5mm]
\Delta \left(\frac{\tilde{x}}{\tilde{y}} \right) = \left| \frac{x}{y} - \frac{\tilde{x}}{\tilde{y}} \right| = \left| \frac{x \tilde{y} - y \tilde{x}}{y \tilde{y}} \right| = \left| \frac{(\tilde{x} + \alpha) \tilde{y} - (\tilde{y} + \beta )\tilde{x}}{\tilde{y}^2} \right| \cdot \left| \frac{1}{1 + \beta/\tilde{y}} \right|  \\
\le \frac{|\tilde{x}||\beta| + |\tilde{y}||\alpha|}{\tilde{y}^2} \cdot \frac{1}{1 - \delta(\tilde{y})} = \frac{|\tilde{x}|\Delta(\tilde{y}) + |\tilde{y}|\Delta(\tilde{x})}{\tilde{y}^2} \cdot \frac{1}{1 - \delta(\tilde{y})}. \tag{1}
\end{gather}
$$
$$
\textbf{Q.E.D}
$$
