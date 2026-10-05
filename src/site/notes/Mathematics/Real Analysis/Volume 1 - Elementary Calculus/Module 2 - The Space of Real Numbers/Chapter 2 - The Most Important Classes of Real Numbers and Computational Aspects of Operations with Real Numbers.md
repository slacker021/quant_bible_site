---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/","dg-note-properties":{}}
---

Having established the axiomatic foundation of the real numbers, it's time to turn to identifying several fundamental subsets within $\mathbb{R}$. While there's many real numbers that one could think of, these subsets form the most critical classes of real numbers that formulate the theoretical and fundamental foundations of computation-based mathematics. Furthermore, these subsets provide useful tools that enable the discovery of interesting properties that can be used to prove important statements. 

---
# The Natural Numbers and the Principle of Induction
The concept of an *inductive set* has several meanings in set theory. In the case of these notes, an inductive set is a *nonempty partially ordered* set where every element has a successor:
$$\begin{gather} \textbf{Definition: Inductive Set} \\ \text{A set } X \subset \mathbb{R} \text{ is inductive if for each number } x \in X, \text{ it also contains } x + 1. \end{gather}$$

>[!example]+ Example: The Set of Real Numbers being Inductive
>The set of real numbers $\mathbb{R}$ is an inductive set. Additionally, the set of positive numbers is also inductive. The intersection $X = \bigcap_{a \in A} X_{\mathcal{a}}$, if not empty, is an inductive set. More formally, 
>$$
>\begin{gather} \\
> \left( x \in X = \bigcap X_{\mathcal{a}} \right) \implies (\forall \mathcal{a} \in A (x \in X_{\mathcal{a}})) \implies  \\
> (\forall \mathcal{a} \in A ((x + 1)) \in X_{\mathcal{a}}) \implies \left((x + 1) \in \bigcap_{\mathcal{a} \in A} X_{\mathcal{a \in A}} X_{\mathcal{a}} = X \right) \tag{1}
\end{gather}
>$$

The example above provides the general idea and notation used to describe an inductive set. 

The most basic and intuitive subset of real numbers which can be described as inductive are the *natural numbers*:
$$\begin{gather} \textbf{Definition: The Set of Natural Numbers} \\ \text{The set of natural numbers, denoted } \mathbb{N}, \text{ is the smallest inductive set containing 1.} \\ \text{It is the intersection of all inductive sets that contain 1.} \end{gather}$$

>[!info]+ Remark: To or Not to Include $0$ as Part of the Natural Numbers?
>From a set-theoretic perspective, it might be more rational to begin the natural numbers with $0$. This would alter the definition of the set of natural numbers such that it's the smallest inductive set containing $0$. However, these notes will stick to the provided definition above. 
>
>Instead, the set of natural numbers with zero will be defined as the *whole numbers*. 

The definition of the natural numbers, where the set's smallest element begins at $1$, yields a direct corollary that serves as a vital proof technique:
$$\begin{gather} \textbf{Theorem: The Principle of Induction} \\ \text{If a subset } E \subset \mathbb{N} \text{ satisfies } 1 \in E \text{ and } (x \in E \implies (x + 1) \in E), \text{ then } E = \mathbb{N}. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Induction Works\|proof]])

This principle can be illustrated in action by having it prove several useful properties of the natural numbers that'll see constant use from now on:
$$\begin{gather} \textbf{Proposition: Properties of Natural Numbers} \\ \text{1. The sum and product of natural numbers are natural numbers.} \\ \text{2. } (n \in \mathbb{N}) \wedge (n \ne 1) \implies ((n - 1) \in \mathbb{N}). \\ \text{3. For any } n \in \mathbb{N}, \text{ the set } \{x \in \mathbb{N} \mid n < x\} \text{ contains a minimal element, namely, } \\ \min\{x \in \mathbb{N} \mid n < x\} = n + 1. \\ \text{4. } (m, n \in \mathbb{N}) \wedge (n < m) \implies (n + 1 \le m). \\ \text{5. } n + 1 \text{ is the immediate successor of } n \text{ in } \mathbb{N} \text{ (no natural numbers lie between them).} \\ \text{6. If } n \ne 1, n - 1 \text{ is the immediate predecessor of } n \text{ in } \mathbb{N}. \\ \text{7. Any nonempty subset of } \mathbb{N} \text{ contains a minimal element.} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

---
# Rational and Irrational Numbers

### Prelude to Rational Numbers: Integers
The notion of natural numbers can be extended to include the neutral element $0$ along with negative versions of said natural numbers. This leads to the formation of the set of *integers*:
$$\begin{gather} \textbf{Definition: The Integers} \\ \text{The set of integers, denoted } \mathbb{Z}, \text{ is the union of the set of natural numbers,} \\ \text{the set of their negatives, and zero.} \end{gather}$$
Like with natural numbers, operations involving integers yield integers:
$$
\begin{gather}
\textbf{Proposition: Adding and Multiplying Integers:} \\[5mm]
\text{The addition and multiplication of integers does not lead to a sum or } \\
\text{product that isn't an integer. }
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Integer Operations Yield Integers\|proof]])
The proposition above easily leads to the next realization:
$$
\begin{gather}
\textbf{Proposition: When Integers are Abelian} \\[5mm]
\mathbb{Z} \text{ is an abelian group with respect to addition. With respect to multiplication, } \mathbb{Z} \\
\text{isn't a group, nor is } \mathbb{Z}\setminus 0, \text{ since the reciprocals of the integers aren't in } \mathbb{Z}  \\
\text{except for the reciprocals of } 1 \text{ and } -1. 
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of When Integers are Abelian\|proof]])

> [!info]+ Remark: Divisibility 
> If $m, n \in \mathbb{Z}$ and $k = m \cdot n^{-1} \in \mathbb{Z}$, it is stated that $m$ is a *multiple* of $n$, or $n$ divides $m$. The latter statement can also be written as $m|n$. In other words, $n$ divides $m$ if and only if the product is an integer.

A special case of natural numbers is said to emerge from the natural numbers:
$$
\begin{gather}
\textbf{Definition: Prime Numbers} \\[5mm]
\text{A number } p \in \mathbb{N}, \text{ where } p \ne 1, \text{ is prime if it has no divisors in } \mathbb{N} \text{ except } 1 \text{ and } p. 
\end{gather}
$$
The prime numbers are used to construct a very important rule in elementary arithmetic:
$$\begin{gather} \textbf{Theorem: Fundamental Theorem of Arithmetic} \\ \text{Each natural number admits a representation as a product } n = p_1 \cdots p_k, \\ \text{where } p_i \text{ are prime numbers. This representation is unique except for the order of factors.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Fundamental Theorem of Arithmetic\|proof]])

>[!info]+ Remark: Relatively Prime
>Numbers $m,n \in \mathbb{Z}$ are said to be relatively prime if they've no common divisor except $1$ and $-1$. 

$$
\begin{gather}
\text{Euclid's Lemma: } \\[5mm]
\text{It follows from the fundamental theorem of arithmetic that if the product } \\
m \cdot n \text{ of relatively prime numbers } m \text{ and } n \text{ is divisible by a prime } p, \text{ then one of } \\
\text{ the two numbers is also divisible by } p.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Fundamental Theorem of Arithmetic\|proof]])

### Rational Numbers
With the notion of integers being well-defined, there may be instances where multiplying two integers, where one is in the form of a whole number while the other is in the form of $n_{1}/n_{2}$, yields a number that doesn't fit into the previous sets of numbers defined. Such a phenomenon requires the formation of another set of numbers: 
$$\begin{gather} \textbf{Definition: The Rational Numbers} \\[5mm] \text{Numbers of the form } m \cdot n^{-1} \text{ (or } m/n \text{), where } m, n \in \mathbb{Z} \text{ and } n \ne 0, \\ \text{are called rational. The set of rational numbers is denoted } \mathbb{Q}. \end{gather}$$
Any rational number can be represented by proportional pairs $(m_1, n_1)$ and $(m_2, n_2)$ where $m_1n_2 = m_2n_1$. Thus, the ordered pair $(m,n)$ of integers defines the rational number $q = m \cdot n^{-1}$ if $n \ne 0$. 

>[!info]+ Remark: Quotient
>The number $q = m \cdot n^{-1}$ can also be written as the *quotient* of $m$ and $n$, that is, as a so-called *rational fraction* $m/n$. 

##### Operations Involving Rational Numbers
One of the most fundamental rules involving rational numbers follows immediately from the definition of a rational number and the axioms for the real numbers. In particular, the value of a fraction is unchanged when both the *numerator*, which is the integer component at the top of the rational expression, and the *denominator*, which is the integer component at the bottom of the rational expression, are multiplied by the same non-zero integer $k$. Therefore, the fractions $mk/nk$ and $m/n$ represent the same rational number. In fact, since $(nk)(k^{-1}n^{-1}) = 1$, that is $(n \cdot k)^{-1} = k^{-1} \cdot n^{-1}$, the result is $(mk)(nk)^{-1} = (mk)(k^{-1}n^{-1}) = m \cdot n^{-1}$. 

Thus, the different ordered pairs $(m, n)$ and $(mk, nk)$ define the same rational number. Consequently, after suitable reductions, any rational number can be presented as an ordered pair of relatively prime integers. 

On the other hand, if the pairs $(m_{1}, n_{1})$ and $(m_{2}, n_{2})$ define the same rational number, that is $m_{1} \cdot n_{1}^{-1} = m_{2}n_{2}^{-1}$, then $m_{1}n_{2} = m_{2}n_{1}$, and if, for example, $m_{1}$ and $n_{1}$ are relatively prime, it follows from the corollary of the fundamental theorem of arithmetic mentioned above that $n_{2} \cdot n_{1}^{-1} = m_{2} \cdot m_{1}^{-1} = k \in \mathbb{Z}$. 

It has now been demonstrated that two ordered pairs $(m_{1},n_{1})$ and $(m_{2},n_{2})$ define the same rational number if and only they're proportional. That is, there's an integer $k \in \mathbb{Z}$ such that, for example, $m_{2} = km_{1}$ and $n_{2} = kn_{1}$.

---
# Irrational Numbers
The last type of real number is something that cannot be represented as an integer or rational number. In fact, attempting to represent this sorta number as a fraction leads to the number going on forever, which means that it cannot be represented in integer or rational terms. Instead, these numbers can only be represented in their "exact" form: 
$$\begin{gather} \textbf{Definition: The Irrational Numbers} \\[5mm] \text{Real numbers that are not rational are called irrational.} \end{gather}$$
The classical example of an irrational number is $\sqrt{ 2 }$. In the case of these notes, this is the first number that demonstrates the existence of irrational numbers within the wider realm of real numbers:
$$\begin{gather} \textbf{Proposition: Existence of Irrational Numbers} \\[5mm]\text{There exists a real number } s > 0 \text{ such that } s^2 = 2, \text{ and } s \notin \mathbb{Q} \text{ (denoted } \sqrt{2} \text{).} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that the Square Root of 2 is Irrational\|proof]])

> [!info]+ Remark: Algebraic vs. Transcendental 
> Real numbers are _algebraic_ if they are roots of polynomial equations with rational coefficients, which can be represented as 
> $$a_{0}x^{n} + \dots + a_{n - 1}x + a_{n} = 0 \tag{2}$$
 Otherwise, they are _transcendental_.

---
# The Principle of Archimedes
The *Principle of Archimedes* links order and completeness, with it being important in both its theoretical aspects and application of numbers in measurements and computations. 

>[!remark]+ Remark: The Principle of Archimedes
>In other axiomatic systems for the real numbers, the principle of Archimedes is considered a fundamental principle frequently included in the list of axioms. In these notes, this principle shall be proven using the axiom of completeness. 

