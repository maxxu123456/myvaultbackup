A set is an unordered collection of **distinct** objects.
Example {a,b,c}. This set has 3 elements.

$a \in A$ a is an element of A

Capital letters are sets and lowercase letters are elements.

The set of English vowels: {a,e,I,o,u}

The empty set is the set with nothing $ \emptyset$

List notation is using curly braces, which is only good for small finite sets.

We can use set builder notation.

{x| x has property P}

Ex:

{x| x is an odd integer and 0<x<10}

Or 


{x|x is an odd integer}

Or

{f(x)|  x has some property}

You would get all x then the set would contain f(that x) and other elements.

Example: 
{x^2| x is of and greater than 0 and less than 9}

……….


$\mathbb{Z}$ is the set of integers
$\mathbb{Q}$ is the set of rationals
$\mathbb{N}$ is the set of natural numbers 0,1,2,3,4,5,…
$\mathbb{R}$ is the set of reals
$\mathbb{C}$ is the set of complex numbers
$\mathbb{Z}^+$ is the positive integers

Intervals
(a,b) is {x|x in R and a<x<b}
[a,b] is closed


Set Equality

Two sets are equal if $\forall x(x \in A \iff x \in B)$



Hwo to prove two sets are equal?

Prove x in a implies x in b and vice versa.

Cardinality

|A| is the size of a.

|emptyset| = 1

$\subseteq$ means subset

A is a subset of B is for all x (x in A implies x in B)
$A\subseteq B$ if $\forall x(x\in A \implies x\in B)$

The set containing 1 is not a subset of the set containing $\mathbb{Z}$

$\subset$ means a proper subset

Meaning $A\subseteq B$ and $A\neq B$

Note: $S\subseteq S$ but not $S\subset S$



Power Set
$P(S)=\{s|s\subseteq S\}$

Example
$P(\{a,b\})=\{\{a\},\{b\},\{a,b\},\{\}\}$

$P(\{\}=\{\{\}\}$


Cartesian Product
An ordered pair (a,b). order matters, repetition allowed
(a,b) $\neq$ (b,a)

(a,a) is fine

$A\times B=\{(a,b)|a\in A\land b\in B\}$
Every possible pair (a,b)

$B\times B\times B\times B=B^4$

$A\times \emptyset=\emptyset$

Set operations

Union
$A\cup B$ = A Union B
= $\{x \in A\lor x \in B\}$
![[Pasted image 20240202101319.png]]
The set of all things that are in A or are in B or both 
$\mathbb{Z}^+\cup \mathbb{Z}^-\cup \{ 0 \}=\mathbb{Z}$

Intersection
$A\cap B$ = A Intersect B
=$\{ x|x \in A \land x \in B \}$
![[Pasted image 20240202101311.png]]
Example:
$A=\{ 1,2,3 \},B=\{ 2,4,6 \}$
$A\cap B=\{ 2 \}$

$\mathbb{Z}\cap \mathbb{R}=\mathbb{Z}$

These two sets are disjoint
$\mathbb{Z}^+\cap \mathbb{Z}^-=\emptyset$


Set Subtraction

A-B : $\{ x|x \in A \land x \not\in B \}$

$\mathbb{R}-\mathbb{Q}=\text{Irrational Numbers}$
$\mathbb{Z}-\mathbb{Q}=\emptyset$
![[Pasted image 20240202101330.png]]


Complement
We need to define a universe called $\mathcal{U}$
$A^c=\{ x|x \in \mathcal{U} \land x \not \in A \}$
$A^c =\mathcal{U}-A$

Example:

Universe is $\mathbb{R}$

$A=\{ x|\text{x is a even integer} \}$
$A^c=\text{odd integers} \cup \{ x|x\not \in \mathbb{Z}\land x \in \mathbb{R} \}$
![[Pasted image 20240202101849.png]]

## Set Proofs, Functions

$A\subseteq B$

Prove $x \in A \implies x \in B$

Disprove:

$\neg \forall x(x \in A \implies x \in B)$
$\exists x(x \in A \land \neg x \not \in B)$: Single counter example

$A \subset B$
1. Prove $A\subseteq B$
2. Prove $A\neq B$

Disprove
Either show
1.
![[Pasted image 20240205113655.png]]

Or 

2. A=B


How to prove that A = B

Prove $x \in A \iff x \in B$
1. $x \in A\implies x \in B$ ($A\subseteq B$)
2. $x \in B\implies x \in A$ ($B\subseteq A$)

Disprove it
show $\exists x(x \in A \land x \not \in B)$ or $\exists x(x \in B\land x\not \in A)$
Find something in one but not the other

Showing that $|A|\neq |B|$ shows that A is not a proper subset of B

![[Pasted image 20240205114137.png]]


![[Pasted image 20240213114935.png]]

## Functions

f: A $\to$ B
	f is a function from A to B, f assigns to each element of A an element of B
Def: A is the domain of f
Def B is the codomain of f




f(a)=b
f assigns b to a.
def: a is the pre image of b
def: b is the image of a

![[Pasted image 20240205114500.png]]

Range(f)=$\{ f(x)|x \in A \}$ i.e. the set of outputs/images that  actually occur

To be a well defined function, each pre-image must be assigned exactly one image

![[Pasted image 20240205114708.png]]

## Combining Functions

f: $\mathbb{Z}\to \mathbb{R}$
g: $\mathbb{Q} \to \mathbb{Z}$

$f\circ g$ is allowed since output of g matches input of f
$g\circ f$ is not allowed


### One-One (Injection)

A function is one to one if different inputs have different outputs

$\forall a\forall b(f(a)=f(b)\implies a=b)$

![[Pasted image 20240205115412.png]]

is $x\mapsto x^2$ one to one?
Depends
if$\mathbb{Z}\to \mathbb{Z}$
not since (-7)^2=7^2

if $\mathbb{N}\to \mathbb{N}$
then yes

![[Pasted image 20240205115546.png]]

![[Pasted image 20240205115732.png]]




Surjection (onto)

A function is onto if every element of the codomain is an image of something in the domain.
![[Pasted image 20240209093818.png]]
![[Pasted image 20240209093928.png]]

To prove a function is surjective, you must create a pre-image generator.

For f: A->B, a preimage generator g is such that, given a y in B, f(g(y)) = y

Example:

For each output, find pre-image

$x\mapsto x^2$
$\mathbb{R}\mapsto \mathbb{R}^+$

is this onto?

yes. $\sqrt{ y }$ or $-\sqrt{ y }$ is a preimage


For $\mathbb{N}\mapsto \mathbb{N}$  is $x\mapsto x+1$ onto?

No, 0 is not the image of any $x \in \mathbb{N}$

0 is the counterexample


If instead the function was on $\mathbb{Z}\mapsto \mathbb{Z}$ is it onto ?
Yes.

The generator is g(y)=y-1

![[Pasted image 20240209100223.png]]


## Bijection

A bijection is a function that is both one to one and onto.

Theorem: a function has an inverse if and only if it is bijective

A function $f^{-1}$ is the inverse of a funciton if and only if $f(f^{-1}(y))=y$
and $f^{-1}(f(x))=x$

## Floor and Ceiling


The floor of a number is the largest integer smaller than that number $\lfloor x\rfloor$

The ceiling of a number is the smallest integer not less than that number $\lceil x \rceil$

