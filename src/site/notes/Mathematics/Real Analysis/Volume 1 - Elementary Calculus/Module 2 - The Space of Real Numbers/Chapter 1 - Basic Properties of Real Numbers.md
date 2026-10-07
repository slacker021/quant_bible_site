---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/chapter-1-basic-properties-of-real-numbers/","dg-note-properties":{}}
---

# The Axiom System and Some General Properties of the Set of Real Numbers

Mathematical theories find application because they allow the transformation of one set of numbers—the initial data or collection of inputs—into another set, representing the intermediate or final objective of computations—which are usually seen as outputs. Thus, numerical-valued functions hold a distinguished position in mathematics and its applications. These functions, specifically differentiable ones, form the core subject of classical real analysis. However, a complete description of these functions' properties necessitates a precise definition of the set of real numbers on which they operate.

The concept of numbers is fundamental, yet achieving a rigorous understanding requires abstraction. This chapter aims to construct the universe of real numbers that are utilized in basic algebra and arithmetic, but in a more non-ambiguous fashion.  Given that real numbers are one of the most basic abstractions in mathematics, a dedicated course could even be provided for this topic. However, this module seeks only to unify and explain what the reader already knows from highschool and their everyday experience with counting. 

---
# Definition of the Set of Real Numbers

$$\begin{gather} \textbf{Definition: The Set of Real Numbers} \\[5mm] \text{A set } \mathbb{R} \text{ is called the set of real numbers, and its elements are real numbers,} \\ \text{if it satisfies the axioms of addition and multiplication.} \end{gather}$$
In the realm of real numbers, *addition* and *multiplication* form the two basic operations that can be performed on the numbers. 

