Prove $\forall xP(x)$

Proof by cases: split domain into cases, cases must cover the entire domain

For example, split domain into even and odd

Example:
Prove $\forall x(x^2\geq x)$ x is an integer

Case 1: X is positive
x>0 definition of positive,
$x\geq 1$ definition of $\mathbb{Z}$
$x\cdot x\geq x$ multiply by x
$x^2\geq x$ math
This case hold

Case 2: x is negative
$x<0$ definition of negative
$x<1$  since 0<1
$x\cdot x>1*x$ multiply both sides by x and flip signs since x is negative
$x^2>x$ math
$x^2\geq x$ definiotn of $\geq$
This case holds

Case 3: x is 0
$x\cdot x=0\cdot x$. Multiply both sides by x
$x^2=0$ math
$x=x^2$ transitive property
$x^2\geq x$ definiton of $\geq$
This case holds

Since it is true for all cases, I have proven that $x^2$ is greater than or equal to  x for all integers x.

![[Pasted image 20240129100628.png]]

Proving $\exists xP(x)$

Constructive: actually find a specific x that satisfies P(x)
Non-construction: no actual specific x located

Example
Prove $\exists x(\text{x is the sum of its factors})$
for 6: 1,2,3. 6=1+2+3. Therefore I have proven this statement constructively.

Prove that there are two irrantional numbers x,y, such that $x^y$ is rational.

Check $\sqrt{ 2 }^{\sqrt{ 2 }}$

If it is rational then, we are done.

If it is irrational,
then

$(\sqrt{ 2 }^{\sqrt{ 2 }})^{\sqrt{ 2 }}$ is rational since it equals 2. Irrational ^ irrational = rational.

Since one of these 2 cases must hold, I have proven this statement nonconstructively.

Proving $\exists!xP(x)$
is equivalent to proving $\exists xP(x)\land \forall y\forall z(P(y)\land P(z)\implies y=z)$

1. Prove $\exists xP(x)$ (Construcitvely or not)
2. Prove $\forall y\forall z(P(y)\land P(z)\implies y=z)$ using direct, contrapostive, etc.

Rules of Inference for quantified Statements

Every GT student is busy. Tarun is a GT student.

$$\begin{align*}
\forall x[GT(x)\implies B(x)] \\ GT(\text{Tarun}) \\ GT(\text{Tarun})\implies B(\text{Tarun}) \\ \hline \therefore B(\text{Tarun})
\end{align*}$$


If you want to prove that some GT student is busy, use existential Generalision on $B(\text{Tarun})$