Before the principle of Archimedes is to be proven, several important facts must be proven first: 
$$\begin{gather} \textbf{Proposition: Bounds in } \mathbb{N} \text{ and } \mathbb{Z} \\[5mm] \text{1. Any nonempty subset of } \mathbb{N} \text{ bounded above contains a maximal element.} \\ \text{2. The set } \mathbb{N} \text{ is not bounded above.} \\ \text{3. Any nonempty subset of } \mathbb{Z} \text{ bounded above contains a maximal element.} \\ \text{4. Any nonempty subset of } \mathbb{Z} \text{ bounded below contains a minimal element.} \\ \text{5. The set } \mathbb{Z} \text{ is unbounded above and below.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Bounds in the Natural Numbers and Integers\|proof]])
These facts can then be used to demonstrate that the Archimedes' principle holds true:

$$\begin{gather} \textbf{Theorem: The Principle of Archimedes} \\[5mm] \text{For any fixed positive number } h \text{ and any real number } x, \\ \text{there exists a unique integer } k \text{ such that } (k - 1)h \le x < kh. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Principle of Archimedes\|Proof]])

And now, some corollaries: 
$$\begin{gather} \textbf{Proposition: Corollaries to Archimedes' Principle} \\[5mm]\text{1. For any } \epsilon > 0, \text{ there exists } n \in \mathbb{N} \text{ such that } 0 < 1/n < \epsilon. \\ \text{2. If } x \ge 0 \text{ and } x < 1/n \text{ for all } n \in \mathbb{N}, \text{ then } x = 0. \\ \text{3. Between any real numbers } a < b, \text{ there is a rational } r \in \mathbb{Q} \text{ such that } a < r < b. \\ \text{4. For any } x \in \mathbb{R}, \text{ there exists a unique } k \in \mathbb{Z} \text{ such that } k \le x < k + 1. \\ \text{This } k \text{ is the integer part } [x], \text{ and } \{x\} := x - [x] \text{ is the fractional part.} \end{gather}$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Archimedian Corollaries\|proof]])

---
# Geometric Interpretation and Computations

The set $\mathbb{R}$ can be modeled geometrically as a continuous line where each point corresponds to a coordinate. This form of interpretation is often more intuitive and descriptive than relying purely on symbolics. By the axioms of Geometry, there's a one-to-one correspondence $f:\mathbb{L} \rightarrow \mathbb{R}$ between the points of a line $\mathbb{L}$ and the set $\mathbb{R}$ of real numbers. Furthermore, this correspondence is connected with the rigid motions of the line. To be specific, if $T$ is a parallel translation of the line $\mathbb{L}$along itself, there's a number $t \in \mathbb{R}$—which depends only on T—such that $f(T(x)) = f(x) + t$ for each point $x \in \mathbb{L}$. 

The number $f(x)$ corresponding to a point $x \in \mathbb{L}$ is the *coordinate* of $x$. In view of the one-to-one nature of the mapping $f:\mathbb{L} \rightarrow \mathbb{R}$, the coordinate of a point is often called simply a point. Given the correspondence $f:\mathbb{L} \rightarrow \mathbb{R}$, the line $\mathbb{L}$ is the *coordinate axis*, *number axis*, or the *real line*, and its points are called points of the real line. As 

As noted above, the bijective mapping $f:\mathbb{L} \rightarrow \mathbb{R}$ that defines coordinates on $\mathbb{L}$ has the property that under a parallel translation $T$ the coordinates of the images of points of the line $\mathbb{L}$ differ from the coordinates of the points themselves by a number $t \in \mathbb{R}$, the same for every point. For this reason, $f$ is determined completely by specifying the point that's to have coordinate $0$ and the point $1$. The *closed interval* determined by the ray with origin at $0$ containing $1$ is the *positive direction* and a motion in that direction (from $0$ to $1$) is the motion from left to right. In accordance with this convention, $1$ lies to the right of $0$ and $0$ to the left of $1$. 
Under a parallel translation $T$ that moves the origin $x_{0}$ to the point $x_{1} = T(x_{0})$ with coordinate $1$, the coordinates of the images of all pints are one unit larger than those of their [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 1 - General Mathematical Concepts and Notation/Chapter 4 - Functions and Cardinality\|pre-images]], and therefore, the point $x_{2} = T(x_{1})$ can be located with coordinate $2$, the point $x_{3} = T(x_{2})$ with coordinate $3$, ..., and the point $x_{n+1} = T(x_{n})$ with coordinate $n + 1$, as well as the point $x_{-1} = T^{-1}(x_{0})$ with coordinate $-1, \dots,$ the point $x_{{-n-1}} = T^{-1}(x_{-n})$ with coordinate $-n-1$. In this way, all the points with integer coordinates $m \in \mathbb{Z}$ are obtained. 

Knowing how to double, triple, ... the unit interval, the *Thales' Theorem* can be used to partition this interval into $n$ congruent subintervals: 
$$
\begin{gather}
\textbf{Thales' Theorem: } \\[5mm]
\text{If a line is drawn parallel to one side of a triangle to intersect the other two} \\
\text{sides in distinct point, the other two sides are divided in the same ratio. }
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Thales' Theorem\|Proof of Thales' Theorem]])
By taking the subinterval having an endpoint at the origin, it is revealed that the coordinate of its other end, which is denoted by $x$, satisfies the equation $n \cdot x = 1$, that is $x = \frac{1}{n}$. From this, all points with rational coordinates $\frac{m}{n} \in \mathbb{Q}$ are found. 

But there still remains points of $\mathbb{L}$, since it's been established that there're intervals incommensurable with the unit interval. Each such point, like every other point of the
line, divides the line into two rays, on each of which there are points with integer
or rational coordinates. (This is a consequence of the original geometric principle
of Archimedes.) Thus a point produces a partition, or, as it is called, a *cut* of $\mathbb{Q}$ into two nonempty sets $X$ and $Y$ corresponding to the rational points—points with rational coordinates—on the left and right-hand rays. By the axiom of completeness, there's a number $c$ that separates $X$ and $Y$, that is $x \le c \le y$ for all $x \in X$ and all $y \in Y$. Since $X \cup Y = \mathbb{Q}$, it follows that the supremum of $X$ is equal to $s$, which is equal to $i$, which is equal to the infimum of $Y$. For otherwise, $s < i$ and there'd be a rational number between $s$ and $i$ lying neither in $X$ nor in $Y$. Thus, $s = i = c$. This uniquely determined number $c$ is assigned to the corresponding point of line. 

