
Vocab:
* Axiom: unproven statements on which all future arguments rest. Choice of axioms determines your math.
* Theorem: true, proven statement. 
* Lemma: a true statement used to prove a larger, more important statement 
* Conjecture: unproven statement said by someone important. 
	* conjecture + proof => theorem
* Corollary: true statements that follow directly from a theorem 

Example:
* an integer x is odd, if we can write it as x = 2*k + 1, for some integer k
* Axiom: every integer is even or odd, but not both
* Def: an integer x is even if we can write x = 2*k, for some integer k
* Definition: a number is rational if we can write it as a/b, where a and b are integers, and b is not 0
* Axiom: every rational has a fully simplified form
* Axiom: the integers are closed under addition and multiplication

Direct Proof
Prove $p\implies q$
1. Start by assuming p
2. intermediate steps
3. eventually show q as a consequence of p

Example
* Prove, by direct proof, that if n is odd, then $n^2$ is odd.
* Prove $p\implies q$ by direct proof

| Steps                         | Reasons                                                          |
|-------------------------------|------------------------------------------------------------------|
| n is odd                      | Assume p                                                         |
| n=2k+1, for some $\mathbb{Z}$ | definition of odd                                                |
| $n^2=(2k+1)^2$                | Square both sides                                                |
| $n^2=4k^2+4k+1$               | Expand                                                           |
| $n^2=2(2k^2+2k)+1$            | Factor out 2                                                     |
| $w=2k^2+2k$                     | define new variable                                              |
| w is an integer               | integers closed under multiplicaiton addition and exponentiation |
| $n^2=2w+1$, w is an integer   | Substitution w into expression                                   |
| $n^2$ is odd                  | Definitnion of Odd                                               |

Therefore, by direct proof, I have shown $p\implies q$

Definitions
* $\mathbb{Z}$ is the set of integers
* $\mathbb{Q}$ is the set of rationals
* $\in$ is in
* $x\in \mathbb{Z}$: x is an integer
* $\mathbb{Z}^{+}$: positive integer
* $\mathbb{R}$ is the set of reals


Prove by direct proof that the product of two square integers is itself a square.
(Rewrite as conditional)
Prove that, if x and y are squares, then xy is square.

p: x and y are squares
q: xy is a square
prove: $p\implies q$

![[IMG_7434.jpeg]]

Example:

![[IMG_7435.jpeg]]

Example:

