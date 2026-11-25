# Exercise 2. Gaussian Elimination — One Solution

## Problem

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.

## Method

We write the system as an augmented matrix and use elementary row operations to create zeros below the pivots.

These operations preserve the solution set. Once the system is in upper triangular form, we use back substitution: first find $z$, then $y$, and finally $x$.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y,z$, the augmented matrix is

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2
\end{array}
\right].
$$

### 2. Eliminate x from the second and third rows

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
\begin{aligned}
&(2-2,\;-1-2,\;1-2,\;3-12) \\
&\qquad=(0,-3,-1,-9).
\end{aligned}
$$

Next, apply

$$
R_3\leftarrow R_3-R_1.
$$

The new third row is

$$
\begin{aligned}
&(1-1,\;2-1,\;-1-1,\;2-6) \\
&\qquad=(0,1,-2,-4).
\end{aligned}
$$

Thus, the augmented matrix becomes

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4
\end{array}
\right].
$$

### 3. Choose a convenient second pivot

Interchange the second and third rows:

$$
R_2\leftrightarrow R_3.
$$

This gives

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9
\end{array}
\right].
$$

The second pivot is now 1, which makes the next elimination step straightforward. Interchanging equations does not change the solution set.

### 4. Eliminate y from the third row

Apply

$$
R_3\leftarrow R_3+3R_2.
$$

The new third row is

$$
\begin{aligned}
&(0+3\cdot0,\;-3+3\cdot1,\;-1+3(-2),\;-9+3(-4)) \\
&\qquad=(0,0,-7,-21).
\end{aligned}
$$

We obtain the upper triangular system

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21
\end{array}
\right].
$$

Equivalently,

$$
\begin{cases}
x+y+z=6, \\
y-2z=-4, \\
-7z=-21.
\end{cases}
$$

### 5. Use back substitution

From the third equation,

$$
z=\frac{-21}{-7}=3.
$$

Substitute $z=3$ into the second equation:

$$
\begin{aligned}
y-2\cdot3&=-4, \\
y&=2.
\end{aligned}
$$

Finally, substitute $y=2$ and $z=3$ into the first equation:

$$
\begin{aligned}
x+2+3&=6, \\
x&=1.
\end{aligned}
$$

Therefore, the solution is

$$
(x,y,z)=(1,2,3).
$$

There is a nonzero pivot for every variable, so no variable is free. Back substitution determines all three variables uniquely.

## Verification

Substitute $(x,y,z)=(1,2,3)$ into each original equation.

First equation:

$$
x+y+z=1+2+3=6.
$$

Second equation:

$$
2x-y+z=2\cdot1-2+3=3.
$$

Third equation:

$$
x+2y-z=1+2\cdot2-3=2.
$$

All three equations are satisfied. Hence, the system is consistent, and its unique solution is $(1,2,3)$.
