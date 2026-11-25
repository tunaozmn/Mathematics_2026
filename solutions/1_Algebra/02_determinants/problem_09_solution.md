# Exercise 9. Area and the Determinant

## Problem

The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

## Method

For two vectors in the plane, the area of their parallelogram is the absolute value of the determinant of the matrix having those vectors as its columns:

$$
\text{Area}=\left|\det[u\ v]\right|.
$$

For a $2\times2$ matrix, we calculate the determinant using

$$
\det
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
=ad-bc.
$$

Reversing the order of the vectors exchanges the two columns. This changes the sign of the determinant but preserves its absolute value.

## Solution

### 1. Place the vectors in the columns of a matrix

With $u$ as the first column and $v$ as the second,

$$
[u\ v]=
\begin{pmatrix}
3 & 1 \\
1 & 4
\end{pmatrix}.
$$

Its determinant is

$$
\begin{aligned}
\det[u\ v]
&=3\cdot4-1\cdot1\\
&=12-1\\
&=11.
\end{aligned}
$$

### 2. Calculate the area

The area is the absolute value of this determinant:

$$
\text{Area}=|11|=11.
$$

Therefore, the parallelogram has an area of $11$ square units.

### 3. Reverse the order of the vectors

Putting $v$ first and $u$ second gives

$$
[v\ u]=
\begin{pmatrix}
1 & 3 \\
4 & 1
\end{pmatrix}.
$$

Now the determinant is

$$
\begin{aligned}
\det[v\ u]
&=1\cdot1-3\cdot4\\
&=1-12\\
&=-11.
\end{aligned}
$$

This agrees with the column-swap property:

$$
\det[v\ u]=-\det[u\ v].
$$

### 4. Explain the geometric effect

The sign of the determinant describes the orientation of the ordered pair of vectors. Reversing their order reverses that orientation, so the determinant changes from $11$ to $-11$.

However, the vectors still form the same parallelogram. Its area remains

$$
|-11|=11.
$$

Thus, the determinant changes sign, but the area does not change.

## Verification

We can check the area using base times height.

Taking $u$ as the base, its length is

$$
\|u\|=\sqrt{3^2+1^2}=\sqrt{10}.
$$

The line through the origin in the direction of $u$ has equation

$$
x-3y=0.
$$

The perpendicular distance from the endpoint of $v$, which is $(1,4)$, to this line is the height of the parallelogram:

$$
h=\frac{|1-3\cdot4|}{\sqrt{1^2+(-3)^2}}
=\frac{11}{\sqrt{10}}.
$$

Therefore,

$$
\text{Area}=\|u\|h
=\sqrt{10}\cdot\frac{11}{\sqrt{10}}
=11.
$$

This agrees with the determinant calculation.