### Axioms of Addition
$$
\begin{gather}
\textbf{Axioms of Addition} \\[5mm]
\text{An operation } \\[2.5mm] +:\mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}, \\[2.5mm] \text{ which is the operation of addition, is defined, according to each} \\
\text{ordered pair } (x,y) \text{ of elements } x,y \in \mathbb{R} \text{, which is the sum of  } x \text{ and } y\text{.} \\
\text{This operation satsfies the following conditions: } \\
\end{gather}
$$
$$
\begin{align}
& \text{1. There's a neutral element or identity element } 0 \text{, which is zero, such that } \\[2.5mm]
 & \mathmakebox[4][c]{x + 0 = 0 + x = x} \\[2.5mm]
& \text{2. For every element } x \in \mathbb{R}\text{, there's an element } -x \text{ such that } \\[2.5mm]
& \mathmakebox[3][c]{x + (-x) = (-x) + x = 0} \\[2.5mm] 
& \text{3. The operation } + \text{ is associative, that is, the relation } \\[2.5mm]
& \mathmakebox[3][c]{x + (y + z) = (x + y) + z} \\[2.5mm] 
& \text{4. The operation } + \text{ is commutative, that is, } \\[2.5mm]
& \mathmakebox[5.5][c]{x + y = y + x} \\[2.5mm]
\end{align}
$$

>[!info]+ Remark: Additive and Abelian Group 
> If an operation is defined on a set $G$ satisfying axioms 1-3, this is described as a *group structure* that's defined on $G$ or that $G$ is a group. If the operation is called addition, the group is an *additive group*. If it's also known that the operation is commutative, that is, condition 4 holds, the group is *commutative* or *Abelian.* Therefore, the four basic rules of addition assert that $\mathbb{R}$ is an additive abelian group. 

>[!danger]+ Intuition: Subtraction
>At first glance, subtraction appears to be its own operation. However, this is merely a facade; Subtraction is a unique case of addition involving the addition of negative numbers. 
### Axioms of Multiplication
$$
\begin{gather}
\textbf{Axioms of Multiplication} \\[5mm]
\text{An operation } \\[2.5mm]
• : \mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R},  \\[2.5mm]
\text{The operation of multiplication is defined, assigning to each ordered } \\
\text{pair } (x,y) \text{ of elements } x \text{ and } y \text{ of } \mathbb{R} \text{ a certain element } x \cdot y \in \mathbb{R}, \text{ which is the } \\
\text{product of } x \text{ and } y\text{. This operation satisfies the following conditions: } \\
\end{gather}
$$
$$
\begin{align}
& \text{1. There's a neutral element or identity element } 1 \in \mathbb{R} \setminus 0 \text{, which is one, such that } \\[2.5mm]
 & \mathmakebox[5][c]{x \cdot 1 = 1 \cdot x = x} \\[2.5mm]
& \text{2. For every element } x \in \mathbb{R} \setminus 0 \text{, there's an element } x^{-1} \in \mathbb{R} \text{, which is the inverse } \\[2.5mm] 
& \text{reciprocal of } x \text{ such that } \\[2.5mm]
& \mathmakebox[3.75][c]{x \cdot x^{-1} = x^{-1} \cdot x = 1} \\[2.5mm] 
& \text{3. The operation } • \text{ is associative, that is, the relation } \\[2.5mm]
& \mathmakebox[3.85][c]{x \cdot (y \cdot z) = (x \cdot y ) \cdot z} \\[2.5mm] 
& \text{4. The operation } • \text{ is commutative, that is, } \\[2.5mm]
& \mathmakebox[7.][c]{x \cdot y = y \cdot x} \\[2.5mm]
\end{align}
$$

>[!info]+ Remark: Multiplicative Group
>With respect to the operation of multiplication the set $\mathbb{R} \setminus 0$, as one can verify, is a *multiplicative group*. 

>[!danger]+ Intuition: Division
>Similar to the case of subtraction, division is merely a unique case of multiplication. To divide a number $x$ is to simply multiply it by $1/y$. This is a repeated form of subtraction. 
##### The Connection Between Addition and Multiplication
Multiplication is *distributive* to addition, that is
$$
\begin{gather}
\textbf{Axiom: The Connection Between Addition and} \\
\textbf{Multiplication} \\[5mm]
(x + y)z = xz + yz \ \forall x\forall y\forall z \in \mathbb{R}
\end{gather}
$$

>[!info]+ Remark: Commutativity of Multiplication
>By the commutativity of multiplication, this equality continues to hold if the order of the factors is reversed on either side. If two operations satisfying these axioms are defined on a set $G$, then $G$ is a *field*. 

### Order Axioms
In addition to the basic operations of multiplication and addition, two values or expressions can be compared in terms of their "value." This is involves the use of an *ordering* system, which are more commonly known as *inequalities*. Inequalities are based on the *Order Axioms*:
$$
\begin{gather}
\textbf{Axioms of Ordering: } \\[5mm]
\text{Between elements of } \mathbb{R} \text{ there's a relation } \leq, \text{ that is, for elements }  \\
x,y \in \mathbb{R} \text{ one can determine whether } x \leq y \text{ or not. For this to be true, } \\
\text{the following conditions must hold: }
\end{gather}
$$
$$
\begin{align}
\text{1. } & \forall x \in \mathbb{R} (x \leq x) \\
\text{2. } & (x ≤ y) ∧ (y ≤ x) ⇒ (x = y) \\
\text{3. } & (x ≤ y) ∧ (y ≤ z) ⇒ (x ≤ z) \\
\text{4. } & ∀x ∈ \mathbb{R} \ ∀y ∈ \mathbb{R} \ (x ≤ y) ∨ (y ≤ x)
\end{align}
$$
This relation $\leq$ on $\mathbb{R}$ is an *inequality*. A set on which a there's a relation between pairs of elements satisfying Axioms 1-2 is *partially ordered*. If in addition Axiom 3 holds, that is, any two elements are comparable, then the set is *linearly ordered.* Therefore, the set of real numbers is linearly ordered by the relation of inequality between elements. 

### The Axiom of Completeness (Continuity)
The final axiom of real numbers deals with *continuity*, which implies the lack of "gaps" or "holes" in the field of real numbers:
$$
\begin{gather}
\textbf{Axiom of Completeness: } \\[5mm]
\text{If } X \text{ and } Y \text{ are nonempty subsets of } \mathbb{R} \text{ having the property } \\
\text{such that } x \leq y \  \forall x \forall y\text{, then there's a } c \in \mathbb{R} \text{ such that } x \leq c \leq y \  \forall x \forall y
\end{gather}
$$

> [!info]+ Remark: Consistency and Categoricity 
> The list of axioms such that any set on which these axioms hold can be considered a concrete realization or model of the real numbers is now complete. This definition requires no prior knowledge about numbers. However, there's always the question of how is to be determined that these axioms are consistent. After all, these principles are assumed to be true without proof. 
> 
> Someone who never learned how to count or measure line segments, or even know the concepts of numbers altogether, would view these axioms as arbitrary. These leads to two questions in relation to any abstract system of axioms: 
> 1.  Are these axioms consistent? That is, does there exist a set satisfying all the
conditions just listed? This is the problem of consistency of the axioms.
> 2. Does the given system of axioms determine the mathematical object
uniquely? That is, as the logicians would say, is the axiom system categorical?
>
>Here, uniqueness must be understood as follows: If two people $A$ and $B$ construct models
independently, say of number systems $\mathbb{R}_{A}$ and $\mathbb{R}_{B}$ , satisfying the axioms, then a bijective correspondence can be established between the systems $\mathbb{R}_{A}$ and $\mathbb{R}_{B}$, say $f : \mathbb{R}_{A} → \mathbb{R}_{B}$ , preserving the arithmetic operations and the order, that is, 
> $$
>\begin{gather}
> f(x + y) = f(x) + f(y), \\
> f(x \cdot y) = f(x) \cdot f(y) \\
> x \leq y \iff f(x) \leq f(y)
>\end{gather}
>$$
> In this case, from the mathematical point of view, $\mathbb{R}_{A}$ and $\mathbb{R}_{B}$ are merely distinct but equally valid realizations
of the real numbers. For example, $\mathbb{R}_{A}$ might be the set of infinite decimal fractions and $\mathbb{R}_{B}$ the set of points on the real number line. Such realizations are *isomorphic* and the mapping $f$ is an *isomorphism*. The result of this mathematical activity
isn't about any particular realization, but about each model in the class of isomorphic models of the given axiom system. The rest of this
module won't focus on discussing the questions posed above, but instead confine itself to giving informative answers on them. 

---
# General Algebraic Properties of Real Numbers
Now that the axioms of addition, multiplication, and continuity have been established, useful facts can be deduced from these axioms that enable easier computation of real numbers. Beginning with useful facts and tricks for addition: 
$$\begin{gather} \textbf{Proposition: Consequences of the Addition Axioms} \\[5mm] \text{1. There is only one zero in the set of real numbers.} \\ \text{2. Each element of the set of real numbers has a unique negative.} \\ \text{3. In the set } \mathbb{R}, \text{ the equation } a + x = b \text{ has the unique solution } x = b + (-a) =: b - a. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Addition Axioms\|proof]])

$$\begin{gather} \textbf{Proposition: Consequences of the Multiplication Axioms} \\[5mm] \text{1. There is only one multiplicative unit (one) in the real numbers.} \\ \text{2. For each } x \ne 0, \text{ there is only one reciprocal } x^{-1}. \\ \text{3. For } a \in \mathbb{R} \setminus \{0\}, \text{ the equation } a \cdot x = b \text{ has the unique solution } x = b \cdot a^{-1}. \end{gather}$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Multiplication Axioms\|proof]])

