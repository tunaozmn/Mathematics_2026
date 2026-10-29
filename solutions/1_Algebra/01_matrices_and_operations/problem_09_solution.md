# Problem 9 — Composing Transformations

## Problem

Consider the matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},
\qquad
R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix},
$$

where $S$ represents a nonuniform scaling and $R$ represents a counterclockwise rotation through $90^\circ$.

For the vector

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix},
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of the transformations matters.

## Method

When a product of matrices acts on a column vector, the rightmost matrix acts first:

$$
RSx=R(Sx),
\qquad
SRx=S(Rx).
$$

The matrix $S$ doubles the horizontal coordinate and leaves the vertical coordinate unchanged:

$$
S
\begin{pmatrix}
u \\
v \\
\end{pmatrix}=
\begin{pmatrix}
2u \\
v \\
\end{pmatrix}.
$$

The matrix $R$ rotates a vector counterclockwise through $90^\circ$:

$$
R
\begin{pmatrix}
u \\
v \\
\end{pmatrix}=
\begin{pmatrix}
-v \\
u \\
\end{pmatrix}.
$$

## Solution

### 1. Scaling followed by rotation

To compute $RSx$, first apply $S$:

$$
Sx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot1+0\cdot2 \\
0\cdot1+1\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}.
$$

Then apply $R$:

$$
RSx=R(Sx)=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
0\cdot2-1\cdot2 \\
1\cdot2+0\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}.
$$

### 2. Rotation followed by scaling

To compute $SRx$, first apply $R$:

$$
Rx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
0\cdot1-1\cdot2 \\
1\cdot1+0\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}.
$$

Then apply $S$:

$$
SRx=S(Rx)=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot(-2)+0\cdot1 \\
0\cdot(-2)+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}.
$$

### 3. Comparison and geometric explanation

The results are different:

$$
RSx=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\neq
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}=SRx.
$$

When scaling is applied first, the vector changes from $(1,2)$ to $(2,2)$. The rotation then takes it to $(-2,2)$. The horizontal component that was doubled becomes the vertical component after rotation.

When rotation is applied first, the vector changes from $(1,2)$ to $(-2,1)$. Scaling then doubles its new horizontal coordinate, giving $(-4,1)$.

The scaling acts along the fixed horizontal axis. A rotation changes which component lies along that axis, so applying the scaling before or after the rotation produces different results.

Therefore, these transformations do not commute.

## Verification

Compute the two matrix products directly:

$$
RS=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix},
$$

$$
SR=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}.
$$

Applying these products to the original vector gives

$$
(RS)x=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix},
$$

$$
(SR)x=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}.
$$

These results agree with the step-by-step calculations.
