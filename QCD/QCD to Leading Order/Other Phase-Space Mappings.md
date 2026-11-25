The [isotropic phase-space](Phase-space%20Integration.md) is a good example of a democratic approach where all particles are treated equally. However, a uniform phase space will not deliver accurate results when the distribution of final state momenta is not uniform. There is another set of processes where a democratic approach delivers better results, processes with QCD only final states, where the leading amplitudes assume a simple form. For instance, for purely gluonic processes the most singular amplitudes are the $\text{MHV}$ and $\overline{\text{MHV}}$, which for a colour-ordered $n$-gluon process behave like
$$\mathcal{A}_{n}^{\text{MHV},\overline{\text{MHV}}}\propto \prod_{i=1}^{n} \frac{1}{s_{i(i+1)}}\quad \text{with}\quad \hat{s}_{n(n+1)}=\hat{s}_{n 1}\tag{7.1}.$$
This simple form is also recovered in other processes; the inclusion of quarks just leads to the absence of some of the $1/\hat{s}$ factors, therefore rendering the amplitudes somewhat less complicated to integrate. 

A first method that has been optimised for the integration of such amplitudes is SARGE. It builds on sequentially filling the phase space through emissions that follow the basic antenna density
$$d\mathcal{A}_{ij}^{k}=\frac{1}{\pi}d^{4}p_{k}\delta p_{k}^{2}\Theta(p_{k}^{0}) \frac{{(p_{i}p_{j})}}{(p_{i}p_{k})(p_{j}p_{k})}g(\xi_{ij}^{ik})g(\xi_{ij}^{jk}).\tag{7.2}$$
where the
$$\xi_{ij}^{jk}=\frac{{(p_{j}p_{k})}}{(p_{i}p_{j})}\tag{7.3}$$
are the arguments of the regulator functions
$$g(\xi)=\frac{1}{2\log \xi_{m}}\Theta(\xi-\xi_{m}^{-1})\Theta(\xi_{m}-\xi),\tag{7.4}$$
which ensure that the divergences for $(p_{i}p_{k})\to 0$ and $(p_{j}p_{k})\to 0$ are avoided and are chosen such that $d\mathcal{A}$ integrates to unity. The cut-off value $\xi_{m}$ depends on the actual cuts being applied on the outgoing momenta. Demanding that for each pair of momenta $i,j$, $(p_{i}+p_{j})^{2}\geq s_{0}$, the expression for $\xi_{m}$ is
$$\xi_{m}=\frac{\hat{s}}{s_{0}}-\frac{(n+1)(n+2)}{2}\tag{7.6}$$
To generate a momentum $p_{k}$ according to the basic antenna structure SARGE proceeds along the following steps:
- The initial momenta $p_{i},p_{j}$ are boosted into their centre-of-mass frame
- Two numbers $\xi_{ij}^{ik},\xi_{ij}^{jk}$ are generated with a probability density of $g(\xi)/\xi$. They allow the calculation of the energy of the particle $k$, $p_{k}^{0}$, and its polar angle $\theta$ with respect to $p_{i}$.
- The azimuthal angle is chosen uniformly in $[0,2\pi]$, which then enables the construction of $p_{k}$ in the rest frame of $i.j$. 
- Boosting $p_{k}$ back into their lab frame finishes the generation of one emitted momentum. 

It is worth noting that this algorithm does not respect four-momentum conservation, since recoil effects on the emitters $i,j$ are not captured here.

The algorithm is now iterated to yield all outgoing momenta along the following lines. Generating two outgoing momenta $q_{1},q_{2}$ in the centre-of-mass frame of the partonic collision triggers the consecutive generation of the $(n-2)$ other momenta through the basic antennae $d\mathcal{A}_{1n}^{2}d\mathcal{A}_{2n}^{3}\dots d\mathcal{A}_{(n-2)n}^{n-1}$ already discussed. Using the same boost and scaling transformation yields the final momenta $p_{i}$ which, by construction, satisfies 4-momentum conservation.

There also process where a democratic approach cannot be used, where the final state particles emerge from a very specific set of Feynman diagrams which could be interpreted as a sequence of production processes of usually resonant particles followed by their decay into lighter particles. An example of this is the production of a $t\bar{t}$ pair and its subsequent decay into two $b$ quarks and two $W$ bosons, which in turn decay further. In such a case democratic and, in particular, isotropic mappings will not be efficient as the particles are not distributed independently in phase space but will enjoy strong correlations due to the intermediate resonances. Knowing this and understanding the underlying phase space structure lends itself to the textbook Monte Carlo method of importance sampling for efficient phase space generation.