$$\begin{gather} \textbf{Proposition: Consequences of the Connection Axiom} \\[5mm] \text{For any } x, y \in \mathbb{R}: \\ \text{1. } x \cdot 0 = 0 \cdot x = 0. \\ \text{2. } (x \cdot y = 0) \implies (x = 0) \lor (y = 0). \\ \text{3. } -x = (-1) \cdot x. \\ \text{4. } (-1)(-x) = x. \\ \text{5. } (-x) \cdot (-x) = x \cdot x. \end{gather}$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of the Consequences of the Connection Axioms\|proof]])

$$\begin{gather} \textbf{Proposition: Consequences of the Order Axioms} \\[5mm] \text{Strict inequality } x < y \text{ denotes } x \le y \text{ and } x \ne y. \\ \text{1. For any } x, y \in \mathbb{R}, \text{ precisely one holds: } x < y, x = y, x > y. \\ \text{2. For any } x, y, z \in \mathbb{R}: \\ (x < y) \wedge (y \le z) \implies (x < z) \\ (x \le y) \wedge (y < z) \implies (x < z) \end{gather}$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Order Axioms\|proof]])

$$\begin{gather} \textbf{Proposition: Consequences of Order with Addition and Multiplication} \\[5mm] \text{For any } x, y, z, w \in \mathbb{R}: \\ \text{1. } (x < y) \implies (x + z) < (y + z) \\ \text{2. } (0 < x) \implies (-x < 0) \\ \text{3. } (x \le y) \wedge (z \le w) \implies (x + z) \le (y + w) \\ \text{4. } (x \le y) \wedge (z < w) \implies (x + z < y + w) \\ \text{5. } (0 < x) \wedge (0 < y) \implies (0 < xy) \\ \text{6. } (x < 0) \wedge (y < 0) \implies (0 < xy) \\ \text{7. } (x < 0) \wedge (0 < y) \implies (xy < 0) \\ \text{8. } (x < y) \wedge (0 < z) \implies (xz < yz) \\ \text{9. } (x < y) \wedge (z < 0) \implies (yz < xz) \\ \text{10. } 0 < 1 \\ \text{11. } (0 < x) \implies (0 < x^{-1}) \\ \text{12. } (0 < x) \wedge (x < y) \implies (0 < y^{-1}) \wedge (y^{-1} < x^{-1}) \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of Consequences of Order with Addition and Multiplication\|proof]])

