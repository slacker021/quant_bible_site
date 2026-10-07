---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-induction-works/","dg-note-properties":{}}
---

# Reworded Theorem Statement
For this proof, the original theorem statement is reworded: 
For each positive integer $n$, let $P(n)$ be a statement. Now, assume that $P(1)$ is true—namely that $P(1)$ exists because it has a corresponding mapping for the domain element $1$—and that the implication
$$
\text{If } P(x), \text{ then } P(x + 1) \text{ is true for every positive integer } x \tag{1}
$$
then $P(n)$ is true for every positive integer $n$. 

---
# Actual Proof
Assume, to the contrary, that the theorem is false. Further assume that $P(1)$ is true and that the implication of step $1$ is also true. However, there's some positive integers $n$ for which $P(n)$ is a false statement. Let 
$$
S = \{n \in \mathbb{N} \ | \ P(n) \text{ is false }  \}. \tag{2}
$$
Since $S$ is a nonempty subset of $\mathbb{N}$, it follows by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|well-ordering principle]] that $S$ contains at a least a element $s$. Since $P(1)$ is true, $1 \not\in S$. Thus, $s \geq 2$ and $s - 1 \in \mathbb{N}$. Therefore, $s - 1 \not\in S$ and so $P(s - 1)$ is a true statement. By the implication of step $1$, $P(s)$ is also true and so $s \not\in S$. However, this contradicts the premise that $s \in S$. This is because $s$ is the least element in the set $S$. 
$$\textbf{Q.E.D}$$

