---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-thales-theorem/","dg-note-properties":{}}
---

Let $\Delta ABC$ be a triangle, where $\overline{BC}$ is the base of the triangle, while $\overline{AB}$ is the left reg and $\overline{AC}$ is the right leg. Now, suppose that parallel to $\overline{BC}$ (more specifically, on top of $\overline{BC}$), there is another line that's shorter, which is denoted as $\overline{DE}$. Thus, it can be said that $BDEC$ form a trapezoid, where $D$ is a point on $\overline{AB}$ and $E$ is a point on $\overline{AC}$. Lastly, let $N$ be some point on $\overline{AD}$ and $M$ be some point on $\overline{AE}$. Thus, it can be said that $\Delta DEM$ forms a right triangle—where $M$ is the right angle—$\Delta EDN$ also forms a right triangle—where $N$ is the right angle. The entire figure needed for this proof is now complete. 

Now, suppose that the area of the triangle is to be defined as $\frac{1}{2} \cdot b \cdot h$, where $b$ is the base of the triangle and $h$ is the height. Thus, the ratio between the length of side $\overline{AD}$ and $\overline{BD}$ is
$$
\frac{\text{area of } \Delta ADE}{\text{area of } \Delta BDE} = \frac{\frac{1}{2} \cdot \text{ length of } \overline{AD} \cdot \text{ length of } \overline{EN}}{\frac{1}{2} \cdot \text{length of } \overline{BD} \cdot \text{ length of } \overline{EN}} = \frac{\text{length of } \overline{AD}}{\text{length of } \overline{BD}} \tag{1}
$$
while the ratio between the length of side $\overline{AE}$ and $\overline{EC}$ is
$$
\frac{\text{area of } \Delta ADE}{\text{area of } \Delta CDE} = \frac{\frac{1}{2} \cdot \text{ length of } \overline{AE} \cdot \text{ length of } \overline{DM}}{\frac{1}{2} \cdot \text{length of } \overline{EC} \cdot \text{ length of } \overline{DM}} = \frac{\text{length of } \overline{AE}}{\text{length of } \overline{EC}} \tag{2}
$$
However, the area of $\Delta BDE$ and $\Delta CED$ are equal with one anther because both share the same base and the same parallel line from steps 1 and 2. Therefore, steps 1 and 2 are a contradiction. Therefore, 
$$
\frac{\overline{AD}}{\overline{DB}} = \frac{\overline{AE}}{\overline{EC}} \tag{3}
$$
Which means that $\frac{\overline{AD}}{\overline{DB}}$ and $\frac{\overline{AE}}{\overline{EC}}$ are divided into the same ratio. 
$$
\textbf{Q.E.D}
$$
