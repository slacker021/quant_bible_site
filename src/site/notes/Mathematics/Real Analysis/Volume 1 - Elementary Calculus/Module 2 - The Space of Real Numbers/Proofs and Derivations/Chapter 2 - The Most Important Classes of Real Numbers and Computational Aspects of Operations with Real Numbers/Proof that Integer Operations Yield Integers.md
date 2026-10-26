---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-that-integer-operations-yield-integers/","dg-note-properties":{}}
---

Let $m, n \in \mathbb{Z}$. By definition, $\mathbb{Z} = \mathbb{N} \cup \{0\} \cup (-\mathbb{N})$, where $-\mathbb{N} = \{-k \mid k \in \mathbb{N}\}$.
# Closure Under Addition and Subtraction
First, observe that for any $z \in \mathbb{Z}$, its additive inverse $-z$ also belongs to $\mathbb{Z}$: 
1. If $z = 0$, then $-0 = 0 \in \mathbb{Z}$; if $z \in \mathbb{N}$, then $-z \in -\mathbb{N} \subset \mathbb{Z}$; and if $z = -k \in -\mathbb{N}$ with $k \in \mathbb{N}$, then $-z = -(-k) = k \in \mathbb{N} \subset \mathbb{Z}$. Because $m - n = m + (-n)$, closure under subtraction follows immediately once closure under addition is established.

To verify $m + n \in \mathbb{Z}$, consider the possible sign cases for $m$ and $n$:
1. **At least one summand is zero:** If $m = 0$, then $m + n = n \in \mathbb{Z}$; if $n = 0$, then $m + n = m \in \mathbb{Z}$.
2. **Both summands have the same sign:**
   * If $m, n \in \mathbb{N}$, then $m + n \in \mathbb{N} \subset \mathbb{Z}$ by [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Proposition 1 of the Properties of Natural Numbers]].
   * If $m, n \in -\mathbb{N}$, then $a := -m \in \mathbb{N}$ and $b := -n \in \mathbb{N}$. Thus, $a + b \in \mathbb{N}$, which implies $m + n = -(a + b) \in -\mathbb{N} \subset \mathbb{Z}$.
3. **Summands have opposite signs:** Without loss of generality (by commutativity of addition), suppose $m \in \mathbb{N}$ and $n \in -\mathbb{N}$, so that $b := -n \in \mathbb{N}$ and $m + n = m - b$. By trichotomy on $\mathbb{N}$, either $m = b$, $m > b$, or $m < b$:
   * If $m = b$, then $m - b = 0 \in \mathbb{Z}$.
   * If $m > b$, consider the set $S := \{x \in \mathbb{N} \mid b + x \le m\}$. Since $b < m$, [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Proposition 4 of the Properties of Natural Numbers]] gives $b + 1 \le m$, so $1 \in S \ne \emptyset$. Furthermore, every $x \in S$ satisfies $x < b + x \le m$, so choosing the maximal such $x \in \mathbb{N}$ (or by induction on $m$) yields $b + k = m$ for some $k \in \mathbb{N}$, meaning $m - b = k \in \mathbb{N} \subset \mathbb{Z}$.
   * If $m < b$, the symmetric argument yields $b - m = k \in \mathbb{N}$, so $m - b = -(b - m) = -k \in -\mathbb{N} \subset \mathbb{Z}$.

---
# Closure Under Multiplication
To verify $m \cdot n \in \mathbb{Z}$, evaluate the exhaustive cases for $m$ and $n$:
1. **At least one factor is zero:** If $m = 0$ or $n = 0$, then $m \cdot n = 0 \in \mathbb{Z}$.
2. **Both factors are non-zero:**
   * If $m, n \in \mathbb{N}$, then $m \cdot n \in \mathbb{N} \subset \mathbb{Z}$ by [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Properties of Natural Numbers\|Proposition 1 of the Properties of Natural Numbers]].
   * If $m, n \in -\mathbb{N}$, then $(-m) \in \mathbb{N}$ and $(-n) \in \mathbb{N}$, so the field axioms yield
     $$
     \begin{gather}
     m \cdot n = (-m) \cdot (-n) \in \mathbb{N} \subset \mathbb{Z} \tag{1}
     \end{gather}
     $$
   * If one factor belongs to $\mathbb{N}$ and the other belongs to $-\mathbb{N}$ (say, $m \in \mathbb{N}$ and $-n \in \mathbb{N}$), then $m \cdot (-n) \in \mathbb{N}$, which implies
     $$
     \begin{gather}
     m \cdot n = -(m \cdot (-n)) \in -\mathbb{N} \subset \mathbb{Z} \tag{2}
     \end{gather}
     $$
Thus, $\mathbb{Z}$ is closed under addition, subtraction, and multiplication.
$$
\begin{gather}
\textbf{Q.E.D}
\end{gather}
$$