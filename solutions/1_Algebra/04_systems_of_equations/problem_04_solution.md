# Exercise 4. Infinitely Many Solutions

## Problem

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.

## Method

We use Gaussian elimination to identify the independent equations and the pivot variables.

A zero row with a zero right-hand side imposes no additional restriction. If the system is consistent and a variable has no pivot, we may choose that variable freely and express the remaining variables in terms of it.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y,z$, we obtain

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
2 & 2 & 2 & 4 \\
1 & -1 & 1 & 0
\end{array}
\right].
$$

### 2. Eliminate x from the second and third rows

Apply

$$
R_2\leftarrow R_2-2R_1,
\qquad
R_3\leftarrow R_3-R_1.
$$

The second row becomes zero because the second original equation is twice the first. The third row becomes $(0,-2,0,-2)$.

Thus, the augmented matrix is

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & -2 & 0 & -2
\end{array}
\right].
$$

Interchange the second and third rows:

$$
R_2\leftrightarrow R_3.
$$

This gives the row echelon form

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & -2 & 0 & -2 \\
0 & 0 & 0 & 0
\end{array}
\right].
$$

### 3. Identify the free variable

The nonzero rows represent

$$
\begin{cases}
x+y+z=2, \\
-2y=-2.
\end{cases}
$$

The last row represents $0=0$, so it introduces no contradiction or additional restriction.

There are pivots in the $x$ and $y$ columns, but no pivot in the $z$ column. Therefore, $z$ is a free variable.

From the second equation,

$$
y=1.
$$

Substituting into the first equation gives

$$
x+z=1.
$$

### 4. Write the parametric solution

Let

$$
z=t,\qquad t\in\mathbb{R}.
$$

Then

$$
x=1-t,\qquad y=1.
$$

Hence, all solutions are

$$
(x,y,z)=(1-t,1,t),
\qquad t\in\mathbb{R}.
$$

Equivalently, in vector form,

$$
\begin{aligned}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
&=
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix}
+t
\begin{pmatrix}
-1 \\
0 \\
1
\end{pmatrix}.
\end{aligned}
$$

Every real value of $t$ gives a different solution, so the system has infinitely many solutions.

## Verification

Choose $t=2$. The corresponding point is

$$
(x,y,z)=(-1,1,2).
$$

Substitute into all three original equations:

$$
\begin{aligned}
x+y+z&=-1+1+2=2, \\
2x+2y+2z&=2(-1)+2(1)+2(2)=4, \\
x-y+z&=-1-1+2=0.
\end{aligned}
$$

Thus, the chosen point satisfies the system.

We can also check the entire family by substituting $(1-t,1,t)$:

$$
\begin{aligned}
(1-t)+1+t&=2, \\
2(1-t)+2+2t&=4, \\
(1-t)-1+t&=0.
\end{aligned}
$$

All three identities hold for every real $t$, confirming the parametric solution.
