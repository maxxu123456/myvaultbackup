Study of the properties of integers

$a|b$ "a divides b"

True if $\exists c\in \mathbb{Z}$ such that b = a\*c

$3|12$ is true
$5|27$ is not true
$3|-12$ is true

Theorom:
$a|b,a|c\implies a|b+c$
$a|b\implies a|bc$
$a|b,b|c\implies a|c$

Division "Algorithm": let $a\in \mathbb{Z},b \in \mathbb{Z}^+$ , then find unique q,r such that $q\in \mathbb{Z}, r\in \mathbb{Z}, 0\leq r<b$. a=$qb+r$
q = a div b
r = a mod b

$a\equiv_{m}b$ "a is equivalent to b mod m"

if $m|a-b$

Question:
IS $7\equiv_{3}22$ true?
$3|7-22$
$3|-15$
So its true

Theorem $a\equiv_{m}b \iff a\pmod m=b\pmod m$
Theorem $a\equiv_{m}b \iff b=a+mk(k\in \mathbb{Z})$

## Bases

Theorem: if b is an integer, base-b representations of numbers are unique. Can use golden ratio as base, but can write the same number different ways.

![[Pasted image 20240221100031.png]]


![[Pasted image 20240221100057.png]]



![[Pasted image 20240221100739.png]]

## Primes

A prime number is a positive integer $\geq 2$ whose only factors are 1 and itself.


Fundamental Theorem of Artihmatic
Every positive integer has a unique prime factorization (up to multiplicity)

Finding primes less than n: Sieve of Erasthenes


Write out all n integers in a $\sqrt{ n }$ x $\sqrt{ n }$ square. For all primes from 2 to $\sqrt{ n }$, keep the prime but cross out all factors. After this, any uncrossed numbers are primes.

To check if a number if primes check every prime from 2 up tp $\sqrt{ n }$


Let $\pi(x)$ = the number of primes less than x

Theorem: $\pi(x)\approx \frac{x}{\ln(x)}$

## Greatest Common Divisor

The gcd of a and b is the largest integer d such that d|a and d|b


if the gcd is 1, then a and b are relatively prime



Use the Euclidean algorithm to find GCD

## Mod Inverse

We want to solve $5x-2\equiv 4\pmod {11}$

We get $5x\equiv 6\pmod{11}$
We use the fact that $5\cdot 9\equiv 1 \pmod{11}$

Multiply both sides by 9

$5\cdot 9x\equiv 54\pmod{11}$
$x\equiv 10\pmod{11}$

Theorem: $a^{-1}\pmod{m}$ exists if and only if $\gcd(a,m)=1$
so basically when a and m are relatively prime





$\phi(n)$ = # positive integers < n that are relatively prime to n

$\phi(p)=p-1$ if p is prime

Suppose prime factorization of n:

$p_{1}^{a_{1}}p_{2}^{a_{2}}\dots$
$\phi(n)=n\left( 1-\frac{1}{p_{1}} \right)\left( 1-\frac{1}{p_{2}} \right)\cdot\dots$
## Chinese Remainder Theorem

Chinese Remainder Theorem Statement
Given a set of mod equivalences
$x\equiv a_{1}\pmod{m_{1}}$
$x\equiv a_{2} \pmod{m_{2}}$
$x \equiv a_{3} \pmod{m_{3}}$

A solution exists as long as m1 and m2 and m3 are relatively prime, there is one solution 0<x<m1\*m2\*m3

Construct an x that works
![[Pasted image 20240228095249.png]]

![[Pasted image 20240228095402.png]]






