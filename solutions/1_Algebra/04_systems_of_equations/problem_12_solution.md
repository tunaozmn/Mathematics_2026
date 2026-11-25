# Exercise 12. Homogeneous System

## Problem

Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

> **Why this exercise:** shows the special case of a system with a zero right-hand side without introducing additional theory.

## Method

A homogeneous linear system has zero on the right-hand side of every equation.

We use Gaussian elimination to identify the pivot variables and any free variables. Then we express all solutions in terms of the free variables.

The zero vector always satisfies a homogeneous system because substituting zero for every unknown makes every left-hand side zero.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y,z$, we obtain

$$
\left[
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
2 & 4 & -2 & 0 \\
1 & -1 & 2 & 0
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

The second row becomes zero because the second equation is twice the first. The third row becomes $(0,-3,3,0)$.

Therefore,

$$
\left[
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & 0 & 0 & 0 \\
0 & -3 & 3 & 0
\end{array}
\right].
$$

Interchange the second and third rows:

$$
R_2\leftrightarrow R_3.
$$

The resulting row echelon form is

$$
\left[
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
0 & -3 & 3 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right].
$$

### 3. Identify the free variable and substitute back

The nonzero rows represent

$$
\begin{cases}
x+2y-z=0, \\
-3y+3z=0.
\end{cases}
$$

There are pivots in the $x$ and $y$ columns, but no pivot in the $z$ column. Therefore, $z$ is free.

The second equation gives

$$
y=z.
$$

Substitute this into the first equation:

$$
\begin{aligned}
x+2z-z&=0, \\
x&=-z.
\end{aligned}
$$

### 4. Write all solutions in parametric form

Let

$$
z=t,\qquad t\in\mathbb{R}.
$$

Then

$$
x=-t,\qquad y=t.
$$

Thus, all solutions are

$$
(x,y,z)=(-t,t,t),
\qquad t\in\mathbb{R}.
$$

Equivalently,

$$
\begin{aligned}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
&=
t\begin{pmatrix}
-1 \\
1 \\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
\end{aligned}
$$

There is one free variable and no contradiction, so the system has infinitely many solutions.

### 5. Explain the zero solution

Taking $t=0$ gives

$$
(x,y,z)=(0,0,0).
$$

More generally, every homogeneous linear system has the form

$$
A\mathbf{x}=\mathbf{0}.
$$

Setting $\mathbf{x}=\mathbf{0}$ gives

$$
A\mathbf{0}=\mathbf{0}.
$$

Therefore, the zero vector always satisfies a homogeneous system. Such a system cannot have no solution, although it may have either only the zero solution or infinitely many solutions.

## Verification

Substitute $(x,y,z)=(-t,t,t)$ into every original equation:

$$
\begin{aligned}
x+2y-z
&=-t+2t-t=0, \\
2x+4y-2z
&=-2t+4t-2t=0, \\
x-y+2z
&=-t-t+2t=0.
\end{aligned}
$$

All three equations hold for every real $t$, confirming the full parametric solution.
