# Exercise 8. Inverse of a Transformation

## Problem

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

> **Why this exercise:** gives the inverse the interpretation of undoing a transformation.

## Method

A diagonal matrix scales each coordinate by its corresponding diagonal entry.

If all diagonal entries are nonzero, we undo the scaling by multiplying each coordinate by the reciprocal of its original scale factor. The inverse is therefore diagonal, with reciprocal entries.

We will identify the action of $S$, construct the transformation that reverses it, and check that applying both transformations recovers the original vector.

## Solution

### 1. Describe the action of S

For a general vector,

$$
\begin{aligned}
S\begin{pmatrix}
x \\
y
\end{pmatrix}
&=
\begin{pmatrix}
2x \\
\frac12 y
\end{pmatrix}.
\end{aligned}
$$

Thus, $S$ doubles the horizontal coordinate and halves the vertical coordinate.

Geometrically, it stretches the plane horizontally by a factor of $2$ and compresses it vertically by a factor of $\frac12$.

### 2. Find the inverse transformation

To undo the horizontal scaling, we multiply the first coordinate by $\frac12$.

To undo the vertical scaling, we multiply the second coordinate by $2$.

Therefore,

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0\\
0 & 2
\end{pmatrix}.
$$

Both original scale factors are nonzero, so both changes can be reversed.

### 3. Explain the geometry of the inverse

The inverse acts as

$$
\begin{aligned}
S^{-1}\begin{pmatrix}
x \\
y
\end{pmatrix}
&=
\begin{pmatrix}
\frac12 x \\
2y
\end{pmatrix}.
\end{aligned}
$$

It compresses the plane horizontally by a factor of $\frac12$ and stretches it vertically by a factor of $2$.

When applied after $S$, these reciprocal scalings restore both coordinates to their original values.

## Verification

Take the vector

$$
v=
\begin{pmatrix}
1\\
2
\end{pmatrix}.
$$

First, apply $S$:

$$
\begin{aligned}
Sv
&=
\begin{pmatrix}
2\cdot1\\
\frac12\cdot2
\end{pmatrix}\\
&=
\begin{pmatrix}
2\\
1
\end{pmatrix}.
\end{aligned}
$$

Next, apply $S^{-1}$ to the result:

$$
\begin{aligned}
S^{-1}(Sv)
&=
\begin{pmatrix}
\frac12\cdot2\\
2\cdot1
\end{pmatrix}\\
&=
\begin{pmatrix}
1\\
2
\end{pmatrix}\\
&=v.
\end{aligned}
$$

The original vector is recovered.

We can also confirm the inverse relationship for every vector by multiplying the matrices:

$$
S^{-1}S=
\begin{pmatrix}
\frac12\cdot2 & 0\\
0 & 2\cdot\frac12
\end{pmatrix}
=I.
$$

The reverse product $SS^{-1}$ is also $I$, since the same reciprocal scale factors multiply to $1$ in each coordinate.
