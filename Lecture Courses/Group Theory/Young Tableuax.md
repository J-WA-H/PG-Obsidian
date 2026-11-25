Young tableaux are useful for dealing with irreducible representations of [[Lie Groups]].

The observation is that the $\mathbf{\bar{3}}$ representation is an antisymmetric combination of two 3s, so we do not need the second fundamental representation to construct higher dimensions. We can write an arbitrary representation as a tensor product of 3s with an appropriate symmetry. In fact, Young tableaux correspond to irreducible representations of the permutation group and the connection with the irreducible representations of $SU(3)$ is that they transform irreducibly under permutation of the labels of the indices. 

Consider a general representation, $(n,m)$. It is a tensor with components$$\tag{3.1} A^{i_{1}\dots i_{n}}_{j_{1}\dots j_{m}}$$separately symmetric in upper and lower indices, and traceless. We can raise all lower indices with $\varepsilon$ tensors to get
$$a^{i_{1}\dots i_{n}k_{1}\ell_{1}\dots k_{m}\ell_{m}}= \varepsilon^{j_{1}k_{1}\ell_{1}}\dots \varepsilon^{j_{m}k_{m}\ell_{m}}A^{i_{1}\dots i_{n}}_{j_{1}\dots j_{m}} \tag{3.2}.$$
This shows that it is antisymmetric in each pair $k_{i}\leftrightarrow \ell_{i}$ and symmetric in the exchange of pairs $k_{i},\ell_{i}\leftrightarrow k_{j},\ell_{j}$.

For each such tensor, we can associate a Young tableau:

| $k_{1}$    | $\dots$ | $k_{m}$    | $i_{1}$ | $\dots$ | $i_{n}$ |
| ---------- | ------- | ---------- | ------- | ------- | ------- |
| $\ell_{1}$ | $\dots$ | $\ell_{m}$ |         |         |         |
The aim is to find a rule that associates with the Young tableau the specific symmetry of the tensor. The final result is that rows represent symmetries, i.e. how the $i$s are symmetric, and columns show antisymmetries, i.e. how $k_{i}\leftrightarrow \ell_{i}$ is antisymmetric. The traceless condition also becomes
$$\varepsilon_{i_{1}k_{1}\ell_{1}}a^{i_{1}\dots i_{n}k_{1}\ell_{1}\dots k_{m}\ell_{m}}=0\tag{3.3}.$$
Thus the Yong tableau is a rule for symmetrising a tensor to project out a specific irreducible representation. For example, if $a^{j_{1}j_{2}k_{1}}$ is a general tensor with three upper indices, but no special symmetry property, the Young diagram
![[Pasted image 20261019154523.png|171]]
produces the tensor
$$a^{j_{1}j_{2}k_{1}}+a^{j_{2}j_{1}k_{1}}-a^{k_{1}j_{2}j_{1}}-a^{j_{2}k_{1}j_{1}}\tag{3.4},$$
which transforms under the $(1,1)$ (or adjoint) representation.

This works when forming the Young tableau for any tensor - symmetrise with rows, antisymmetrise with columns.
For example, in $SU(3)$, the tensors corresponding to the Young tableaux with more than three boxes in any column vanish because no tensor can be completely antisymmetric in four or more indices which take on only three values. Any column with three boxes correspond to a factor of $\varepsilon$ in the three indices
![[Pasted image 20261019160228.png]]

To decompose the tensor product of irreducible representations $\alpha,\beta$ corresponding to tableaux $A,B$, you build onto $A$ using the boxes of $B$ in the following way: Begin by putting $a$s in the top row of $B$ and $b$s in the second row. Take the boxes from the top row of $B$ and put them on $A$, building to the right and/or down, to form legal tableau (that is collections of boxes in which numbers of boxes in the columns are not increasing as you go down, and the number of boxes in the columns are not increasing as you go right), with no two $a$s in the same column. Then take the second row and add the boxes to each of the resulting tableau to form legal tableaux with one further condition. Reading along the rows from right to left from the top row down to the bottom row, the number of $a$s must be greater than or equal to the number of $b$s. This avoids double counting. The tableaux produced by this construction corresponds to the irreducible representations in $\alpha \otimes\beta$.