# Exercise 8. Two Systems with the Same Coefficient Matrix

## Problem

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.

## Method

Both systems have the same coefficient matrix,

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & -1
\end{pmatrix},
$$

but different right-hand sides.

We use the same row operations on both augmented matrices: interchange the rows to obtain a first pivot equal to 1, then eliminate the entry below it. Finally, use back substitution.

## Solution

### 1. Solve the first system

The augmented matrix is

$$
\left[
\begin{array}{cc|c}
2 & 1 & 5 \\
1 & -1 & 1
\end{array}
\right].
$$

Interchange the rows:

$$
R_1\leftrightarrow R_2.
$$

This gives

$$
\left[
\begin{array}{cc|c}
1 & -1 & 1 \\
2 & 1 & 5
\end{array}
\right].
$$

Now eliminate the first entry of the second row:

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
\begin{aligned}
&(2-2\cdot1,\;1-2(-1),\;5-2\cdot1) \\
&\qquad=(0,3,3).
\end{aligned}
$$

Therefore,

$$
\left[
\begin{array}{cc|c}
1 & -1 & 1 \\
0 & 3 & 3
\end{array}
\right].
$$

The second equation gives

$$
3y=3,\qquad y=1.
$$

Substituting into the first equation,

$$
x-y=1,\qquad x=1+1=2.
$$

Thus, the first system has the unique solution

$$
(x,y)=(2,1).
$$

### 2. Solve the second system

The augmented matrix is

$$
\left[
\begin{array}{cc|c}
2 & 1 & 1 \\
1 & -1 & 4
\end{array}
\right].
$$

Apply the same row interchange:

$$
R_1\leftrightarrow R_2.
$$

We obtain

$$
\left[
\begin{array}{cc|c}
1 & -1 & 4 \\
2 & 1 & 1
\end{array}
\right].
$$

Next, apply the same elimination operation:

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
\begin{aligned}
&(2-2\cdot1,\;1-2(-1),\;1-2\cdot4) \\
&\qquad=(0,3,-7).
\end{aligned}
$$

Therefore,

$$
\left[
\begin{array}{cc|c}
1 & -1 & 4 \\
0 & 3 & -7
\end{array}
\right].
$$

The second equation gives

$$
3y=-7,\qquad y=-\frac73.
$$

Substitute into the first equation:

$$
\begin{aligned}
x-y&=4, \\
x&=4+y \\
&=4-\frac73 \\
&=\frac53.
\end{aligned}
$$

Thus, the second system has the unique solution

$$
(x,y)=\left(\frac53,-\frac73\right).
$$

### 3. Compare the elimination steps

Both systems used exactly the same operations:

$$
R_1\leftrightarrow R_2,
\qquad
R_2\leftarrow R_2-2R_1.
$$

The coefficient matrix changed in the same way in both cases, producing

$$
\begin{pmatrix}
1 & -1 \\
0 & 3
\end{pmatrix}.
$$

The pivots and the elimination multiplier were identical because they were determined by the same original coefficients.

Only the right-hand side calculations differed:

| Stage | First system | Second system |
| --- | --- | --- |
| Original right-hand side | $(5,1)^T$ | $(1,4)^T$ |
| After interchanging rows | $(1,5)^T$ | $(4,1)^T$ |
| After elimination | $(1,3)^T$ | $(4,-7)^T$ |

Thus, the coefficient elimination is reusable. The same operations must be applied to each right-hand side, after which back substitution gives the corresponding solution.

Both systems have two nonzero pivots, so each has exactly one solution.

## Verification

For the first solution, $(x,y)=(2,1)$:

$$
\begin{aligned}
2x+y&=2\cdot2+1=5, \\
x-y&=2-1=1.
\end{aligned}
$$

For the second solution, $(x,y)=\left(\frac53,-\frac73\right)$:

$$
\begin{aligned}
2x+y
&=2\cdot\frac53-\frac73 \\
&=\frac{10-7}{3}=1, \\
x-y
&=\frac53-\left(-\frac73\right) \\
&=\frac{12}{3}=4.
\end{aligned}
$$

Each solution satisfies its own original system.
