# Exercise 10. A Polynomial Through Three Points

## Problem

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.

## Method

If the graph passes through a point $(x,y)$, then $p(x)=y$.

Substituting the three given points produces three linear equations in the unknown coefficients $a,b,c$. We solve this system and then check the resulting polynomial at each given input.

Although the polynomial contains $x^2$, the system is linear in $a,b,c$, which are the unknowns in this problem.

## Solution

### 1. Translate the points into equations

The point $(0,1)$ gives

$$
p(0)=a\cdot0^2+b\cdot0+c=1,
$$

so

$$
c=1.
$$

The point $(1,3)$ gives

$$
p(1)=a+b+c=3.
$$

The point $(2,9)$ gives

$$
p(2)=4a+2b+c=9.
$$

Therefore, the coefficients must satisfy

$$
\begin{cases}
c=1, \\
a+b+c=3, \\
4a+2b+c=9.
\end{cases}
$$

### 2. Substitute the known value of c

Using $c=1$ in the remaining equations gives

$$
\begin{cases}
a+b=2, \\
4a+2b=8.
\end{cases}
$$

The augmented matrix for this reduced system, using the variable order $a,b$, is

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
4 & 2 & 8
\end{array}
\right].
$$

### 3. Solve for a and b by elimination

Apply

$$
R_2\leftarrow R_2-4R_1.
$$

This gives

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -2 & 0
\end{array}
\right].
$$

The second row represents

$$
-2b=0,
$$

so $b=0$.

Substituting into $a+b=2$ gives $a=2$.

Thus, the coefficients are

$$
a=2,\qquad b=0,\qquad c=1.
$$

### 4. Write the polynomial

Substituting the coefficients into $p(x)=ax^2+bx+c$, we obtain

$$
p(x)=2x^2+1.
$$

Each coefficient was uniquely determined, so this is the unique polynomial of the stated form through the three points.

## Verification

At $x=0$,

$$
p(0)=2\cdot0^2+1=1,
$$

so the graph passes through $(0,1)$.

At $x=1$,

$$
p(1)=2\cdot1^2+1=3,
$$

so the graph passes through $(1,3)$.

At $x=2$,

$$
p(2)=2\cdot2^2+1=8+1=9,
$$

so the graph passes through $(2,9)$.

All three points satisfy the polynomial, confirming the result.
