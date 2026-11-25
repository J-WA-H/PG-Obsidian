The harmonic oscillator or [[Free Particles]] are exceptional cases which are exactly solvable, but for most physically interesting systems this is not the case and we need to study our problems as small perturbations of a problem we know how to solve.

Suppose our system has as its Lagrangian
$$L=L_{0}-V\tag{6.1}$$
where $L_{0}$ is the Lagrangian of an exactly solvable model and $V$ is some small perturbation. Then we can write
$$Z[J]=\mathcal{N}\int \mathcal{D}q\exp\left[ \frac{i}{\hbar}S_{0}[q]+\int dtJ(t)q(t)-\frac{i}{\hbar}\int dt\,V(q(t)) \right]=\exp\left[ -\frac{i}{\hbar}\int dtV\left( \frac{\delta}{\delta J(t)} \right) \right]\mathcal{N}\int \mathcal{D}q\exp\left[ \frac{i}{\hbar}S_{0}[q]+\int dtJ(t)q(t) \right]\\ = \frac{\mathcal{N}}{\mathcal{N}_{0}}\exp\left[ -\frac{i}{\hbar}dt V\left( \frac{\delta}{\delta J(t)} \right) \right]Z_{0}[J]\tag{6.2}$$
where $S_{0}=\int dt\,L_{0}$ is the action of the unperturbed Lagrangian and $Z_{0}$ is the [[Generating Functional]] of the unperturbed Lagrangian. Note that in deriving the above equation for $Z[J]$ we made use of the fact that a functional derivative with respect to $J(t)$ amounts to an insertion of $q(t)$ since the functional derivative with respect to $J(t)$ is independent of $q$ we can move it outside the path integral. The same applies for the function $V(q(t))$. The exponential of $V$ can now be expressed to the desired order in the small parameter that $V$ depends on. Knowing that the generating functional of the unperturbed system $Z_{0}[J]$ we can then use the expansion of $(6.2)$ in the small parameter to obtain $Z[J]$ to any desired order in said parameter.

For example, use the harmonic oscillator with a $q^3$ potential. The Lagrangian is
$$L=\underbrace{\frac{m}{2}\dot{q}^2 - \frac{m\omega^2}{2}q^2}_{L_{0}} - \underbrace{\frac{\lambda}{3!}q^3}_{V(q)}\tag{6.3}$$
where $\lambda$ is a small parameter. We can now write the generating functional as
$$Z[J]=\frac{\mathcal{N}}{\mathcal{N}_{0}}\exp\left[ -\frac{i}{\hbar} \frac{\lambda}{3!}\int dt \left( \frac{\delta}{\delta J(t)} \right)^3 \right]\overbrace{\exp\left[ \frac{1}{2}\int_{-\infty}^{\infty}dt_{1}dt_{2}J(t_{1})G_{0}(t_{1},t_{2})J(t_{2}) \right]}^{Z_{0}[J]}=\frac{\mathcal{N}}{\mathcal{N}_{0}}\left( 1-\frac{i}{\hbar} \frac{\lambda}{3!} \int dt \left( \frac{\delta}{\delta J(t)} \right)^{3}+\mathcal{O}(\lambda^2) \right)Z_{0}[J]\tag{6.4}.$$
Here $G_{0}(t_{1},t_{2})$ obeys $(5.11)$. The subscript $0$ will distinguish this from the two-point Green function for the full cubic system. To simplify the expressions define
$$G_{0t_{1}t_{2}}\equiv G_{0}(t_{1},t_{2}),\quad J\cdot G_{0}\equiv \int dt_{1}dt_{2}J(t_{1})G_{0}(t_{1},t_{2})J(t_{2}), \\ J_{i}\equiv J_{t_{i}}\equiv J(t_{i}) , \quad (J\cdot G_{0})_{t}\equiv \int dt_{1}dt_{2}J(t_{1})G(t_{1},t).\tag{6.5}$$
We can evaluate the functional derivatives to obtain the generating functional to order $\lambda$,
$$\left( \frac{\delta}{\delta J(t)} \right)^{3}\exp\left[ \frac{1}{2}J\cdot G_{0}\cdot J \right]=\left( \frac{\delta}{\delta J(t)} \right)^{2}\left( (G_{0}\cdot J)_{t}\exp\left[ \frac{1}{2}J\cdot G_{0}\cdot J \right] \right)\\=\left( \frac{\delta}{\delta J(t)} \right)(G_{0tt}+(G_{0}\cdot J)^2_{t}) \exp\left[ \frac{1}{2}J\cdot G_{0}\cdot J \right]=(3G_{0tt}(G_{0}\cdot J)_{t}+(G_{0}\cdot J)_{t}^{3})\exp\left[ \frac{1}{2}J\cdot G_{0}\cdot J \right]\tag{6.6}$$
so we get
$$Z[J]=\frac{\mathcal{N}}{\mathcal{N}_{0}}\left( 1-\frac{i\lambda}{\hbar}\left( \frac{1}{2}\int dtG_{0tt}(G_{0}\cdot J)_{t}+\int dt \frac{1}{3!}(G_{0}\cdot J)^{3}_{t}\right)+\mathcal{O}(\lambda^{2}) \right)\exp\left[ \frac{1}{2}J\cdot G_{0}\cdot J \right]\tag{6.7}.$$
We can fix the normalisation by demanding that $Z[0]=\braket{ 0 | 0 }=1$, where as usual we assume the ground state is normalisable. We get
$$Z[0]=\frac{\mathcal{N}}{\mathcal{N}_{0}}(1+\mathcal{O}(\lambda^2)), \iff \frac{\mathcal{N}}{\mathcal{N}_{0}}= \frac{1}{1+\mathcal{O}(\lambda^2)}\tag{6.8}.$$
Now we have $Z[J]$ we can compute various Green functions by taking functional derivatives.