---
# The Completeness Axiom and Bounds
While the set of real numbers appears vast and infinite, it's nonetheless possible to construct subsets of it that are *uncountably finite*. This is the principle of *bounding*: 
$$
\begin{gather}  
\textbf{Definition: Bounded Sets} \\[5mm]
 \text{A set } X \subset \mathbb{R} \text{ is bounded above (respectively, bounded below) if there} \\ \text{exists a number } c \in \mathbb{R} \text{ such that } x \le c \text{ (respectively, } c \le x \text{) for all } x \in X. \\ \text{The number } c \text{ is called an upper bound (majorant) or lower bound (minorant).} \\ \text{A set bounded both above and below is called bounded.} 
\end{gather}
$$
Intuitively, the concept of bounded sets implies that some of them have a "largest" or "lowest" element that bounds the list on the "top" or "bottom." This calls for the description of a *minimal* or *maximal* element that bounds said subset:
$$
\begin{gather}  
\textbf{Definition: Maximal and Minimal Elements} \\[5mm] 
\text{An element } a \in X \text{ is the largest or maximal element (} \max X \text{) if } x \le a \text{ for all } x \in X: \\[2.5mm] (a = \max X) := (a \in X) \wedge \forall x \in X (x \le a). \\[2.5mm] \text{Similarly, for the minimal element (} \min X \text{):} \\[2.5mm] (a = \min X) := (a \in X) \wedge \forall x \in X (a \le x). 
\end{gather}
$$

>[!info]+ Remark: Maximal and Minimal Elements
>Not every bounded set has a maximal or minimal element. For example, $X = \{x \in \mathbb{R} \mid 0 \le x < 1\}$ has no maximum. While it has a minimum of $0$, it has no maximum because there are an infinite amount of real numbers between 0 (including 0, which is the minimum) and 1 (which is not a maximum because it isn't included in the list). By definition, $x < 1$ means that the value must be less than one but not one. 

$$\begin{gather} \textbf{Definition: Least Upper Bound and Greatest Lower Bound} \\[5mm] \text{The least upper bound (supremum) of a set } X \text{ bounded above is denoted } \sup X: \\[2.5mm] (s = \sup X) := \forall x \in X (x \le s) \wedge \forall s' < s \ \exists x' \in X (s' < x'). \\[2.5mm] \text{The greatest lower bound (infimum) of a set } X \text{ bounded below is denoted } \inf X: \\[2.5mm] (i = \inf X) := \forall x \in X (i \le x) \wedge \forall i' > i \ \exists x' \in X (x' < i'). \end{gather}$$
The notation used for defining the least upper and greatest lower bound is somewhat verbose. This calls for a more concise definition:
$$
\begin{gather}
\textbf{Definition: Least Upper and Greatest Lower Bound (Concise Version)} \\[5mm]
\text{sup} \ X:=\text{min}\{ c \in \mathbb{R} \ | \ \forall x \in X (x \le c)  \} \\[2.5mm]
\text{inf} \ X := \text{max} \{ c \in \mathbb{R} \ | \ \forall x \in X (c \le x) \}
\end{gather}
$$
Given that not every set has a minimal or maximal element, the definitions provided for the least upper and greatest lower bounds require an argument. This argument is provided in the following lemma:
$$\begin{gather} \textbf{Lemma: The Least Upper Bound Principle} \\[5mm] \text{Every nonempty set of real numbers that is bounded from above has a} \\ \text{unique least upper bound.} \end{gather}$$


(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of the Least Upper Bound Principle\|proof]])
Naturally, the existence and uniqueness of the greatest lower bound of a nonempty set of numbers that's bounded from below is analogous: 

$$
\begin{gather} 
\textbf{Lemma: The Greatest Lower Bound Principle} \\[5mm] \text{Every nonempty set of real numbers that is bounded from below has a} \\ \text{unique greatest lower bound.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 1 - Basic Properties of Real Numbers/Proof of The Greatest Lower Bound Principle\|proof]])