The assignment of coordinates to points of the line just described provides a visualizable model for both the order relation in real numbers—hence it being a *linear ordering*—and for the axiom of completeness of continuity in the real numbers, which in geometry is interpreted as there being no "holes" or "gaps" in the line $\mathbb{L}$, which would separate it into two pieces having no points in common. 

It's with this geometric interpretation that the following notation and terminology for the number sets is listed below: 
$$\begin{gather} \textbf{Definition: Intervals} \\[5mm] \text{Open: } ]a, b[ := \{x \in \mathbb{R} \mid a < x < b\} \\ \text{Closed: } [a, b] := \{x \in \mathbb{R} \mid a \le x \le b\} \\ \text{Half-open: } ]a, b] := \{x \in \mathbb{R} \mid a < x \le b\}, \ [a, b[ := \{x \in \mathbb{R} \mid a \le x < b\} \\ \text{The length of interval } I \text{ with endpoints } a, b \text{ is } \vert{}I\vert{} = b - a. \end{gather}$$
*Open*, *closed*, and *half-open* intervals are called *numerical intervals* or simply *intervals*. The number determining an interval are called its *endpoints*.  The quantity $b-a$ can be described as the *length* of the interval. 

In accordance with the use of the symbols $+\infty$ (read as "positive infinity") and $-\infty$ (read as "negative infinity") it is customary to denote the fact that the numerical set $X$ is not bounded above (respectively below), by writing $\text{sup } X = +\infty$ and $\text{inf } X = -\infty$. 

An open interval can also have a specific point placed inside it:
$$\begin{gather} \textbf{Definition: Neighborhood} \\[5mm] \text{An open interval containing a point } x \in \mathbb{R} \text{ is a neighborhood of } x. \\ \text{A } \delta\text{-neighborhood of } x \text{ is } ]x - \delta, x + \delta[ \text{ (where } \delta > 0\text{).} \end{gather}$$
In particular, when $\delta > 0$, the open interval $]x - \delta, x + \delta[$ is the $\delta$-neighborhood of $x$ and has a length of $2\delta$. The distance between points $x, y \in \mathbb{R}$ is measured by the length of the interval having them as endpoints. The number $\frac{a+b}{2}$ is often called the *midpoint* or *center* of the interval with endpoints $a$ and $b$, since it is equidistant from the endpoints of the interval. In particular, a point $x \in \mathbb{R}$ is the center of its $\delta$-neighborhood $]x - \delta, x + \delta[$ and all points of the $\delta$-neighborhood lie at a distance from $x$ less than $\delta$. 

So as not to investigate which of the points is "left" and "right", that is, whether $x < y$ or $y < x$ and whether the length is $y - x$ or $x - y$, the useful functions below may be used:
$$\begin{gather} \textbf{Definition: Absolute Value and Distance} \\[5mm] \text{The absolute value } \vert{}x\vert{} \text{ is } x \text{ if } x \ge 0, \text{ and } -x \text{ if } x < 0. \\ \text{The distance between } x, y \in \mathbb{R} \text{ is } \vert{}x - y\vert{}. \end{gather}$$
The distance is nonnegative and equals zero only when the points x and y are
the same. The distance from $x$ to $y$ is the same as the distance from $y$ to $x$, since $|x - y| = |y - x|$. Finally, if $z \in \mathbb{R}$, then $|x - y| \le |x-z|+|z-y|$. That is, the so-called *triangle-inequality* holds. 

The triangle inequality follows from a property of the absolute value that is also
called the triangle inequality (since it can be obtained from the preceding triangle
inequality by setting $z = 0$ and replacing $y$ by $-y$: 
$$\begin{gather} \textbf{Proposition: The Triangle Inequality} \\[5mm] \vert{}x + y\vert{} \le \vert{}x\vert{} + \vert{}y\vert{} \\ \text{Equality holds if and only if } x \text{ and } y \text{ are both nonnegative or both nonpositive.} \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Triangle Inequality\|proof]])

### Errors in Computations
In measuring a real physical quantity, a number is obtained such that it changes when the measurement is repeated, especially if one changes either the method of making the measurement or the instrument used. Thus the result of measurement is usually an approximate value of the quantity being sought. The quality or precision of a measurement is characterized, for example, by the magnitude of the possible discrepancy between the true value of the quantity and the value obtained for it by measurement. When this is done, it may happen that the exact value of the measurement can never be acquired. Taking a more constructive position, however, involves getting the desired quantity with a preassigned precision. Taking this position is tantamount to identifying the number with a sequence of more and more precise approximations by numbers obtained from measurement. But every measurement is a finite set of comparisons with some standard or with a part of the standard commensurable with it, so that the result of the measurement will necessarily be expressed in terms of natural numbers, integers, or, more generally, rational numbers. Hence theoretically the whole set of real numbers can be described in terms of sequences of rational numbers by constructing, after due analysis, a mathematical
copy or, better expressed, a model of what people do with numbers who have no
notion of their axiomatic description. The latter add and multiply the approximate
values rather than the values being measured, which are unknown to them (To be
sure, they do not always know how to say what relation the result of these operations
has to the result that would be obtained if the computations were carried out with
the exact values. ). 

Having identified a number with a sequence of approximations to it, one should, for example, add the sequences of approximate values when one wishes to add two numbers.  The new sequence thus obtained must be regarded as a new number, called the sum of the first two. But is it a number? The subtlety of the question resides in the fact that not every randomly constructed sequence is the sequence of arbitrarily precise approximations to some quantity. That is, one still has to learn how to determine from the sequence itself whether it represents some number or not.
Another question that arises in the attempt to make a mathematical copy of operations with approximate numbers is that different sequences may be approximating sequences for the same quantity. The relation between sequences of approximations defining a number and the numbers themselves is approximately the same as that between a point on a map and an arrow on the map indicating the point. The arrow determines the point, but the point determines only the tip of the arrow, and does not exclude the use of a different arrow that may happen to be more convenient.

