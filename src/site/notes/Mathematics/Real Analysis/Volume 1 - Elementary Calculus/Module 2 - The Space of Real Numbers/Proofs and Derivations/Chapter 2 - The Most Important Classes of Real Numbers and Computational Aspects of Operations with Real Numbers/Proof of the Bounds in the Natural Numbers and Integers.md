---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-bounds-in-the-natural-numbers-and-integers/","dg-note-properties":{}}
---

# Proposition 1
If $E \subset \mathbb{N}$ is the subset in question, then by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|least-upper-bound lemma]], $\exists!\text{sup}E = s \in \mathbb{R}$. By definition of the least upper bound, there's a natural number $n \in E$ satisfying the condition $s − 1 < n ≤ s$. But then, $n = \text{max} \ E$, since a natural number that is larger than $n$ must be at least $n + 1$, and $n + 1 > s$. 

---
# Proposition 2
This is a corollary of proposition 1. Otherwise, there would be a maximal natural number. However, it's known that $n < n + 1$. 

---
# Proposition 3
If $E \subset \mathbb{Z}$ is the subset in question, then by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|least-upper-bound lemma]], $\exists!\text{sup}E = s \in \mathbb{R}$. By definition of the least upper bound, there's a natural number $n \in E$ satisfying the condition $s − 1 < n ≤ s$. But then, $n = \text{max} \ E$, since a natural number that is larger than $n$ must be at least $n + 1$, and $n + 1 > s$. 

---
# Proposition 4
Let $A$ be a subset of $\mathbb{Z}$, and that there's a Now, suppose that $A$ has no minimum. Then for every $n \in \mathbb{Z}$ there must be some $a \in A$ such that $a < s$, which is a contradiction. 

>[!remark]+ Remark: Other (Less Efficient) Means of Proving
>This can be proven by repeating the proof for the first proposition and replacing $\mathbb{N}$ by $\mathbb{Z}$ and using the greatest-lower-bound principle. Alternatively, one can pass to the negatives of the numbers ("changing signs") and use what's been proven in proposition 3. 

---
# Proposition 5
This proposition follows from proposition 3 and 4, or directly from 2. 

### Proof that $\mathbb{Z}$ is Unbounded Above
Assume that the set of integers $\mathbb{Z}$ is bounded above. By definition, this implies there exists a least upper bound (supremum), $\varepsilon$, such that for every $z \in \mathbb{Z}, z \le \varepsilon$. According to the third proposition, if there's a subset of integers bounded by $\varepsilon$, there's a natural number (and thus an integer) $n$ such that: 
$$
\varepsilon - 1 < n < \varepsilon \tag{1}
$$
In this context, $n$ represents the maximal integer in the set. Because $n$ is an integer and the fact that the successor property of integers, as noted in the second proposition, the next consecutive integer is $n + 1$. From the inequality $\varepsilon - 1 < n$, $1$ can be added to both sides: 
$$
\varepsilon < n + 1 \tag{2}
$$
This is a contradiction because by the initial assumption, $n + 1$ must be less than or equal to $\varepsilon$ because $\varepsilon$ is the upper bound. Since $n + 1$ cannot be both less than or equal to $\varepsilon$ and strictly greater than $\varepsilon$, the initial assumption that $\mathbb{Z}$ is bounded above must be false. Therefore, the integers are unbounded above. 

### Proof that $\mathbb{Z}$ is Unbounded Below
Firstly, assume that the set of integers has a smallest integer. This smallest integer is to be denoted as $n$. Now, consider $n - 1$, which is also an integer. By definition, $n - 1$ is less than $n$, contradicting the assumption that $n$ is the smallest integer. Therefore, there is no smallest integer. 

Secondly, the fourth proposition states that if a set $A \subset \mathbb{Z}$ has no minimum, then for every $n \in \mathbb{Z}$ there must be some $a \in A$ such that $a < n$. Since the set of integers has no minimum, proposition 4 would show that there'll always be another integer $a$ such that $a < n$. This confirms that no matter how small an integer is chosen, there'll always be a preceding integer that's less. Therefore, it must be that the integers are unbounded below. 
$$
\textbf{Q.E.D}
$$


