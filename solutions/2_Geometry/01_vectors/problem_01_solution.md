# Exercise 1. Vector Operations and Their Meaning

## Problem

For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute

$$
u+v,\qquad u-v,\qquad 3u-2v.
$$

Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

> **Why this exercise:** reinforces basic operations and immediately connects them with their geometric meaning.

## Method

Vector addition and subtraction are performed coordinate by coordinate. Multiplication by a scalar multiplies every coordinate by that scalar.

Geometrically, vectors represent displacements. Adding two vectors combines their displacements using the head-to-tail rule.

## Solution

### 1. Compute the sum

Add the corresponding coordinates:

$$
\begin{aligned}
u+v
&=(2+(-1),\;-1+4,\;3+2) \\
&=(1,3,5).
\end{aligned}
$$

### 2. Compute the difference

Subtract each coordinate of $v$ from the corresponding coordinate of $u$:

$$
\begin{aligned}
u-v
&=(2-(-1),\;-1-4,\;3-2) \\
&=(3,-5,1).
\end{aligned}
$$

Geometrically, subtraction means adding the opposite vector:

$$
u-v=u+(-v).
$$

### 3. Compute the linear combination

First, multiply each vector by its scalar:

$$
3u=(6,-3,9),
\qquad
2v=(-2,8,4).
$$

Then subtract:

$$
\begin{aligned}
3u-2v
&=(6-(-2),\;-3-8,\;9-4) \\
&=(8,-11,5).
\end{aligned}
$$

### 4. Explain vector addition geometrically

To construct $u+v$, draw $u$ first. Then translate $v$ so that its tail is at the head of $u$, keeping its length, direction, and orientation unchanged.

The vector from the starting point of $u$ to the endpoint of the translated $v$ is $u+v$.

For these vectors, starting at the origin and moving by $u$ takes us to $(2,-1,3)$. Moving by $v$ from there takes us to $(1,3,5)$, the endpoint of the sum.

Equivalently, if $u$ and $v$ are drawn from the same starting point, their sum is the diagonal from that point of the parallelogram they form.

## Verification

Using the calculated sum,

$$
\begin{aligned}
(u+v)-v
&=(1,3,5)-(-1,4,2) \\
&=(1-(-1),\;3-4,\;5-2) \\
&=(2,-1,3) \\
&=u.
\end{aligned}
$$

Thus, subtracting $v$ reverses the displacement contributed by $v$ and recovers $u$.

As an additional check on the linear combination,

$$
\begin{aligned}
(3u-2v)+2v
&=(8,-11,5)+(-2,8,4) \\
&=(6,-3,9) \\
&=3u.
\end{aligned}
$$
