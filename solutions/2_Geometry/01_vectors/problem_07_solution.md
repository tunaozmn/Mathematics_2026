# Exercise 7. Linear Dependence Without Heavy Computation

## Problem

Given

$$
u=(1,2,3),\qquad v=(2,4,6),\qquad w=(0,1,1).
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

> **Why this exercise:** develops the habit of recognizing structure before applying a computational procedure.

## Method

Vectors are linearly dependent if a linear combination of them equals the zero vector with coefficients that are not all zero.

If one vector is a scalar multiple of another, this immediately gives such a relation. We therefore inspect the coordinates before attempting any elimination or determinant calculation.

## Solution

### 1. Identify the relation between u and v

Each coordinate of $v$ is twice the corresponding coordinate of $u$:

$$
\begin{aligned}
2u
&=2(1,2,3) \\
&=(2,4,6) \\
&=v.
\end{aligned}
$$

Thus,

$$
v=2u.
$$

### 2. Decide whether the three vectors are independent

Rearranging the relation gives

$$
2u-v=0.
$$

Including $w$ explicitly, we have

$$
2u-v+0w=(0,0,0).
$$

The coefficients are $2,-1,0$, which are not all zero. Therefore, this is a nontrivial linear relation, and the three vectors are linearly dependent.

The coefficient of $w$ may be zero: linear dependence requires that not all coefficients are zero, not that every coefficient is nonzero.

### 3. Explain why no long calculation is needed

The relation $v=2u$ already proves dependence. Adding a third vector cannot remove this existing relation, so no elimination or determinant calculation is necessary.

Geometrically, $u$ and $v$ lie along the same line and point in the same direction. The vector $v$ is twice as long as $u$, but it introduces no new direction.

The vector $w$ is not a scalar multiple of $u$. Indeed, if $w=cu$, its first coordinate would force $c=0$, which would make all its coordinates zero. This contradicts $w=(0,1,1)$.

Thus, $u$ and $w$ provide two independent directions, while $v$ repeats the direction already supplied by $u$. Together, the three vectors span a plane rather than all of three-dimensional space.

## Verification

Check the dependence relation coordinate by coordinate:

$$
\begin{aligned}
2u-v+0w
&=2(1,2,3)-(2,4,6)+0(0,1,1) \\
&=(2-2,\;4-4,\;6-6) \\
&=(0,0,0).
\end{aligned}
$$

Since the coefficients are not all zero, this verifies that $u,v,w$ are linearly dependent.
