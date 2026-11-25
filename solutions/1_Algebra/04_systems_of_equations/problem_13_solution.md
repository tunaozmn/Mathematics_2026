# Exercise 13. Does Every Equation Add New Information?

## Problem

Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

> **Why this exercise:** teaches how to recognize redundant equations within a system.

## Method

We compare the equations to see whether one can be obtained from the others.

An equation that follows from the remaining equations is redundant: removing it does not change the solution set. We solve the independent equations by choosing a free variable and expressing the other variables in terms of it.

## Solution

### 1. Identify the relation between the equations

Subtract the second equation from the first:

$$
\begin{aligned}
(x_1+x_2)-(x_2+x_3)&=10-8, \\
x_1-x_3&=2.
\end{aligned}
$$

This is exactly the third equation. Therefore, the third equation follows from the first two and adds no new restriction.

The first two equations are independent: neither is a scalar multiple of the other.

### 2. Confirm the redundancy using elimination

The augmented matrix, using the variable order $x_1,x_2,x_3$, is

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
1 & 0 & -1 & 2
\end{array}
\right].
$$

Apply

$$
R_3\leftarrow R_3-R_1.
$$

This gives

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & -1 & -1 & -8
\end{array}
\right].
$$

Next, apply

$$
R_3\leftarrow R_3+R_2.
$$

We obtain

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & 0 & 0 & 0
\end{array}
\right].
$$

The zero row represents $0=0$, confirming that the third equation supplies no additional information.

### 3. Find the parametric solution

There are pivots in the $x_1$ and $x_2$ columns, while $x_3$ is free. Let

$$
x_3=t,\qquad t\in\mathbb{R}.
$$

From the second equation,

$$
x_2=8-t.
$$

Using the first equation,

$$
\begin{aligned}
x_1
&=10-x_2 \\
&=10-(8-t) \\
&=2+t.
\end{aligned}
$$

Thus, all solutions are

$$
(x_1,x_2,x_3)=(2+t,8-t,t),
\qquad t\in\mathbb{R}.
$$

Equivalently,

$$
\begin{aligned}
\begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix}
&=
\begin{pmatrix}
2 \\
8 \\
0
\end{pmatrix}
+t
\begin{pmatrix}
1 \\
-1 \\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
\end{aligned}
$$

There is one free variable, so the system has infinitely many solutions.

### 4. State which equations are necessary

All three equations are not independently necessary. The first two alone describe the full solution set because their difference gives the third.

In fact, any two of the equations imply the remaining one:

- The first minus the second gives the third.
- The second plus the third gives the first.
- The first minus the third gives the second.

Thus, any pair is sufficient, but one equation alone is not.

## Verification

Substitute the parametric solution into all three original equations:

$$
\begin{aligned}
x_1+x_2
&=(2+t)+(8-t)=10, \\
x_2+x_3
&=(8-t)+t=8, \\
x_1-x_3
&=(2+t)-t=2.
\end{aligned}
$$

Every equation holds for every real $t$. This confirms both the solution family and the fact that the third equation places no further restriction on it.