In the example of $t\bar{t}$ production and decay this could be achieved by:
- Assuming a useful distribution of the $t\bar{t}$ pair in terms of its centre of mass energy and rapidity, which for an $e^{+}e^{-}$ collider could naively be fixed, while for hadron colliders PDF effects would have to be taken into account. 
- Then, in the centre of mass frame of the pair, the top and the anti-top would be isotropically distributed, with back-to-back kinematics and their invariant mass given by a Breit-Wigner form.
Each of the top decays, again, could be treated in their respective rest frame, with the invariant masses of the $W$'s again given through a Breit-Wigner form. This process would be finally for the $W$s.

This implies a hierarchical structure of Breit-Wigner distributed invariant masses of the intermediate resonant particles followed by their binary decays, which in the respective rest frames reduces to choosing one pair $(\theta,\phi)$ fixing the orientation in the solid angle of the back-to-back binary decay kinematics.

This example can be extended also for processes where a number of hierarchies compete with each other. Up to now the best solution for such cases can be constructed by combining different mappings in a dynamic form. This is the multi-channel method. Expressed in technical terms, this method presents itself as an interesting amalgamation of the traditional Monte Carlo integration methods of stratified and importance sampling, where the binning of the stratified sampling is not in actual integration parameters or phase-space but rather independent functional forms of individual mappings. Multi-channeling performs a stratified sampling over various importance samplings.

Mathematically speaking, a mapping function $g(\vec{x})$ is constructed as a sum of individual mappings $g_{j}(\vec{x})$, each of them with an a priori weight $a_{j}$:
$$g(\vec{x})=\frac{1}{\sum_{j}a_{j}}\sum_{j}a_{j}g_{j}(x)\tag{7.7}.$$
As before, the estimate for the integral is given by
$$\langle I \rangle _{x}\equiv \langle f \rangle _{x}=\langle f/g \rangle_{g}\tag{7.8} $$
and the error estimate is
$$\langle E(a) \rangle =\sqrt{ \left\langle \left( \frac{f}{g} \right)^2 \right\rangle_{g}-\left( \left\langle \frac{f}{g} \right\rangle_{g}  \right)^2  }\tag{7.9}.$$
While in principle the integral does not depend on the $a_{j}$, its estimator and, more importantly, the error estimator does. This can easily be understood by writing the expressions above again as an integral. In $I$ the mapping function $g$ cancels, but this is not the case in the first term of $E$:
$$I=\int_{V}d^Dx\,g(\vec{x}) \frac{f(\vec{x})}{g(\vec{x})}=\int_{V}d^Dx\,f(\vec{x}) \\ E=\int_{V}d^Dx\,g(\vec{x}) \left( \frac{f(\vec{x})}{g(\vec{x})} \right)^{2}-I^2\int_{V}d^Dx \frac{f^2(\vec{x})}{g(\vec{x})}-I^2.\tag{7.10}.$$
From here it would be trivial to rediscover stratified sampling by using mappings $g_{j}(x)$ which are unity inside the bin $j$ and zero outside.

This however is not how multi-channel sampling is being used for the phase space integration in scattering processes in particle physics. There, the form of the transition matrix is known. Using, for instance, Feynman diagrams to construct it, one can obtain individual phase-space mappings $g_{j}$ respecting the kinematics of an individual diagram, which is mainly driven by its propagator structure. In principle, they can be represented by intuitive mappings: a simple pole of the form $1/\hat{s}$ for a massless particle, a Breit-Wigner form, defined by the mass $M$ and width $\Gamma$ of the propagating particle, $1/[(\hat{s}-M^2)^2+M^2\Gamma^2]$, and a $t$-channel propagator $1/(\hat{t}-m^2)$. Similar structures also exist for decays, for example isotropic two-body decays of a massive particle, or anisotropic decays to capture, for example, the emission of a gluon or photon in the final state. The individual mappings are then composed by a sequence of decays and propagators, basically a hierarchical mapping for each diagram. This is fairly straightforward. What is typically not clear, though, is which specific phase-space configurations dominate the behaviour of the cross-section, especially in the presence of non-trivial cuts on some of the outgoing momenta. In such a setip, when a suitable linear combination of the most important mappings is hard to find, importance sampling loses its power. Then, the stratified sampling part of the integration does the work and automatically finds a well-suited integration setup.

