---
{"dg-publish":true,"permalink":"/mathematics/real-analysis/volume-1-elementary-calculus/module-3-limits/proofs-and-derivations/chapter-1-limits-of-sequences/proof-of-the-corollary-for-the-squeeze-theorem-of-limits/","dg-note-properties":{}}
---

The main thing to note is that
$$
-|x_{n}| \le x_{n} \le |x_{n}| \tag{1}
$$
Another thing to note is that
$$
\lim_{ n \to \infty }  (-|x_{n}|) = -\lim_{ n \to \infty } |x_{n}| = 0 \tag{2}
$$
It then follows that
$$
\lim_{ n \to \infty }  (-|x_{n}|) = \lim_{ n \to \infty }  |x_{n}| = 0 \tag{3}
$$
And so by the [[Mathematics/Real Analysis/Volume 1 - Elementary Calculus/Module 3 - Limits/Proofs and Derivations/Chapter 1 - Limits of Sequences/Proof of the Squeeze Theorem\|squeeze theorem]], it's demonstrated that $\lim_{ n \to \infty } x_{n} = 0$. 
$$
\textbf{Q.E.D}
$$
