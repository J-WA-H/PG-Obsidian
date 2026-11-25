It is useful to understand deep-inelastic scattering (DIS) where an electron interacts with a proton by exchanging a highly virtual photon. Since the virtual mass of the photon $Q$ is much larger than the proton mass, it can probe the proton's deep internal structure. To analyse the process, the Breit-frame is used. This is the Lorentz frame where the proton moves with a large velocity and the virtual photon has no energy. Their respective momenta are given by
$$\begin{matrix}
P^{\mu}=(P_{0},0,0,P_{z}) \text{ with } P_{z} = \sqrt{ P_{0}^{2} - m_{P}^{2} }\approx P_{0} \\
q^{\mu}=(0,0,0,-q_{z}) \text{ with } Q^{2} = -q^{2} = q_{z}^2
\end{matrix} \tag{3.1}.$$
Introduce the Bjorken variable $x_{B}$,
$$x_{B} = -\frac{q^{2}}{2P\cdot q} =\frac{q_{z}^{2}}{2P_{z}q_{z}}\tag{3.2}.$$
This implies that $q_{z}=2x_{B}P_{z}$. The time of the interaction between the photon and the proton is given by the longitudinal wavelength of the photon, hence
$$\tau_{int} \sim \lambda_{z} \sim \frac{1}{q_{z}}\tag{3.3}$$
For the photon to see the partons inside the hadron, they must have wavelengths at least as large as the photon, which is purely longitudinal. As their longitudinal momenta must be the same, their momenta must also be the same, $p_{z}=q_{z}$. The momentum fraction must then be of the same order as $x_{B}$. The lifetime of these partons is $\tau_{parton}\sim p_{z}/p_{\perp}^{2}$ which is larger than the interaction time provided $p_{z}\gg p_{\perp}$.

In this setup, the point-like photons measure the number of partons with similar longitudinal momentum in an area of size $1/Q^2$, at a momentum fraction of $x=x_{B}$ at a scale $Q^2$. The cross-section is then proportional to the sum of probabilities to find partons with this kinematics, that can interact with the photon, i.e. ignoring higher order diagrams,
$$\sigma_{ep}\sim \sum_{q} e^{2}_{q} f_{q/p}(x,Q^2)\tag{3.4}.$$
if the photon that is responsible for the interaction has a negative virtual mass squared with absolute value $Q^2$ and longitudinal momentum fraction $x$.

If this picture holds true, the photon-parton collision can be treated as the collision of two independent quasi-free particles; the struck parton does not fell the presence of the surrounding partons forming the proton, since the interaction time is smaller than the lifetime of the parton. In this framework, the probabilities to find partons with a given momentum fraction $x$ at a scale $Q^2$ inside a proton is process-independent so the DIS setup with exchanged photons can be replaced by other processes with similar kinematics. Therefore it is sensible to encode the probability of finding a parton $p$ in a hadron $h$ as process-independent parton distribution functions (PDFs) $f_{p/h}(x,Q^2)$.

The PDFs cannot be calculated from first principles since they are truly non-perturbative objects, but they can be measured in different processes and at different scales. These can be related to each other through the DGLAP equations, which for QCD is
$$\frac{\partial}{\partial \log Q^{2}} \begin{bmatrix}
f_{q/h}(x,Q^{2}) \\
f_{g/h}(x, Q^{2})
\end{bmatrix}= \frac{\alpha_{s}(Q^{2})}{2\pi} \int_{x}^{1} \frac{dz}{z} \begin{bmatrix}
\mathcal{P}_{qq}\left( \frac{x}{z} \right) & \mathcal{P}_{qg}\left( \frac{x}{z} \right) \\
\mathcal{P}_{gq}\left( \frac{x}{z} \right) & \mathcal{P}_{gg}\left( \frac{x}{z} \right)
\end{bmatrix} \begin{bmatrix}
f_{q/h}(z, Q^{2}) \\
f_{g/h}(z,Q^2)
\end{bmatrix}\tag{3.5}.$$
The sum over different $2n_{f}$ quark flavours/antiflavours is implicit. The convolution could be schematically written as
$$\frac{\partial}{\partial \log Q^{2}} \begin{bmatrix}
f_{q/h}(Q^{2}) \\
f_{g/h}(Q^2)
\end{bmatrix} = \frac{\alpha_{s}(Q^{2})}{2\pi} \begin{bmatrix}
\mathcal{P}_{qq} & \mathcal{P}_{qg} \\
\mathcal{P}_{gq} & \mathcal{P}_{gg}
\end{bmatrix} \otimes \begin{bmatrix}
f_{q/h}(Q^2) \\
f_{g/h}(Q^2)
\end{bmatrix}.\tag{3.6}$$
The kernels of the evolution equation are the splitting functions, which at leading order are given by
$$\mathcal{P}_{qq}^{(1)}(x)=C_{F}\left[ \frac{{1+x^{2}}}{(1-x)_{+}} +\frac{3}{2} \delta(1-x) \right]=[P_{qq}^{(1)}(x)]_{+}+\gamma_{q}^{(1)}\delta(1-x)$$
$$\mathcal{P}_{qg}^{(1)}(x) = T_{R} [x^{2}+(1-x)^{2}]=P_{qg}^{(1)}(x)$$
$$\mathcal{P}_{gq}^{(1)}(x)=C_{F}\left[ \frac{{1+(1-x)^{2}}}{x} \right]=P_{gq}(x)^{(1)}\tag{3.7}$$
$$\mathcal{P}_{gg}^{(1)}(x)=2C_{A} \left[ \frac{x}{(1-x)_{+}} + \frac{{1-x}}{x} +x(1-x) \right]+ \frac{{11C_{A}-4n_{f}T_{R}}}{6}\delta(1-x)=[P_{gg}^{(1)}(x)]_{+}+\gamma^{(1)}_{g}\delta(1-x).$$
Here $x$ is the splitting parameter, essentially governing the light-cone momentum fraction of the offspring with respect to its emitter. Note that the indices of both $\mathcal{P}_{ba},P_{ba}$ are related to the parton splitting process $a\to bc$, where the type $c$ is fixed by $a$ and $b$. The $\mathcal{P}^{(o)}(x)$ are also called regularised splitting functions to order $o$. 

We can also define fragmentation functions (FFs) $D_{p/h}(x,Q^2)$ which gives the probabilities of finding the hadron or photon $h$ emerging from parton $p$ at a scale $Q^2$ and carrying the fraction $x$ of the partons light-cone momentum. Like PDFs, FFs cannot be calculated but must be measured. Starting at some scale with a parton with some momentum, the DGLAP equation describes how, by successive emissions, momentum is carried away