These can lead to Feynman diagrams. The Feynman rules are 
![[Pasted image 20261109163654.png|411]]

The time integral refers to a time integration on the lines coming out of a node.

These rules are theory dependent, we have drawn a cubic vertex because the perturbing potential was cubic, justified by the $\left( \frac{\delta}{\delta J(t)} \right)^{3}$. There are three functional derivatives acting on the unperturbed generating functional so there will be three arguments of unperturbed two-point functions $G_{0}$ that will have $t$ so we must have three legs labelled by $t$ coming out of the interaction vertex. If we had a potential with a different power we would have a different number of legs. 

For the generating functional we have obtained,
![[Pasted image 20261109164149.png|307]]


where we kept the normalisation to remember we only know it up to order $\lambda^2$. The factor of $\frac{1}{2}$ in the first diagram, $\frac{1}{3!}$ in the second and $\frac{1}{2}$ in the exponential that appear to be missing are cancelled out due to symmetry factors one must add for each diagram. These factors give the number of ways we can interchange the lines and nodes of the diagram without changing it. 

Recall that taking functional derivatives allows us to compute any Green function, we get the pictorial equations
![[Pasted image 20261109164535.png|362]]

where we note that the first diagram comes with a symmetry factor of one-half, while the second diagram does not, as we have a symmetry factor of two. We also have 
![[Pasted image 20261109164713.png|369]]

where the leg labelled by $t$ could be connected to a bigger diagram.

To transition to quantum field theory, you can think of this transition as having $N$ particles $q_{a}(t)$ on a lattice, and as you take the lattice spacing to zero (and the number of particles to infinity) the lattice site label $a$ gets promoted to a coordinate and you obtain fields, $q_{a}(t)\to \phi(x,t)$. Note that for this reason we have denoted the particle's position by $q$ and not $x$. We were studying a non-relativistic particle moving in a one-dimensional space time, and QFT deals with higher dimensional spacetimes, so the generating functional is
$$Z[\phi]=\int \mathcal{D}\phi \exp\left[ \frac{i}{\hbar}\left( S[\phi]+\int d^{4}x J(x)\phi(x)\right) \right]\tag{6.9}.$$
