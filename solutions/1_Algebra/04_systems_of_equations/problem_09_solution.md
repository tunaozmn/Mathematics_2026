# Exercise 9. A System from a Sum Condition

## Problem

Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.

## Method

We use elimination to remove $x$ from the second equation, then substitute back to find $x$.

For the geometric interpretation, each equation describes a line in the plane. Two lines with different slopes intersect at exactly one point, giving a unique solution.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y$, the system becomes

$$
\left[
\begin{array}{cc|c}
1 & 1 & 10 \\
2 & 5 & 32
\end{array}
\right].
$$

### 2. Eliminate x from the second row

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
\begin{aligned}
&(2-2\cdot1,\;5-2\cdot1,\;32-2\cdot10) \\
&\qquad=(0,3,12).
\end{aligned}
$$

Thus, the augmented matrix becomes

$$
\left[
\begin{array}{cc|c}
1 & 1 & 10 \\
0 & 3 & 12
\end{array}
\right].
$$

The second row gives

$$
3y=12,\qquad y=4.
$$

### 3. Find x by back substitution

Substitute $y=4$ into the first equation:

$$
\begin{aligned}
x+4&=10, \\
x&=6.
\end{aligned}
$$

Therefore, the solution is

$$
(x,y)=(6,4).
$$

### 4. Explain geometrically why the solution is unique

Rewrite each original equation in slope-intercept form.

The first equation gives

$$
y=10-x,
$$

so its slope is $-1$.

The second equation gives

$$
y=\frac{32}{5}-\frac25 x,
$$

so its slope is $-\frac25$.

The slopes are different, so the two lines are not parallel and intersect at exactly one point. That intersection is $(6,4)$.

A solution must lie on both lines, so this single intersection explains why the solution is unique.

## Verification

Substitute $x=6$ and $y=4$ into both original conditions:

$$
x+y=6+4=10,
$$

and

$$
2x+5y=2\cdot6+5\cdot4=12+20=32.
$$

Both conditions are satisfied, confirming that the required numbers are $x=6$ and $y=4$.