The reason this is important is because there's the theoretical possibility that more than one natural model of the real numbers may exist. In the real world, it's prudent to show the necessity of approximate computations. These approximate computations are both natural and necessary. These estimates are simple but important, which are precisely detailed as follows: 
$$\begin{gather} \textbf{Definition: Errors} \\[5mm] \text{If } x \text{ is exact and } \tilde{x} \text{ is an approximation:} \\ \text{Absolute error: } \Delta(\tilde{x}) := \vert{}x - \tilde{x}\vert{} \\ \text{Relative error: } \delta(\tilde{x}) := \Delta(\tilde{x}) / \vert{}\tilde{x}\vert{} \text{ (for } \tilde{x} \ne 0\text{)} \end{gather}$$
Since the value $x$ is unknow, the values of $\Delta(\tilde{x})$ and $\delta(\tilde{x})$ are also unknown. However, the upper bounds $\Delta(\tilde{x}) < \tilde{x}$ $\delta(\tilde{x}) < \tilde{x}$ for these quantities are usually known. In this case, the absolute or relative error doesn't exceed $\Delta$ or $\delta$ respectively. In practice, the only measures dealt with are the estimates for the errors, so that the quantities $\Delta$ and $\delta$ themselves are the *absolute* and *relative errors*. 

>[!info]+ Remark: Error Notation
>The notation $x = \tilde{x} \pm \Delta$ means that $\tilde{x} - \Delta \le x \le \tilde{x} + \Delta$. 

>[!example]- Example: Real-Life Quantities
>Several real-world quantities are measured in the form of $x = \tilde{x} \pm \Delta$ because there's always uncertainty when attempting to measure those values. No single method of measuring these real-world values is perfect, and almost all equations used to describe some phenomenon in the real world produce merely approximations. Furthermore, it's usually eneconomical to make measurements to extremely high degrees of precision (unless it's really needed). 
>Below are examples of real-world mathematical constants: 
>- The Gravitational constant $G = (6.672598 ± 0.00085) \cdot 10^{-11} \text{ N } \cdot \text{m}^2/\text{kg}^2$. 
>- The speed of light in a vacuum is $c = 299 792 458 \text{ m/s}$, which is the exact speed. 
>- Planck's constant of $h = (6.6260755 ± 0.0000040) \cdot 10^{-34} \text{ J} \cdot \text{s}$
>- Charge of an electron being $e = (1.60217733 ± 0.00000049) \cdot 10^{-19} \text{ C}$
>- Rest mass of an electron is $m_{e} = (9.1093897 ± 0.0000054) \cdot 10^{-31} \text{ kg}$
>  
>  The main indicator of the precision of a measurement is the relative error in approximation, usually represented in percent form. In the examples given above, the relative error are:
>- Gravitational constant: $13 \cdot 10^{-5}$
>- Speed of light: Zero
>- Planck's constant: $31 \cdot 10^{-7}$
>- Charge of an electron: $31 \cdot 10^{-8}$
>- Rest mess of an electron: $6 \cdot 10^{-7}$


Errors that arise in arithmetic operations with approximate quantities be estimated with the following proposition that is a direct result of the definition given to error propagation: 
$$\begin{gather} \textbf{Proposition: Propagation of Errors} \\[5mm] \Delta(\tilde{x} + \tilde{y}) \le \Delta(\tilde{x}) + \Delta(\tilde{y}) \\ \Delta(\tilde{x} \cdot \tilde{y}) \le \vert{}\tilde{x}\vert{}\Delta(\tilde{y}) + \vert{}\tilde{y}\vert{}\Delta(\tilde{x}) + \Delta(\tilde{x})\Delta(\tilde{y}) \\ \Delta\left(\frac{\tilde{x}}{\tilde{y}}\right) \le \frac{\vert{}\tilde{x}\vert{}\Delta(\tilde{y}) + \vert{}\tilde{y}\vert{}\Delta(\tilde{x})}{\tilde{y}^2 (1 - \delta(\tilde{y}))} \text{ (provided } \delta(\tilde{y}) < 1\text{)} \end{gather}$$

(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Error Propagation Methods\|proof]])

>[!info]+ Remark: Estimates for the Relative Errors
>These estimates for the absolute errors imply the following estimates for the relative errors:
>$$
>\begin{gather}
> \delta(\tilde{x} + \tilde{y}) \le \frac{\Delta(\tilde{x}) + \Delta(\tilde{y})}{|\tilde{x} + \tilde{y}|}  \\
> \delta(\tilde{x} \cdot \tilde{y}) \le \delta(\tilde{x}) + \delta(\tilde{y}) + \delta(\tilde{y}) \cdot \delta(\tilde{y}) \\
> \delta \left(\frac{\tilde{x}}{\tilde{y}} \right) \le \frac{\delta(\tilde{x}) + \delta(\tilde{y})}{1 - \delta(\tilde{y})}
\tag{3}
\end{gather}
>$$
>In practice, when working with sufficiently good approximations, there are $\delta(\tilde{y}) \approx 0$, $\delta(\tilde{x}) \cdot \delta(\tilde{y}) \approx 0$, and $1 - \delta(\tilde{y}) \approx 1$, so that one of the following can be used, even if they're not necessarily formally correct: 
>$$
>\begin{gather}
> 
>\Delta(\tilde{x} \cdot \tilde{y}) \le |\tilde{x}|\Delta(\tilde{y}) + |\tilde{y}|\Delta(\tilde{x})  \\
> \Delta \left( \frac{\tilde{x}}{\tilde{y}} \right) \le \frac{|\tilde{x}| \Delta(\tilde{y}) + \tilde{y} \Delta(\tilde{x})}{\tilde{y}^2} \\
> \delta(\tilde{x} \cdot \tilde{y} ) \le \delta(\tilde{x}) + \delta(\tilde{y})  \\
> \delta \left(\frac{\tilde{x}}{\tilde{y}} \right) \le \delta(\tilde{x}) + \delta(\tilde{y}) \tag{4}
\end{gather}
>$$
>The second and third formulae of step 3 show that it's necessary to avoid dividing by a number near zero and also to avoid using rather crude approximations in which $\tilde{y}$ or $1 - \delta(\tilde{y})$ is small in absolute value terms. Meanwhile, the first formula in the third step warns against adding approximate quantities if they're close to each other in absolute value terms but opposite in sign, since then $|\tilde{x} + \tilde{y}|$ is close to zero. In all these cases, there errors may increase sharply. 

