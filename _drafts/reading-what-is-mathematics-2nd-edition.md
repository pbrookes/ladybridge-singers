---
layout: post
title: Reading "What Is Mathematics? 2nd Edition"
category: Notes
tags: [mathematics]
math: true
---
[*What Is Mathematics?: An Elementary Approach to Ideas and Methods*](https://en.wikipedia.org/wiki/What_Is_Mathematics%3F) is a mathematics book written by [Richard Courant](https://en.wikipedia.org/wiki/Richard_Courant) and [Herbert Robbins](https://en.wikipedia.org/wiki/Herbert_Robbins), first published in 1941. It is an introduction to mathematics, intended both for the mathematics student and for the general public. A second edition was published in 1996 with an additional chapter on recent progress in mathematics, written by [Ian Stewart](https://en.wikipedia.org/wiki/Ian_Stewart_(mathematician)).

This book is an attempt by the authors to combat the overspecialization and over-abstraction of modern mathematics: starting from the most basic elements, explaining the origin of modern mathematics.

- toc
{: toc }

## Chapter I. The Natural Numbers

The concept of natural numbers comes from the collection of concrete things. Mathematicians do not need to care about the philosophical aspects of this transition, but only need to use natural numbers as the basis, on which addition and multiplication are defined, and then study their properties.

### &sect;2. The Infinitude of the Number System. Mathematical Induction

#### 2. The Arithmetical Progression

$$
\sum_{i=1}^{n}i = \frac{n(n+1)}{2}
$$

Proof by mathematical induction: When \\(n=1\\), it is true. Suppose it is true for \\(n\\), then for \\(n+1\\),

$$
\sum_{i=1}^{n+1}i = \sum_{i=1}^{n}i + (n+1) = \frac{n(n+1)}{2} + (n+1) = \frac{(n+1)(n+2)}{2} \blacksquare
$$

#### 3. The Geometrical Progression

$$
\sum_{i=0}^{n}q^i = \frac{1-q^{n+1}}{1-q}
$$

where \\(q \neq 1\\).

Proof by mathematical induction: When \\(n=0\\), it is true. Suppose it is true for \\(n\\), then for \\(n+1\\),

$$
\sum_{i=0}^{n+1}q^i = \sum_{i=0}^{n}q^i + q^{n+1} = \frac{1-q^{n+1}}{1-q} + q^{n+1} = \frac{1-q^{n+2}}{1-q} \blacksquare
$$

#### 4. The Sum of the First n Squares

$$
\sum_{i=1}^{n}i^2 = \frac{n(n+1)(2n+1)}{6}
$$

Proof by mathematical induction: When \\(n=1\\), it is true. Suppose it is true for \\(n\\), then for \\(n+1\\),

$$
\begin{aligned}
\sum_{i=1}^{n+1}i^2 &= \sum_{i=1}^{n}i^2 + (n+1)^2 = \frac{n(n+1)(2n+1)}{6} + (n+1)^2 \\
&= \frac{(n+1)(n(2n+1)+6(n+1))}{6} \\
&= \frac{(n+1)(n+2)(2n+3)}{6} \blacksquare \\
\end{aligned}
$$

#### 5. An Important Inequality

$$
(1+p)^n \geq 1+np
$$

where \\(p>-1\\).

Proof by mathematical induction: When \\(n=1\\), it is true. Suppose it is true for \\(n\\), then for \\(n+1\\),

$$
(1+p)^{n+1} = (1+p)^n(1+p) \geq (1+np)(1+p) = 1 + (n+1)p + np^2 \geq 1 + (n+1)p \blacksquare
$$

#### 6. The Binomial Theorem

$$
(a+b)^n = \sum_{i=0}^n C_{i}^{n}a^{n-i}b^i
$$

where

$$
C_{i}^{n} = \frac{n!}{i!(n-i)!}
$$

It has these properties:

$$
\begin{aligned}
C_{i-1}^{n} + C_{i}^{n} &= \frac{n!}{(i-1)!(n-i+1)!} + \frac{n!}{i!(n-i)!} \\
&= \frac{n!}{i!(n-i)!}(\frac{i}{n+1-i}+1) \\
&= \frac{(n+1)!}{i!(n+1-i)!} \\
&= C_{i}^{n+1}
\end{aligned}
$$

$$
C_{0}^{n} = C_{n}^{n} = 1
$$

Proof by mathematical induction: When \\(n=1\\), it is true. Suppose it is true for \\(n\\), then for \\(n+1\\),

$$
\begin{align}
(a+b)^{n+1} &= (a+b)^n(a+b) = (\sum_{i=0}^n C_{i}^{n}a^{n-i}b^i)(a+b) \\
&=
\begin{aligned}
    C_{0}^{n}a^{n+1} + &C_{1}^{n}a^{n}b + C_{2}^{n}a^{n-1}b^2 + \cdots + C_{n-1}^{n}a^{2}b^{n-1} + C_{n}^{n}ab^n +\\
    & C_{0}^{n}a^{n}b + C_{1}^{n}a^{n-1}b^2 + \cdots + C_{n-2}^{n}a^{2}b^{n-1} + C_{n-1}^{n}ab^n + C_{n}^{n}b^{n+1}
\end{aligned}\\
&= C_{0}^{n+1}a^{n+1} + C_{1}^{n+1}a^{n}b + C_{2}^{n+1}a^{n-1}b^2 + \cdots + C_{n-1}^{n+1}a^{2}b^{n-1} + C_{n}^{n+1}ab^n + C_{n+1}^{n+1}b^{n+1} \\
&= \sum_{i=0}^{n+1} C_{i}^{n+1}a^{n+1-i}b^i \blacksquare
\end{align}
$$

## Supplement to Chapter I. The Theory of Numbers

### &sect;1. The Prime Numbers

#### 1. Fundamental Facts

Theorem: There are infinitely many primes.

Euclid's indirect proof remains a model of mathematical reasoning. Assume there are finite many primes, say \\(n\\), then we can number them: \\(p_1, p_2, \cdots, p_n\\). Now we form a number

$$
A = p_1p_2\cdots p_n+1
$$

\\(A\\) is larger than any \\(p\\), and it divided by any \\(p\\) always leaves a remainder \\(1\\), so \\(A\\) is also a prime. This is contradictory to our assumption. \\(\blacksquare\\)

In fact, the proof process shows us a method to construct an infinite array of primes:

$$
p_n = p_1p_2\cdots p_{n-1} + 1
$$

$$
p_1 = 2, p_2 = 3, p_3 = 7, p_4 = 43, p_5 = 1807, p_6 = 3263443, p_7 = 10650056950807
$$

Fundamental theorem of arithmetic: Every integer greater than 1 can be factored into a product of primes in only one way (ignoring the order of primes).

Proof by contradiction: Suppose there are integers that can be factored into two different products of primes, then there exist a smallest one \\(m\\),

$$
m = p_1p_2\cdots p_r = q_1q_2\cdots q_s
$$

where \\(p\\)'s and \\(q\\)'s are primes, and

$$
p_1 \leq p_2 \leq \cdots \leq p_r, q_1 \leq q_2 \leq \cdots \leq q_s
$$

For convenient, suppose \\(p_1 < q_1\\). Now we form an integer

$$
\begin{aligned}
m' &= m - p_1q_2q_3\cdots q_s \\
&= (q_1 - p_1)q_2q_3\cdots q_s \\
\end{aligned}
$$

So \\(0 < m' < m\\), that means \\(m'\\) can be factored into a product of primes in only one way. According to

$$
m' = p_1(p_2p_3\cdots p_r - q_2q_3\cdots q_s)
$$

we know that \\(p_1\\) is a factor of \\(m'\\). So the decomposition of \\(m'\\) must contains \\(p_1\\). Since \\(q_2, q_3, \cdots, q_s\\) are all greater than \\(p_1\\), \\(p_1\\) won't appear in \\(q_2q_3\cdots q_s\\). So that \\(p_1\\) is a factor of \\(q_1 - p_1\\), i.e. there is an integer \\(t\\),

$$
q_1 - p_1 = p_1 t \Rightarrow q_1 = p_1(t+1)
$$

This is contradictory to the fact that \\(q_1\\) is a prime. \\(\blacksquare\\)

An inference: If a prime \\(p\\) is a factor of the product \\(ab\\), then \\(p\\) must be a factor of either \\(a\\) or \\(b\\).

#### 2. The Distribution of the Primes
