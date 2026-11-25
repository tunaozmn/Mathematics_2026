# Exercise 2. A Line in Space

## Problem

Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
$$

State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

> **Why this exercise:** reinforces the interpretation of parametric form as “point + direction.”

## Method

A parametric line has the form

$$
(x,y,z)=A+tv,\qquad t\in\mathbb{R},
$$

where $A$ is a point on the line and $v$ is a nonzero direction vector.

To check whether a point lies on the line, we must find one value of $t$ that satisfies all three coordinate equations simultaneously.

## Solution

### 1. Identify a point and the direction vector

From the given equation, a point on the line is

$$
A=(2,-1,3),
$$

corresponding to $t=0$.

A direction vector is

$$
v=(1,2,-2).
$$

Increasing $t$ by 1 changes the coordinates by $1$, $2$, and $-2$, respectively.

### 2. Write the coordinate equations

The parametric equation is equivalent to

$$
\begin{cases}
x=2+t, \\
y=-1+2t, \\
z=3-2t.
\end{cases}
$$

### 3. Check whether P lies on the line

For $P=(4,3,-1)$, the first coordinate requires

$$
2+t=4,
$$

so $t=2$.

Check the other two coordinates using this same value:

$$
-1+2\cdot2=3,
$$

$$
3-2\cdot2=-1.
$$

All three coordinates agree with $P$. Therefore,

$$
P\in L.
$$

The corresponding parameter value is $t=2$.

### 4. Find the point corresponding to t = -1

Substitute $t=-1$ into the line equation:

$$
\begin{aligned}
Q
&=(2,-1,3)+(-1)(1,2,-2) \\
&=(2-1,\;-1-2,\;3+2) \\
&=(1,-3,5).
\end{aligned}
$$

Thus, the required point is

$$
Q=(1,-3,5).
$$

Geometrically, a negative parameter moves from $A$ in the direction opposite to $v$. Here, $t=-1$ gives a displacement of exactly $-v$.

## Verification

The displacement from $A$ to $P$ is

$$
\begin{aligned}
P-A
&=(4-2,\;3-(-1),\;-1-3) \\
&=(2,4,-4) \\
&=2(1,2,-2) \\
&=2v.
\end{aligned}
$$

This confirms that $P$ is on the line at $t=2$.

Similarly,

$$
\begin{aligned}
Q-A
&=(1-2,\;-3-(-1),\;5-3) \\
&=(-1,-2,2) \\
&=-v.
\end{aligned}
$$

This confirms that $Q=(1,-3,5)$ corresponds to $t=-1$.