>[!question]- Application: Measuring Height
>Jimbo measures his height using some device, and level of *precision* of said device is $\pm 0.5 \text{ cm}$. Suppose a sheet of paper was placed under his feet before the second measurement. The resulting measurements are
> - Height 1 $H_{1} = (200 \pm 0.05) \text{ cm}$ 
>- Height 2 $H_{2} = (199.8 \pm 0.05) \text{ cm}$
>  It doesn't make sense to try to find the thickness of the paper by getting the difference between $H_{2}$ and $H_{1}$, from which it would follow only that the thickness of the paper
>  is not larger than $0.08 \text{cm}$. That would of course be a crude reflection (if indeed one
>  could even call it a “reflection”) of the true situation.
>  
>  However, it's worthwhile to consider another more useful computational effect through which comparatively precise measurements can be carried out with crude devices. For example, if the device just used for measuring your height was used to measure the thickness of $1000$ sheets of the same paper, and the result was $(20 \pm 0.05) \text{ cm}$, then the thickness of one sheet of paper is $(0.02 \pm 0.0005) \text{mm}$. That is, with an absolute error not larger than $0.005 \text{mm}$, the thickness of one sheet is $0.2 \text{mm}$. Therefore, the relative error in this measurement is at most $0.025$. This idea can be developed and has been proposed, for example, as a way of detecting a weak periodic signal amid the larger random static usually called white noise.


---
# Application: Positional Computation System
While the most common number system is that of *decimal*, which consists of digits $0$ to $9$, it's possible to construct other number base representations with different amounts of digits—where each digit has a specific numerical value it represents. This ties in with the fact with any real number can be represented as a rational approximation. This can easily be done with the the following lemma, which is the primary method for the *positional computation system*: 

$$\begin{gather} \textbf{Lemma: Base representation} \\[5mm] \text{For a fixed base } q > 1 \text{ and any } x > 0, \text{ there exists a unique integer } k \text{ such that } q^{k-1} \le x < q^k. \end{gather}$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Positional Computational System\|proof]])
This lemma is used in the following construction, where $q > 1$ is fixed and an arbitrary positive number $x \in \mathbb{R}$ is taken. By the lemma of base representation, a unique number $p \in \mathbb{Z}$ is found such that 
$$
q^p \le x < q^{p + 1}. \tag{5}
$$
$$
\begin{gather}
\textbf{Definition: Order of } x \\[5mm]
\text{The number } p \text{ satisfying step 5 is the order of } x \text{ in the base } q  \\
\text{or (when q is fixed) simply the order of } x.  
\end{gather}
$$
By the principle of Archimedes, a unique natural number $\alpha_{p} \in \mathbb{N}$ can be found such that 
$$
\alpha_{p}q^{p} \le x < \alpha_{p}q^p + q^p. \tag{6}
$$
Taking step 5 into account, it can be asserted at $\alpha_{p} \in \{1, \dots, q - 1 \}$. It follows from the relation of step 6 and the principle of Archimedes that there's a unique number $\alpha_{p-1} \in \{1, \dots, q - 1 \}$ such that 
$$
\alpha_{p}q^p + \alpha_{p-1}q^{p-1} \le x < \alpha_{p}q^p +  \alpha_{p-1}q^{p-1} + q^{p-1}. \tag{7} 
$$
If $n$ such steps were made, the following relation can be obtained: 
$$
\begin{gather}
\alpha_{p}q^{p} + \alpha_{p-1}q^{p-1} + \dots + \alpha_{p-n}q^{p-n} \le x <  \\
\alpha_{p}q^p + \alpha_{p-1}q^{p-1} + \dots + \alpha_{p-n}q^{p-n} + q^{p-n} \tag{8} 
\end{gather}
$$
then by the principle of Archimedes, there's a unique number $\alpha_{p-n-1} \in \{0, 1, \dots, q -1 \}$ such that 
$$
\begin{gather}
\alpha_{p}q^{p} + \dots + \alpha_{p-n}q^{p-n} + \alpha_{p-n-1}q^{p-n-1} \le \\
x < \alpha_{p}q^{p} + \dots + \alpha_{p-n}q^{p-n} +  \alpha_{p-n-1}q^{p-n-1} +  q^{p-n-1} \tag{9}
\end{gather}
$$
These steps have led to the formation of an algorithm of which a sequence of numbers $\alpha_{p}, \alpha_{p-1}, \dots, \alpha_{p-n}, \dots$ from the set $\{ 0,1, \dots, q - 1\}$ is placed in correspondence with the positive number $x$. In other words, a sequence of numbers of the special form
$$
r_{n} = \alpha_{p}q^p + \dots + \alpha_{p-n}q^{p-n} \tag{10}
$$
has been constructed such that
$$
r_{n} \le x < r_{n} + \frac{1}{q^{n-p}} \tag{11}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Step 11\|proof]])

In other words, better approximations from below and above are constructed to the number $x$ using the special sequence seen in step 10. The symbol $\alpha_{p}\dots \alpha_{p-n}\dots$  is a code for the entire sequence $\{r_{n}\}$. To recover the sequence $\{r_{n}\}$ from this symbol, it's necessary to indicate the value of $p$ and order of $x$. For $p \ge 0$, it's customary to place a period or comma after $a_{0}$; for $p < 0$, the convention is to place $|p|$ zeros left of $\alpha_{p}$ and a period or comma right of the leftmost zero (recall that $\alpha_{p} \neq 0$). 

