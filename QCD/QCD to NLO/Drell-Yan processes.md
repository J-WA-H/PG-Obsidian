To understand one-loop calculations it is useful to consider the simplest case, Drell-Yan processes. These are process where a quark of one colliding hadron and an antiquark in another interact with each other, either annihilating into a photon/$Z^{0}$ if the quark flavour is the same, or produces a $W^{\pm}$ via the weak force. A one loop process for this could be $u\bar{d}\to W^{+}\to \ell^{+}\nu_{\ell}$ with a gluon loop as shown below.
![[Pasted image 20261120095650.png|373]]

The formula for the virtual amplitude is
$$\mathcal{M}_{u\bar{d}\to W^{+}}=g_{W}g_{s}^2 C_{F}\mu^{2\varepsilon}\int \frac{d^Dk}{(2\pi)^{D}}\left\{   \frac{g^{\nu \rho}}{k^2} \bar{v}(p_{d})\left[ \gamma_{\nu} \frac{{\not\! p_{d}+ \not\! k}}{(p_{d}+k)} \gamma^{\mu L} \frac{{\not\! p_{u}-\not\!k}}{(p_{u}-\not\!k)^2}\gamma_{\rho} + \gamma_{\nu} \frac{{\not\! p_{d}+ \not\!k}}{(p_{d}+k)^{2}}\gamma_{\rho} \frac{\not\!p_{d}}{p_{d}^2}\gamma^{\mu L} + \gamma^{\mu L} \frac{\not\!p_{u}}{p_{u}^2}\gamma_{\nu} \frac{{\not\!p_{u}-\not\!k}}{(p_{u}-k)^2}\gamma_{\rho} \right] u(p_{u})\varepsilon_{\mu}(W^{+})\right\}.\tag{2.1}$$
The contribution of the vertex correction, represented by the first term in the square brackets, is the only lengthy calculation that needs to be performed. This term can be written as
$$\mathcal{M}_{u\bar{d}\to W^{+}}^{(\text{vertex})}=g_{W}g_{s}^{2}C_{F} \mu^{4-D}\int \frac{d^Dk}{(2\pi)^{D}} \frac{V^{\mu}\varepsilon_{\mu}(W^{+})}{k^{2}(p_{d}+k)^{2}(p_{u}-k)^{2}},\tag{2.2}$$
where the current $V^{\mu}$ is
$$V^{\mu}=\bar{v}(p_{d})\gamma_{\nu}(\not\!p_{d}+\not\!k)\gamma^{\mu L}(\not\!p_{u}-\not\!k)\gamma^{\nu}u(p_{u})\tag{2.3}.$$
This expression is readily simplified with a little $\gamma$-matrix algebra to the form
$$V^{\mu}=\bar{v}(p_{d})[-2(\not\!p_{u}-\not\!k)\gamma^{\mu R}(\not\!p_{d}+\not\!k)+2\varepsilon a^{CDR}(\not\!p_{d}+\not\!k)\gamma^{\mu R}(\not\!p_{u}-\not\!k)]u(p_{u})\tag{2.4}.$$
The equation introduces a constant, $a^{CDR}$, that specifies the variant of the regularisation scheme to be used in the calculation. In conventional dimensional regularisation all quantities are continued into $D$ dimensions such that $\gamma_{\mu}\gamma^{\mu}=D=4-2\varepsilon$. This corresponds to the choice $a^{CDR}=1$. In dimensional reduction only loop momentum is continued into $D$ dimensions, and then $\gamma_{\nu}\gamma^{\nu}=4$ implying that $a^{CDR}=0$.

