---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-2-the-space-of-real-numbers/proofs-and-derivations/chapter-2-the-most-important-classes-of-real-numbers-and-computational-aspects-of-operations-with-real-numbers/proof-of-the-positional-computational-system/","dg-note-properties":{}}
---

Let the set of numbers of the form $q^{k}$, where $k$ is a natural number, isn't bounded above. If it were, it would have a [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 2 - The Space of Real Numbers/Chapter 1 - Basic Properties of Real Numbers\|least upper bounds]] $s$, and by definition of the least upper bounds, there'd be a natural number $m \in \mathbb{N}$ such that
$$
\frac{s}{q} < q^{m} \le s. \tag{1}
$$
However, this would mean that $s < q^{m+1}$, so that could not be an upper bound of the set. 

Since $1 < q$, it follows that $q^m < q^n$ when $m < n$ for all $m,n \in \mathbb{Z}$. Hence, it's been shown that for every real number $c \in \mathbb{R}$, there's a natural number $N \in \mathbb{N}$ such that $c < q^{n}$ for all $n > N$. It would then follow that for any $\varepsilon > 0$, there's a $M \in \mathbb{N}$ such that $c < q^{n}$ for all natural numbers $m > M$. 

It suffices to set $c = 1/\varepsilon$ and $N = M$; then $1/\varepsilon < q^m$ when $m > M$. Thus, the set of integers $m \in \mathbb{Z}$ satisfying the inequality $x < q^m$ for $x > 0$ is bounded below. It therefore has a minimal element $k$, which is the one being searched for, since, for this integer, 
$$
q^{k-1} \le x < q^k. \tag{2}
$$
The uniqueness of such an integer $k$ follows from the fact that is $m$ and $n$ are integers, and for example $m < n$, then $m \le n - 1$.Hence if $q > 1$, then $q^{m} \le q^{n-1}$. Indeed, it can be seen from this remark that the inequalities
$$
q^{m-1} \le x < q^m \tag{3}
$$
and 
$$
q^{n-1} \le x < q^n, \tag{4}
$$
which imply 
$$
q^{n-1} \le x < q^m, \tag{5}
$$
are compatible if $m \ne n$. 
$$
\textbf{Q.E.D}
$$