>[!example]- Example: Decimal Versus Binary
>The most common numbering system is decimal, which in the case of the system specified earlier would make $q = 10$. By definition, the decimal number $123.45$ would be
>$$
>\begin{gather}
>123.45 := 1 \cdot 10^2 + 2 \cdot 10^1 + 3 \cdot 10^0 + 4 \cdot 10^{-1} + 5 \cdot 10^{-2} \tag{12}
\end{gather}
>$$
>Meanwhile, the number $0.00123$ in decimal can be expanded to
>$$
>0.00123 := 1 \cdot 10^{-3} + 2 \cdot 10^{-4} + 3 \cdot 10^{-5} \tag{13}
>$$
>Meanwhile, representing a number in binary would mean that $q = 2$. For example, the binary digit 
>$$
>1000.001 := 1 \cdot 2^3 + 1 \cdot 2^{-3} \tag{14}
>$$

Thus, the value of a digit in the symbol $\alpha_{p}\dots \alpha_{p-n}\dots$ depends on the position it occupies relative to the period or comma. With this convention, the symbol $\alpha_{p}\dots \alpha_{0}\dots$ makes it possible to recover the whole sequence of operations. It can be seen in step 11 that different sequences $\{r_{n}\}$ and $\{r'_{n}\}$, and therefore different symbols $\alpha_{p}\dots a_{0},\dots$ and $\alpha'_{p}\dots a'_{0},\dots$ correspond to different numbers $x$ and $x'$. Therefore, there's no real number $x$ that corresponds to every symbol $\alpha_{p}\dots a_{0},\dots$. 

>[!info]- Remark
>By virtue of the algorithm just described for obtaining the numbers $\alpha_{p-1} \in \{1, \dots, q - 1 \}$ successively, it cannot happen that all these numbers from some point are equal to $q-1$. Indeed, if 
>$$
>r_{n} = \alpha_{p}q^{p} + \dots + \alpha_{p-k}q^{p-k} + (q-1)q^{p-k-1} + \dots + (q-1)q^{p-n} \tag{15}
>$$ 
>for all $n > k$, that is, 
>$$
>r_{n} = r_{k} + \frac{1}{q^{k-p}} - \frac{1}{q^{n-p}}, \tag{16}
>$$
>then by step 11, the result is 
>$$
>r_{k} + \frac{1}{q^{k-p}} - \frac{1}{q^{n-p}} \le x < r_{k} + \frac{1}{q^{k-p}}. \tag{17}
>$$
>Then for any $n > k$, 
>$$
>0 < r_{k} + \frac{1}{q^{k-p}} - x < \frac{1}{q^{n-p}}, \tag{18}
>$$
>which, as stipulated by step 11, is impossible. 
>
>It's also useful to note that if at least one of the numbers $\alpha_{p-k-1}, \dots, \alpha_{p-n}$ is less than $q - 1$, then instead of writing it as seen in step 18, it can be presented as 
>$$
>r_{n} < r_{n} + \frac{1}{q^{k-p}} - \frac{1}{q^{n-p}} \tag{19}
>$$
>or, what is the same
>$$
>r_{n} + \frac{1}{q^{n-p}} < r_{k} + \frac{1}{q^{k-p}} \tag{20}
>$$
>It's now possible to prove that any symbol $\alpha_{n}\dots a_{0},\dots$ composed of the numbers $\alpha_{k} \in \{1, \dots, q - 1 \}$, and in which there're numbers from different $q-1$ with arbitrarily large indices, corresponds to some number $x \ge 0$. Indeed, from the symbol $\alpha_{p}\dots a_{p-n},\dots$, the sequence $\{r_{n}  \}$ of the form in step 10 can be constructed. By virtue of the relations $r_{0} \le r_{1} \le r_{n} \le \dots$, taking account of step 10 and 11, the result is
>$$
>r_{0} \le r_{1} \le \dots \le \dots \le \dots \le r_{n} + \frac{1}{q^{n-p}} \le \dots \le r_{1} + \frac{1}{q^{1-p}} \le r_{0} + \frac{1}{q^{-p}} \tag{21}
>$$
>The strict inequalities from in this last relation should be understood as follows: every element of the left-hand sequence is less than every element of the right-hand sequence. This follows from step 20. 
>Taking $x = \text{sup}_{n \in \mathbb{N}}r_{n}(=\text{inf}_{n \in \mathbb{N}}(r_{n}) + q^{-(n-p)})$, then the sequence $\{r_{n}\}$ will satisfy steps 11 and 12, that is, the symbol $\alpha_{p}\dots \alpha_{p-n}\dots$ corresponds to the number $x \in \mathbb{R}$. 

Thus, a one-to-one correspondence between the positive numbers $x \in \mathbb{R}$ and the symbols of the form $\alpha_{p}\dots, \alpha_{0},\dots$ if $p \le 0$ or $0,0\dots 0 \alpha_{p}$ ($|p|$ zeros) if $p < 0$. The symbol assigned to $x$ is the $q$-ary representation of $x$; the numbers that occur in the symbol are called its *digits*, and the position of a digit relative to the period is called its *rank*. It's been established that to assign to a number $x <0$ the symbol for the positive number $-x$, prefixed by a negative sign. Finally, the symbol $0.0\dots0\dots0$ to the number $0$. Therefore, the positional $q$-*ary system* of writing real numbers has been constructed. 

>[!question]+ Application: Digital Computer Systems
>Digital computers make use of binary, which has the digits $0$ and $1$. Additionally, some advanced computer systems make use of *ternary* and *octal systems.* 

---
# Additional Useful Facts
$$
\begin{gather}
\textbf{Theorem: Isomorphism and Categoricity in } \mathbb{R} \\[5mm]
\text{Any two complete linearly ordered fields are isomorphic because of a unique} \\
\text{ order-preserving field isomorphism}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Isomorphism and Categoricity in the Real Numbers\|proof]])
This is the categorical closure of the axiomatic definition of $\mathbb{R}$. It guarantees that the axiomatic model that was constructed in this chapter is unique up to isomorphism, validating that all analytical derivations describe a universal mathematical structure rather than an arbitrary realization. 