In order to evaluate the loop integral, it is simplest to combine the loop propagators by introducing Feynman parameters, here $x,y,z$. Applying the identity
$$\frac{1}{A_{1}^{\nu_{1}}\dots A_{n}^{\nu_{n}}}=\frac{\Gamma(\nu)}{\prod_{i}\Gamma(\nu_{i})}\int_{0}^{1}d^nx_{i}\delta\left( \sum_{i}x_{i}-1 \right) \frac{\prod_{i}x^{\nu_{i}-1}_{i}}{\left( \sum_{i}x_{i}A_{i} \right)^{\sum_{i}\nu_{i}}}\tag{2.5}$$
yields
$$\frac{1}{(p_{d}+k)^2(p_{u}-k)^2k^2}=\int_{0}^{1}dxdydz \frac{2\delta(1-x-y-z)}{[x(p_{d}+k)^{2}+y(p_{u}-k)^{2}+zk^2]^{3}}=\int_{0}^{1}dx \int_{0}^{1-x}dy \frac{2}{[k^2+2k\cdot(xp_{d}-yp_{u})]^3}\tag{2.6}$$
where one of the Feynman parameters has been eliminated immediately using the $\delta$-function. In a second step, the denominator has been simplified with the on-shell conditions $p_{u}$ and $p_{d}$. It is now useful to shift the variable of integration from $k$ to $\ell$ with the relation $k=\ell-xp_{d}+yp_{u}$. After this shift the denominator takes the simple form $(\ell^2+Q^2xy)^3$ where $Q^2=2p_{d}\cdot p_{u}$. 

At a first glance, performing the same shift on the current $V^{\mu}$ leads to a proliferation of terms. However, since the denominator is an even function of $\ell$, any odd powers of $\ell$ may be dropped in the numerator since they will vanish upon integration. Moreover, the integral of the term $\ell^{\alpha}\ell^{\beta}$ must be proportional to $g^{\alpha\beta}$ and contracting with $g_{\alpha\beta}$ fixes the overall constant. It is therefore sufficient to replace $\ell^{\alpha}\ell^{\beta}\to g ^{\alpha \beta} \ell^2/D$ under the integral. Finally the equations of motion for the spinors $\bar{v}(p_{d}) \not\!p_{d}=\not\!p_{u}u(p_{u})=0$ greatly simplify many of the resulting expressions.

