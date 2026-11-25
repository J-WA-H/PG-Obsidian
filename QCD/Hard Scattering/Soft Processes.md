Starting at some scale with a parton with some momentum, the [DGLAP](Deep%20Inelastic%20Scattering.md) equation describes how, by successive emissions, momentum is carried away by secondary partons, until the scale is reached where the hadron is measured.

As gluons carry a colour charge, the emission pattern in QCD is very different to QCD, as emitted gluons can further radiate gluons themselves. The splitting function reveals that the emission of secondary gluons off gluons exhibits divergent structures in the splitting parameter $z$, namely $1/z$ and $1/(1-z)$. This, compared to the finite structure of bosons splitting into fermions, drives a further acceleration of radiation beyond the effect of the larger coupling in QCD compared to QED. Ignoring the finite splitting of bosons into fermion pairs, the colour of the gluons means that the simple eikonal picture of iterating independent emissions in QED will not directly translate into QCD, since for any photon emission is always spanned by the muons acting as eikonal partners $p,p'$ and the emission of photons by photons is absent in the QED case. In the QCD case, as gluons can emit gluons, after each gluon emission, the structure of the eikonals will change, as the emitted gluons introduce more directions of the colour field. In the large-$N_{c}$ limit, this leads to the notion of colour dipoles emitting gluons. The leading behaviour of QCD emission processes follows a pattern given by
$$dw^{q\to qg}= \frac{\alpha_{s}(k_{\perp}^{2})}{2\pi} C_{F} \frac{dk_{\perp}^{2}}{k_{\perp}^{2}} \frac{d\omega}{\omega}\left[ 1+\left( 1-\frac{\omega}{E} \right)^{2} \right]= \frac{\alpha_{s}(k_{\perp}^{2})}{2\pi} C_{F} \frac{dk_{\perp}^{2}}{k_{\perp}^{2}} dz \frac{{1+z^{2}}}{1-z} = \frac{\alpha_{s}(k_{\perp}^{2})}{2\pi} C_{F} \frac{dk_{\perp}^{2}}{k_{\perp}^{2}} dz P_{gg}^{(1)}(z).\tag{4.1}$$
This is for gluon emission off a quark with energy $E$. In the soft limit, for vanishing gluon energies $\omega=E(1-z)$, this reproduces the dipole form.

The emission of massless final state partons leads to divergences of the form $1/k_{\perp}^{2}$ and $1/\omega$ as seen in $(4.1)$ that need to be cured. Typically a cut on the phase space of resolvable emissions is applied, which in the case of photons could be expressed by minimal photon energies. In QCD, this cut-off would be provided by the scale at which the phase transition of the partons to the hadrons occurs. This is done by parameterising this scale through a cut on relative transverse with respect to its emitters, and as it must by far above the Landau pole of QCD, such cut offs are of the magnitude $k_{\perp}^{(min)}\approx 1\text{ GeV}>\Lambda_{QCD}$.

For quarks or other colour charges being produced at energies $E$ in a hard interaction, time dilation occurs, similar to how charged particles experience it in QED. The reasoning has far-reaching consequences .Identifying with $m$ the constituent mass of a quark, typically $\mathcal{O}(\Lambda_{QCD})\approx R^{-1}$ for light quarks and $m_{Q}$ for heavy quarks, and with $r_{\perp}$ a typical hadronic size, $R=\mathcal{O}(1\text{ fm})$, immediately yields a hadronisation time $t^{(had)}$ proportional to the energy of the quark,
$$t^{(had)}\approx \begin{cases}
ER^{2}  & \text{for light quarks} \\
ER/M_{Q} & \text{for heavy quarks}
\end{cases}\tag{4.2}.$$
Qualitatively, this naive picture emerges in a quantum mechanical treatment. For hadrons of characteristic size $R$, the confining QCD forces are associated with gluon fields with typical momenta
$$k\approx k_{\parallel}\approx k_{\perp}\approx R^{-1}\tag{4.3}$$
in the hadronic rest frame. They emerge after typical times
$$t\approx R \approx \frac{1}{k_{\perp}}\tag{4.4},$$
which, including a Lorentz boost factor as before leads to hadronisation times
$$t^{(had)}\approx \frac{k_{\parallel}}{k_{\perp}^{2}}\approx \frac{ER}{m}\tag{4.5}.$$
Here $m$ is a typical hadronic mass scale; the result is the same as in the classical approach above.

It is also important to see how long it actually takes for a gluon to form in the emission off, say, a quark. Naively, this formation time can be estimated from the invariant mass of the quark-gluon pair and its energy as
$$t^{(form)}\approx \frac{1}{m_{qg}} \frac{E}{m_{qg}} \approx \frac{E}{kE\theta^{2}_{qg}}\approx \frac{k}{k_{\perp}^{2}} \approx \frac{k_{\parallel}}{k_{\perp}^{2}} \tag{4.6}.$$
The starting point is given by a combination of uncertainty principle and Lorentz time dilation effects, and in some intermediate steps a small opening angle of the resulting pair has been assumed.

Comparing this with the hadronisation time and demanding that gluons be formed before they hadronise, yields a constraint on the emission kinematics:
$$\frac{k_{\parallel}}{k_{\perp}^{2}}\approx t^{(form)}\leq t^{(had)}\approx k_{\parallel}R^{2} \to k_{\perp} \geq \frac{1}{R} = \mathcal{O}(\sim \text{few } \Lambda_{QCD}).\tag{4.7}$$
Extending this case for heavy quarks $Q$, such as top quarks, it is worth noting that in their case the lifetime given by
$$\tau_{Q}\sim \left( \frac{m_{W}}{m_{Q}} \right)^{3} \frac{E}{m_{q}}\ll \frac{E}{m_{q}} \sim t^{(had)}\tag{4.8}$$
is smaller than their hadronisation time, they behave as truly free quarks.

At this low scale, QCD enters a new regime, where the strong interaction becomes so strong that the partons start to confine into hadronic states. As in the initial case, the transition between parton and hadron cannot be quantitatively described. This is where the FFs become important. A significant difference from PDFs in the initial state as there may be more than one hadron emerging from a parton, so the FFs describe the transition of the parton into the corresponding hadron plus any other hadrons. They are mainly useful for describing the inclusive production of this one given hadron in a collision, ignoring all other hadrons which may eventually emerge as well. To reach a more inclusive picture, other methods are nessesary. 