$$
\begin{gather}
\textbf{Theorem: Dedekind's Cut Principle and Completeness Equivalence} \\[5mm]
\text{Any two complete linearly ordered fields are isomorphic via } \\
\text{a unique order-preserving field isomorphism.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Dedekind's Cut Theorem and Complete Equivalence\|proof]])
This can be considered the categorical closure of the axiomatic definition of $\mathbb{R}$. It guarantees that the axiomatic model constructed in the previous chapter is unique up to isomorphism, validating that all analytical derivations describe a universal mathematical structure rather than an arbitrary realization. 


$$
\begin{gather}
\textbf{Proposition: Monotonicity and Ordering of Extrema } \\[5mm]
\text{If } A \subset B \subset \mathbb{R}, \text{ then the sup}(A) \le \text{sup(B)}  \text{ and inf}(A) \ge \text{inf(B)}. \\
\text{If } X,Y \subset \mathbb{R} \text{ are non-empty sets such that } x \le y \text{ for all } x \in X, y \in Y, \text{ then } \\
\text{sup}(X) \le \text{inf}(Y).  \\[2.5mm]
\text{In other words, } X \cup Y = \mathbb{R}, then \text{sup}(X) = \text{sup(Y)}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Monotonicity and Ordering of Extrema\|proof]])
This is useful for handling bounds across subsets, approximations, and partitions. 

$$
\begin{gather}
\textbf{Proposition: Algebraic Operations on Bounded Sets} \\[5mm]
\text{Let } A+B \text{ be the set of the numbers of the form } a + b \text{ and }  \\
A \cdot B \text{ the set of numbers of the form } a \cdot b, \text{ where } a \in A \subset \mathbb{R} \\
\text{ and } b \in B \subset \mathbb{R}. \text{The following would then hold true: } \\[2.5mm]
\text{sup}(A + B) = \text{sup}(A) \\
\text{sup}(A \cdot B) = \text{sup}(A) \cdot \text{sup}(B)
\end{gather}
$$
This provides the foundational methods for bounding *Minkowski* set sums and products, which are used throughout variational formulations and *functional analysis*. 

$$
\begin{gather}
\textbf{Proposition: Bernouilli's Inequality} \\[5mm]
\text{For all } x > -1 \text{ and } n \in \mathbb{N}, (1 + x)^n \le 1 + nx, \text{ with equality if and only if } \\
n = 1 \text{ or } x = 0.  
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Bernoulli's Inequality\|proof]])

$$
\begin{gather}
\textbf{Proposition: Existence of Unique } n\text{-th Roots and Rational Exponentiation} \\[5mm]
\text{If } n \in \mathbb{N} \text{ and } a > 0 \text{ the equation } x^{n} = a \text{ has a positive root, which is denoted by } \sqrt[n]{a} \text{ or } a^{1/n} \\[2.5mm]
\text{For } a > 0, b > 0, \text{ and } n,m \in \mathbb{N}, \text{ the following hold true: } \\
\text{1. } \sqrt[n]{ab} = \sqrt[n]{a} \cdot \sqrt{b} \text{ and } \sqrt[n]{\sqrt[m]{a}} = \sqrt{n \cdot m}.  \\
\text{2. } (a^{1/n})^m = (a^m)^{1/n} =: a^{m/n} \text{ and } a^{1/n} \cdot a^{1/m} = a^{1/n + 1/m}. \\
\text{3. For all } r_{1},r_{2} \in \mathbb{Q}, \ a^{r_{1}} \cdot a^{r_{2}} = a^{r_{1} + r_{2}} \text{ and } (a^{r_{1}})^{r_{2}} = a^{r_{1}r_{2}} 
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of the Rules of Rational Expressions\|proof]])
These operations for roots and rational expressions are very useful in equations with radical expressions. 

$$
\begin{gather}\textbf{Proposition: Non-Archimedean Ordering Fields} \\[5mm]
\text{The field of rational functions } \mathbb{Q}(x) \text{ equipped with lexicographic ordering by highest-degree } \\
\text{forms an ordered field that is non-Archimedean.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Non-Archimedean Ordering Fields\|proof]])

$$
\begin{gather}
\textbf{Lemma: Von-Neumann Ordinal Embeddings} \\[5mm]
\text{The successor operation } x^+ = x \cup \{ x \} \text{ on Von Neumann} \\
\text{ordinals satisfy strict injectivity and the minimal element principal for } \\
\text{ subsets under inclusion.}
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Von-Neumann Ordinal Embeddings\|Proof of Von-Neumann Ordinal Embeddings]])

$$
\begin{gather}
\textbf{Lemma: Euclidean Algorithm}  \\[5mm]
\text{Let } m,n \in \mathbb{N} \text{ and } m > n. \text{Their greatest common divisor, gcd}(m,n) = d \in \mathbb{N} \text{ can be found } \\
\text{in a finite number of steps using the following algorithm of Euclid involving} \\
\text{successive divisions with remainder: } \\[2.5mm]
m = q_{1}n + r_{1} (r_{1} < n), \\
n = q_{2}r_{1} + r_{2} (r_{2} < r_{1}), \\
r_{1} = q_{3}r_{2} + r_{3} (r_{3} < r_{2}),  \\
\vdots \\
r_{k-1} = q_{k+1}r_{k} + 0.  \\[2.5mm]
\text{Then } d = r_{k}. \\[2.5mm]
\text{If } d = \text{gcd}(m,n), \text{ prime numbers } p,q \in \mathbb{Z} \text{ can be chosen such that } pm + qn = d;  \\
\text{in particular, if } m \text{ and } n \text{ are relatively prime, then } pm + qn = 1. 
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof that Euclid's Algorithm Works\|Proof that Euclid's Algorithm Works]])

$$
\begin{gather}
\textbf{Lemma: Properties of Order-Preserving Homomorphisms} \\[5mm]
\text{Any non-trivial ring homomorphism } f:\mathbb{R} \rightarrow \mathbb{R}' \text{ maps }  \\
0 \mapsto 0', 1 \mapsto 1', \text{ preserves positive rationals, and restricts to an order isomorphism on } \mathbb{Q}.
\end{gather}
$$
(see [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Proofs and Derivations/Chapter 2 - The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers/Proof of Properties of Order-Preserving Homomorphisms\|proof]])