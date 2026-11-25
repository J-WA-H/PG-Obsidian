The picture outline in [[Hard Scattering Formalism]] can be extended to include hadrons described by QCD. For now consider protons (or anti-protons), which consist of 3 valence quarks which carry the charge, spin, and isospin. This would imply each quark would carry 1/3 of the energy fraction, assuming no interactions between the quarks. Even including interactions that act like rubber bands gluing the valence quarks together, the energy fraction of each quark will average out to 1/3. Due to the nature of the coupling constant in QCD, this cannot be the case, as $\alpha_{s}$ accounts for quantum fluctuations, mediated by loop diagrams.

Including such corrections, and noting all QED and QCD corrections with $\alpha=g^2/4\pi$ they vary with the same scale $\mu_{R}$, also known as the renormalisation scale as
$$\mu_{R}^{2} \frac{\partial\alpha(\mu_{R}^{2})}{\partial \mu_{R}^{2}}=\beta(\alpha)\tag{2.1},$$
where the $\beta$-function $\beta(\alpha)$ can be expanded in a perturbative series and reads
$$-\beta(\alpha)=\sum_{n=o}^{\infty} b_{n} \alpha^{2+n} =\frac{\beta_{0}}{4\pi} \alpha_{s}^{2} +\frac{\beta_{1}}{(4\pi)^{2}} \alpha^{3}_{s}+\dots \tag{2.2}$$
This uses $\alpha_{s}=g_{s} / (4\pi)$ and $\alpha = e^{2} / (4\pi)$.

In an $SU(N)$ gauge theory, the first two coefficients $\beta_{i}$ read
$$\beta_{0}=\frac{11}{3}C_{A}-\frac{4}{3}T_{R}n_{f}\tag{2.3}$$
$$\beta_{1}=\frac{34}{3}C_{A}^{2}-\frac{20}{3}C_{A}T_{R}n_{f}-4C_{F}T_{R}n_{f}\tag{2.4}.$$
$n_{f}$ is the number of active fermions, and where the Casimir operators of the gauge group in its fundamental and adjoint representations are $C_{F}$ and $C_{A}$. In QCD they are given by
$$C_{F}\equiv C_{q}= \frac{{N_{c}^{2}-1}}{2N_{c}}\quad \text{and} \quad C_{A}\equiv C_{g}=N_{c}\tag{2.5}.$$
Also $T_{R}=1/2$.

To first order, and with a reference scale $Q$, the solution $(2.1)$ can be written as
$$\alpha(\mu_{R}^{2})\equiv \frac{g^{2}(\mu_{R}^{2})}{4\pi}= \frac{\alpha(Q^2)}{1+\alpha(Q^{2}) \frac{\beta_{0}}{4\pi}\log \frac{\mu_{R}^{2}}{Q^2}}\tag{2.6}.$$
In QCD the solution is
$$\alpha_{s}(\mu_{R}^{2})\equiv \frac{g_{s}^{2}(\mu_{R}^{2})}{4\pi} = \frac{1}{\frac{\beta_{0}}{4\pi} \log \frac{\mu_{R}^{2}}{\Lambda_{QCD}^{2}}}\tag{2.7}.$$
$\Lambda_{QCD}\approx 250\text{ MeV}$ is the QCD scale. The difference is due to the difference in the $\beta$-function, e.g. in QED, $\beta_{0}=-{2n_{f}}/{3}$. The difference in the overall sign, which is to the gluon loops absent in QED, implies that the strong coupling increases with increasing distance or decreasing scale. This is known as asymptotic freedom.

In a vacuum, in QED fermion anti-fermion pairs will fluctuate in and out of existence. If we introduce an electron, these fermion anti-fermion pairs will start to slightly polarise, orientating themselves in such a way that the positively charged fermions are closer to the election, and the negatively charge fermions further away. If we try to measure the charge of the election, a low $Q^2$ photon will only be able to see a large cloud of charged virtual particles, partially screening the charge of the election, while a high $Q^{2}$ photon can resolve much smaller distance, hence able to probe the electron with diminished influence of the screening cloud.

The case is similar in QCD but the gluons also carry colour charges and contribute to the screening effects. Their contribution comes with a sign opposite to the fermionic contribution. For small scales, $\mu_{R}\to\Lambda_{QCD}$, the running coupling diverges signalling the breakdown of perturbation theory and any ideas of treating quarks as quasi-free particles. This is the Landau pole of QCD.

Applying this to hadrons, we can get gluons being emitted by the quarks, and in turn splitting into gluon or quark anti-quark pairs, at small transverse momenta at scales of the order of $\Lambda_{QCD}^{2}$. This radiation of secondary particles is even stronger than in QED as the $1/k_{\perp}^2$ term in $(1.1)$ is enhanced by the multiplying with the strongly increasing $\alpha_{s}(k_{\perp}^2)$. Since gluons carry a colour charge, they also emit secondary gluons analogous to QED Bremsstrahlung off an electron. Adapting $(1.1)$ for QCD becomes
$$dn_{g}^{q,g}=C_{q,g} \frac{\alpha_{s}(k_{\perp}^{2})}{\pi} \frac{d\omega}{\omega} \frac{dk_{\perp}^{2}}{k_{\perp}^{2}} \tag{2.8},$$
where the colour factors $C_{q,g}=C_{F,A}$ are Casimir operators in the fundamental and adjoint representation of the gauge group underlying QCD, $SU(3)$. In the large-$N_{c}$ limit, $N_{c}\to \infty$, the colour charge of the quark becomes $N_{c}/2$, half as large as the gluon charge, reflecting how gluons carry two colour charges and quarks one. Therefore, gluons are twice more likely to emit a gluon than quarks. Note the large-$N_{c}$ limit is useful as any corrections are suppressed by $1/N_{c}^2$.

Due to the Landau pole, perturbative theory fails at transverse momenta around or below the pole, with the result being that bound state structures of hadrons is more complicated than the valance quarks.

Hard interactions with constituents of the complex Fock state describing an incident fermion breaks its coherence in QED, so something similar should also occur in QCD. There are differences, with the incident particle being a bound state hadron with complicated structure. Ignoring complications, above the Landau pole where we can use a perturbative description, the hadron is made from its valance partons, so, apart from colour exchange binding them together, these objects will start emitting softer quanta, which are known as sea partons. From coherence, the sea partons are forced to recombine, shown in the left panel below. In the right panel, the effect of a hard probe with a photon is shown. The parton that the photon interacts with is kicked out from the hadron, so the colour field is missing a quantum number so the remaining partons cannot recombine. The coherence breaks down and a more complex final state emerges through a reconfiguration of coloured particles.

![[Pasted image 20261102111111.png|500]]

Again starting from a naive picture of 3 quarks for a baryon and a quark anti-quark pair for a meson, multiple emissions of sea partons of these primary valance partons will occur, governed by Equation $(2.8)$. Similar to the case in QED, the lifetime of the sea partons is proportional to $\omega/k_{\perp}^{2}$, and their distance from the emitting valance quark is given by $1/k_{\perp}$. The coherence of the quantum states, encoded by the negative virtual mass, also guarantees, like in QED, that no partons can evade their hadron. In a hard collision this coherence can break down if a parton is kicked out, and the partons that stay behind may go on-shell, becoming physically meaningful objects. 