After this simplification the integral becomes
$$\int \frac{d^{D}k}{(2\pi)^{D}} \frac{V^{\mu}}{k^{2}(p_{d}+k)^{2}(p_{u}-k)^{2}}=\int_{0}^{1}dx \int_{0}^{1-x}dy \int \frac{d^D\ell}{(2\pi)^{D}} \frac{4N\bar{v}(p_{d})\gamma^{\mu L}u(p_{u})}{(\ell^2+Q^2xy)^3}\tag{2.7},$$
where
$$N=Q^2[(1-x)(1-y)-\varepsilon a^{CDR}xy]-\ell^2(1-a^{CDR}\varepsilon)\left( 1-\frac{2}{D} \right)\tag{2.8}.$$
As a consequence of the spinor structure the vertex correction is proportional to the leading order amplitude. The integrals over the loop momentum are now easily performed by using a Wick rotation, whose general result is
$$\int \frac{d^D\ell}{(2\pi)^{D}} \frac{(\ell^2)^{k}}{(\ell^2-\Delta)^n}=\frac{i(-1)^{n-k}}{(4\pi)^{D/2}} \frac{\Gamma(D/2+k)}{\Gamma(D/2)} \frac{\Gamma(n-k-D/2)}{\Gamma(n)}(\Delta-i\varepsilon)^{D/2-n+k}\tag{2.9}.$$
The solutions this gives are
$$\int \frac{d^D\ell}{(2\pi)^D} \frac{\ell^2}{(\ell^2+Q^2xy)^3}=\frac{i}{(4\pi)^{D/2}}\left( \frac{D}{4} \right)\Gamma(\varepsilon)[-Q^2xy]^{-\varepsilon} \\ \int \frac{d^D\ell}{(2\pi)^D} \frac{1}{(\ell^2+Q^2xy)^3}= -\frac{i}{(4\pi)^{D/2}}\left( \frac{1}{2} \right)\Gamma(1+\varepsilon) [-Q^2xy]^{-1-\varepsilon}.\tag{2.10}$$
Hence
$$\int \frac{d^D\ell}{(2\pi)^D} \frac{4N}{(\ell^2+Q^2xy)^3}=\frac{i\Gamma(1+\varepsilon)}{(4\pi)^{D/2}}(-Q^2)^{-\varepsilon}\left\{  2[(1-x)(1-y)-\varepsilon a^{CDR}xy]x^{-1-\varepsilon}y^{-1-\varepsilon}-2(1-a^{CDR}\varepsilon)(1-\varepsilon) \frac{1}{\varepsilon}x^{-\varepsilon}y^{-\varepsilon}  \right\}\tag{2.11}.$$
The integral over $y$ can now be performed in a straight forward manner. The remaining $x$ integral is immediately in the form of a beta function that can in tern be expressed explicitly in terms of gamma functions. After manipulating these and dropping terms of order $\varepsilon$ he final result for the integral is
$$\int \frac{d^Dk}{(2\pi)^{D}} \frac{V^\mu}{k^2(p_{d}+k)^2(p_{u}-k)^2}=\bar{v}(p_{d})\gamma^{\mu L}u(p_{u}) \frac{i(-Q^2)^{-\varepsilon}}{(4\pi)^{2-\varepsilon}} \frac{\Gamma(1+\varepsilon)\Gamma^2(1-\varepsilon)}{\Gamma(1-2\varepsilon)}\left[ \frac{2}{\varepsilon^2}+\frac{3}{\varepsilon}+7+a^{CDR} \right]\\=-i\bar{v}(p_{d})\gamma^{\mu L}u(p_{u})\left( -\frac{4\pi}{Q^2} \right)^{\varepsilon} \frac{1}{16\pi^2} \frac{1}{\Gamma(1-\varepsilon)} \left[ -\frac{2}{\varepsilon^2}-\frac{3}{\varepsilon}-7-a^{CDR} \right]\tag{2.12}.$$
Restoring the overall factors present in $(2.2)$ and extracting the leading order amplitude, the result for the vertex correction to the amplitude is
$$\mathcal{M}_{u\bar{d}\to W^{+}}^{(\text{vertex})}=\mathcal{M}_{u\bar{d}\to W^{+}}^{(0)} \frac{\alpha_{s}}{4\pi}C_{F}\left( -\frac{4\pi \mu^2}{Q^2} \right)^{\varepsilon} \frac{1}{\Gamma(1-\varepsilon)}\left[ -\frac{2}{\varepsilon^2}-\frac{3}{\varepsilon}-7-a^{CDR} \right].\tag{2.13}$$
It is common to identify the factor
$$c_{\Gamma}=\frac{(4\pi)^{\varepsilon}}{\Gamma(1-\varepsilon)}=1+\varepsilon(1+\log(4\pi)-\gamma_{E})+\mathcal{O}(\varepsilon^2)\tag{2.14}$$
which is a universal factor in one-loop calculations. In addition, for the Drell-Yan process, the kinematics require $Q^2>0$ so that it is also necessary to expand the factor $(-1)^{\varepsilon}=1+i\pi\varepsilon-\pi^2\varepsilon^2/2+\mathcal{O}(\varepsilon^2)$. Putting this together yields the final expression
$$\mathcal{M}_{u\bar{d}\to W^{+}}^{(\text{vertex})}=\mathcal{M}_{u\bar{d}\to W^{+}}^{(0)} \frac{\alpha_{s}}{4\pi}C_{F}\left( \frac{\mu^2}{Q^2} \right)^{\varepsilon}c_{\Gamma}\left[ -\frac{2}{\varepsilon^2}-\frac{3}{\varepsilon}-7-a^{CDR}+\pi^2-i\pi\left( \frac{2}{\varepsilon}+3 \right) \right].\tag{2.15}$$
This amplitude enters the cross-section in the virtual correction term $\mathcal{V}$ as
$$\mathcal{V}=2\mathrm{Re}[\mathcal{M}_{u\bar{d}\to W^{+}}^{(1)}\mathcal{M}^{*(0)}_{u\bar{d}\to W^{+}}],\tag{2.16}$$
In conventional dimensional regularisation, with $a^{CDR}=1$, this thus leads to the result for the full virtual contribution. To complete the derivation it is only necessary to demonstrate that the contribution of the self-energy corrections is zero. Repeating the same steps as above for the self-energy contributions, the result is proportional to the value of the integral
$$\int \frac{d^D\ell}{(2\pi)^{D}} \frac{1}{(\ell^2)^2}\tag{2.17}.$$
However since this integral has dimension $D-4$ but contains no dimensionful quantities with which to express the result, it must vanish. As a result, self-energy contributions on massless external lines are zero within dimensional regularisation.

