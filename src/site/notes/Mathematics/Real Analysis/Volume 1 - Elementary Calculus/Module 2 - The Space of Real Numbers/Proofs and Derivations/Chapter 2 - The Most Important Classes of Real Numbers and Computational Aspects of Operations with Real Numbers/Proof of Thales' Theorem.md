---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-thales-theorem/","dg-note-properties":{}}
---

Consider a triangle $\triangle ABC$ with base $\overline{BC}$ and sides $\overline{AB}$ and $\overline{AC}$. Suppose a line segment $\overline{DE}$ is drawn parallel to the base $\overline{BC}$ such that it intersects $\overline{AB}$ at a distinct interior point $D$ and $\overline{AC}$ at a distinct interior point $E$.

Drop a perpendicular altitude $\overline{EN}$ from vertex $E$ onto the line containing $\overline{AB}$ (with foot $N$), and drop a perpendicular altitude $\overline{DM}$ from vertex $D$ onto the line containing $\overline{AC}$ (with foot $M$).

Recall from Euclidean geometry that the area of a triangle is equal to half the product of its base length and its corresponding altitude. Because triangles $\triangle ADE$ and $\triangle BDE$ share the common altitude $\overline{EN}$ perpendicular to the collinear bases $\overline{AD}$ and $\overline{DB}$, the ratio of their areas equals the ratio of their base lengths:
$$
\begin{gather}
\frac{\operatorname{Area}(\triangle ADE)}{\operatorname{Area}(\triangle BDE)} = \frac{\frac{1}{2} \cdot |\overline{AD}| \cdot |\overline{EN}|}{\frac{1}{2} \cdot |\overline{DB}| \cdot |\overline{EN}|} = \frac{|\overline{AD}|}{|\overline{DB}|} \tag{1}
\end{gather}
$$

Similarly, because triangles $\triangle ADE$ and $\triangle CDE$ share the common altitude $\overline{DM}$ perpendicular to the collinear bases $\overline{AE}$ and $\overline{EC}$, the ratio of their areas is given by
$$
\begin{gather}
\frac{\operatorname{Area}(\triangle ADE)}{\operatorname{Area}(\triangle CDE)} = \frac{\frac{1}{2} \cdot |\overline{AE}| \cdot |\overline{DM}|}{\frac{1}{2} \cdot |\overline{EC}| \cdot |\overline{DM}|} = \frac{|\overline{AE}|}{|\overline{EC}|} \tag{2}
\end{gather}
$$

Now compare the denominators $\operatorname{Area}(\triangle BDE)$ and $\operatorname{Area}(\triangle CDE)$. Both triangles $\triangle BDE$ and $\triangle CDE$ share the exact same base segment $\overline{DE}$, and their opposite vertices $B$ and $C$ lie on the line $\overline{BC}$, which is parallel to $\overline{DE}$ by hypothesis. Because the perpendicular distance between two parallel lines is constant, $\triangle BDE$ and $\triangle CDE$ possess equal altitudes relative to base $\overline{DE}$, which implies
$$
\begin{gather}
\operatorname{Area}(\triangle BDE) = \operatorname{Area}(\triangle CDE) \tag{3}
\end{gather}
$$

Substituting step 3 into the left-hand sides of steps 1 and 2 equates the two area ratios, establishing by transitivity that
$$
\begin{gather}
\frac{|\overline{AD}|}{|\overline{DB}|} = \frac{|\overline{AE}|}{|\overline{EC}|} \tag{4}
\end{gather}
$$
Thus, the parallel line $\overline{DE}$ divides the two sides $\overline{AB}$ and $\overline{AC}$ in the exact same ratio.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$