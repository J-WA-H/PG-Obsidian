Before considering the hard scattering of strongly interacting particles like protons, it can be useful to consider the simpler case of initial state lepton collisions, which relies on the simpler theory of QED.

In experiments, it is easy to require the energy of the actual collision to be close to the centre-of-mass energy of the colliding beams, however this cannot always be the case as an effect known as radiative return emits a photon from the incident leptons, denoted as QED initial-state radiation (ISR).

In QED ISR can be treated fairly easily using perturbation theory, but in QCD, the process is much more involved as the colliding particles cannot be interpreted as fundamental quanta, but as bound state hadrons that cannot be described by perturbation theory.

Classically, ISR can be understood with the equivalent photon picture, where in its own rest frame, the lepton acts as the point-like source of a purely radial electric field. Boosting the lepton outside of its rest frame introduces a magnetic field, and as $v\to c$, the two fields become increasingly confined to a plane perpendicular to the axis of motion, as well as perpendicular to each other. The accumulated energy flux is obtained by integrating the Poynting vector over the plane orthogonal to the lepton's axis of motion, which can be interpreted as photons. Their spectrum reads
$$\tag{1.1} dn_{\gamma}=\frac{\alpha}{\pi} \frac{d\omega}{\omega} \frac{dk_{\perp}^2}{k_{\perp}^2}.$$
In such a picture, the physical lepton is given by a superposition of states with varying photon multiplicity,
$$\ket{e} _{phys}=\ket{e} +\ket{e\gamma} +\ket{e\gamma \gamma}+\dots \tag{1.2} ,$$
where you have different energies and transverse momenta. Due to momentum conservation, they are typically off their mass shell, which limits the lifetime of quantum-fluctuations like $\ket{e\gamma}$ or $\ket{e\gamma \gamma}$.

The lifetime of the fluctuation is
$$\tau_{\gamma} \sim \frac{1}{\delta \omega}\approx \frac{2\omega}{k_{\perp}^2}=\frac{2xE}{k_{\perp}^2}\tag{1.3}.$$
Given that photons can split into a fermion-anti-fermion pair, another quantum fluctuation, they can emit further photons, complicating the wavefunction picture.

The wavefunction can be related, at leading order, by probabilities of finding the original lepton, the photons, or secondary leptons at given energies and transverse momenta. $\ell(x,k_{\perp})$ denotes the probability of finding a lepton at energy fraction $x$ and transverse momentum $k_{\perp}$. $\gamma(x,k_{\perp})$ gives the same for the photon. To leading order in $\alpha$, they are given by
$$\ell(x,k_{\perp}^{2}=0)=\delta(1-x) \qquad \text{and} \qquad \gamma(x,k_{\perp}^2=0)=0.\tag{1.4}$$
The radiation that gives rise to these particles can be described by the evolution equations that relate the probabilities of finding quanta with certain $x,k_{\perp}^2$. In the collinear factorisation scheme, they are
$$\frac{d\ell(x,k_{\perp}^{2})}{d\log k_{\perp}^{2}}=\frac{\alpha(k_{\perp}^{2})}{2\pi}\int_{x}^{1} \frac{d\xi}{\xi} \mathcal{P}_{\ell \ell}\left(  \frac{x}{\xi},\alpha(k_{\perp}^{2}) \right)\ell(\xi,k_{\perp}^{2})\tag{1.5}$$
$$\frac{d\gamma(x,k_{\perp}^{2})}{d\log k_{\perp}^{2}} = \frac{\alpha(k_{\perp}^{2})}{2\pi} \int_{x}^{1} \frac{d\xi}{\xi} \mathcal{P}_{\gamma \ell}\left( \frac{x}{\xi},\alpha(k_{\perp}^{2}) \right)\ell(\xi,k_{\perp}^{2})\tag{1.6}.$$
The effect of splitting photons into lepton anti-lepton pairs has been omitted. The first equation shows how the probability density of leptons with smaller energy fraction $x$ is driven by leptons with a larger energy fraction $\frac{x}{\xi}$, equivalent to a lepton losing an energy of $1-\xi$ by emitting a photon. The splitting functions, $\mathcal{P}_{\ell \ell}(x/\xi, \alpha)$, can be understood as the reduced matrix elements for the emission of one photon off the lepton. In general, $\mathcal{P}_{ba}$ denotes such kernels for a transition of a particle of type $a$ to a particle of type $b$, while emitting a particle of type $c$ which is not made explicit.

The splitting kernels at LO are given by
$$\mathcal{P}_{\ell \ell}(z)=e_{q}^{2} \left[ \frac{{1+z^{2}}}{(1-z)_{+}}+ \frac{3}{2}\delta(1-z) \right]\tag{1.7}$$
$$P_{\gamma \ell}(z)=e_{q}^{2}\left[ \frac{{1+(1-z)^{2}}}{z} \right].\tag{1.8}$$
The subscript $+$ is defined though
$$\int_{0}^{1}[f(z)]_{+}g(z)=\int_{0}^{1}dzf(x)[g(z)-g(1)]\tag{1.9}.$$
In a collision, one or more of the quantum excitations (particles forming the lepton's Fock state) may go onto their mass shell through exchange of 4-momentum, acquiring an infinite lifetime so they don't fall back into the original lepton like the case without collisions. These emitted photons are known as initial-state radiation.

Final-state radiation is when the final states emit photons through Bremsstrahlung. For example, in $e^{+}e^{ - }\to \mu^{+}\mu^{-}$, the production of the muon pair causes an acceleration which leads to the emission of photons.