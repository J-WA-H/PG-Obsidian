A group $G$ is a set with a rule for assigning to every (ordered) pair of elements a third element satisfying:
- If $f,g \in G$ then $h=fg\in G$
- If $f,g,h\in G$ then $f(gh)=(fg)h$
- There is an identity element $e$ s.t. $\forall \;f\in G,\; ef=fe=f$
- Every element $f\in G$ has an inverse $f^{-1}$ s.t. $ff^{-1}=f^{-1}f=e$

Thus, a group is a multiplication table specifying $g_{1}g_{2}\;\forall\; g_{1},g_{2}\in G$. If the group elements are discrete, the multiplication table is of the form

| \        | $e$      | $g_1$        | $g_{2}$      | $\dots$  |
| -------- | -------- | ------------ | ------------ | -------- |
| $e$      | $e$      | $g_{1}$      | $g_{2}$      | $\dots$  |
| $g_{1}$  | $g_{1}$  | $g_{1}g_{1}$ | $g_{1}g_{2}$ | $\dots$  |
| $g_{2}$  | $g_{2}$  | $g_{2}g_{1}$ | $g_{2}g_{2}$ | $\dots$  |
| $\vdots$ | $\vdots$ | $\vdots$     | $\vdots$     | $\ddots$ |
A representation of $G$ is a mapping, $D$, of elements of $G$ onto a set of linear operators with the properties:
- $D(e)=\mathbb{1}$, where $\mathbb{1}$ is the identity operator in the space on which the linear operators act.
- $D(g_{1})D(g_{2})=D(g_{1}g_{2})$, in other words the group multiplication law is mapped onto the natural multiplication in the linear space on which the linear operators act.

Example $\mathbb{Z}_{3}$, the cyclic group of order 3

| \   | $e$ | $a$ | $b$ |
| --- | --- | --- | --- |
| $e$ | $e$ | $a$ | $b$ |
| $a$ | $a$ | $b$ | $e$ |
| $b$ | $b$ | $e$ | $a$ |
This group is abelian as the order of the elements in the operation don't matter.

One representation of the group is $D(e)=1,\;D(a)=e^{ 2\pi i/3 },\;D(b)=e^{ 4\pi i/3 }$. This is irreducible so $\mathbb{Z}_{3}$ is given by a $\mathbf{1}$-representation.

The dimension of a representation is the dimension of the space on which it acts, so this representation of $\mathbb{Z}_{3}$ is 1-dimensional.

Another representation of $\mathbb{Z}_{3}$ is the regular representation.
$$D(e)=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix},\; D(a)=\begin{bmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 0
\end{bmatrix},\; D(b)=\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
1 & 0 & 0
\end{bmatrix}.\tag{1.1}$$
This was derived in the orthonormal basis $\{ \ket{e},\ket{a},\ket{b} \}$ and $D(g_{1})D(g_{2})=\ket{g_{1}g_{1}}$, with matrix elements $D_{ij}=\bra{e_{i}}D(g)\ket{e_{j}}$. The construction of the regular representation is completely general for any finite group.

As representations live in linear spaces, a linear transformation can be applied to make them into a more convenient form. If the transformation is invertable, the new states are just as good as the old states. Such a transformation is called a similarity transformation
$$D(g)\to D'(g)=S^{-1}D(g)S\tag{1.2}.$$
$D$ and $D'$ are said to be equivalent representations because they differ by the choice of basis.

A representation is reducible if it has an invariant subspace, which means that the action of any $D(g)$ on any vector in the subspace is still in the subspace. In terms of a projection operator, $P$ onto the subspace this condition can be written as
$$PD(g)P=D(g)P \qquad \forall \;g\in G.\tag{1.3}$$
E.g for the regular representation of $\mathbb{Z}_{3}$, the invariant subspace is projected by
$$P=\frac{1}{3}\begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix},\tag{1.4}$$
because $D(g)P=P\; \forall\;g$. This restriction of the representation to the invariant subspace is itself a representation. In this case, it is the trivial representation for which $D(g)=\mathbb{1}$.

A representation is irreducible if it is not reducible. A representation is completely reducible if it is equivalent to a representation whose matrix elements have the form
$$\begin{bmatrix}
D_{1}(g) & 0 & \dots \\
0 & D_{2}(g) & \dots \\
\vdots & \vdots & \ddots
\end{bmatrix}\tag{1.5},$$
where $D_{j}(g)$ is irreducible $\forall\;j$. This is block diagonal form.

A representation in block diagonal form is said to be the direct sum of subrepresentations $D_{j}(g)$,
$$D_{1}\oplus D_{2}\oplus \dots \tag{1.6}$$
In transforming a representation to block diagonal form, we are decomposing the original representation into a direct sum of its irreducible components. Thus another way of defining reducibility is **a completely reducible representation can be decomposed into a direct sum of irreducible representations**.

Any representation of a finite group is reducible, for example, for $(1.1)$, take
$$S=\frac{1}{3}\begin{bmatrix}
1 & 1 & 1 \\
1 & \omega^2 & \omega \\
1 & \omega & \omega^2
\end{bmatrix}\tag{1.7}$$
where $\omega=e^{ 2\pi i/3 }$. Then
$$D'(e)=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix},\; D'(a)=\begin{bmatrix}
1 & 0 & 0 \\
0 & \omega & 0 \\
0 & 0 & \omega^2
\end{bmatrix},\;D'(b)=\begin{bmatrix}
1 & 0 & 0 \\
0 & \omega^2 & 0 \\
0 & 0 & \omega
\end{bmatrix}.\tag{1.8}$$
