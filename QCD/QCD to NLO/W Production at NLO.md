To give an example of subtraction it is useful to look at the real radiation contributions NLO corrections to $W$ production, in particular the process $u\bar{d}\to gW^{+}$. The squared matrix element for this process is
$$|\mathcal{M}|^2_{u\bar{d}\to g W^{+}}= \frac{|\mathcal{M}^{(LO)}|^2_{u\bar{d}\to W^{+}}}{m_{W}^{2}}(4\pi\alpha_{s}C_{F}) \frac{{\hat{t}^2+\hat{u}^2+2m_{W}^2\hat{s}}}{\hat{t}\hat{u}}\tag{4.1}.$$
This is divergent in the limits $\hat{t},\hat{u}\to 0$. The key to the general approach for handling these IR singularities lies in the ability to deal with collinear singularities associated with each of these limits separately. This can be seen by analysing the kinematic dependence, isolating the divergent terms and then using partial fractioning
$$\frac{{\hat{t}^2+\hat{u}^2+2m_{W}^2\hat{s}}}{\hat{t}\hat{u}}=\frac{{(\hat{t}+\hat{u}^2)+2m_{W}^{2}\hat{s}}}{\hat{t}\hat{u}}-2=\left( \frac{1}{\hat{t}}+\frac{1}{\hat{u}} \right) {\frac{(\hat{t}+\hat{u})^2+2m_{W}^{2}\hat{s}}{\hat{t}+\hat{u}}}-2=\left( \frac{1}{\hat{t}}+\frac{1}{\hat{u}} \right)\left[ (m_{W}^{2}-\hat{s})+\frac{2m_{W}^{2}\hat{s}}{m_{W}^{2}-\hat{s}} \right]-2\tag{4.2}.$$
Overall momentum conservation has been employed, embodied by the identity $\hat{s}+\hat{t}+\hat{u}=m_{W}^{2}$. Furthermore the terms in the square brackets can be written in terms of the single dimensionless quantity $x=m_{W}^{2}/\hat{s}$ leading to
$$|\mathcal{M}^{(LO)}_{u\bar{d}\to g W^{+}}|^2=\frac{2\pi C_{F}\alpha_{s}(\mu_{R})}{m_{W}^2}|\mathcal{M}_{u\bar{d}\to W^{+}}^{(LO)}|^2 \left[ \frac{{\hat{t}^2+\hat{u}^2+2m_{W}^{2}\hat{s}}}{\hat{t}\hat{u}} \right] = \frac{2\pi C_{F}\alpha_{s}(\mu_{R})}{x}|\mathcal{M}^{(LO)}_{u\bar{d}\to W^{+}}|^2 \left[ \left( \frac{1}{\hat{t}}+\frac{1}{\hat{u}} \right)\left( -\frac{2}{1-x}+x+1 \right)-\frac{2x}{m_{W}^{2}} \right]\tag{4.3}$$
for the amplitude squared of the real emission contribution. Isolating the divergent terms $\propto 1/\hat{t},1/\hat{u}$, the equation above can be cast into the form
$$|\mathcal{M}_{u\bar{d}\to gW^{+}}^{(LO)}|^2=\frac{1}{x} |\mathcal{M}^{(LO)}_{u\bar{d}\to gW^{+}}|^2[\mathcal{D}(\hat{t},x)+\mathcal{D}(\hat{u},x)+\mathcal{R}(x)].\tag{4.4}$$
The infrared-singular terms are expressed in terms of the function $\mathcal{D}(\hat{t},x)$, where
$$\mathcal{D}(\hat{t},x)=8\pi\alpha_{s}C_{F}\left[ -\frac{1}{\hat{t}}\left( \frac{2}{1-x}-1-x \right) \right]\tag{4.5}$$
and the non-singular remainder reads
$$\mathcal{R}(x)=8\pi\alpha_{s}C_{F}\left[ -\frac{2x}{m_{W}^{2}} \right]\tag{4.6}.$$
The sum of the two singular terms forms the subtraction term,
$$\mathcal{S}(\Phi_{\mathcal{R}})=\frac{1}{x}|\mathcal{M}^{(LO)}_{u\bar{d}\to W^{+}}|^{2}[\mathcal{D}(\hat{t},x)+\mathcal{D}(\hat{u},x)]\tag{4.7}.$$
To compute the corresponding integrated subtraction term, $\mathcal{I}^{(\mathcal{S})}$, first the phase space must be appropriately factorised to allow an analytic integration over the one-particle phase space of the emitted gluon. The phase space is given by
$$d\Phi_{Wg}=\frac{d^Dp_{W}}{(2\pi)^{D}}(2\pi)\delta(p_{W}^2-m_{W}^2) \frac{d^Dp_{g}}{(2\pi)^{D}}(2\pi)\delta(p_{g}^{2})(2\pi)^{D}\delta^{(D)}(p_{a}+p_{b}-p_{W}-p_{g})=(2\pi)^{2-D} \frac{d^{D-1}p_{g}}{2E} \delta((p_{a}+p_{b}-P_{g})^2-m_{W}^2)\tag{4.8}$$
where $E$ represents the energy of the gluon. It is straightforward to evaluate this in the centre of mass frame,
$$d\Phi_{Wg}=\frac{(2\pi)^{2\varepsilon-2}}{2\sqrt{ \hat{s} }}\left( \frac{\hat{t}\hat{u}}{\hat{s}} \right)^{-\varepsilon}d\left( -\frac{{\hat{t}+\hat{u}}}{2\sqrt{ \hat{s} }} \right)d\hat{t}d\Omega^{1-2\varepsilon}\delta(\hat{s}+\hat{t}+\hat{u}-m_{W}^2)\tag{4.9}$$
where $d\Omega^{D-3}$ is the solid angle in $D-3$ dimensions,
$$\int d\Omega^{1-2\varepsilon}=\frac{2\pi}{\pi^{\varepsilon}\Gamma(1-\varepsilon)}\tag{4.10}.$$
It is convenient to use the two dimensionless variables $x$, $v=-\hat{t}/\hat{s}$. The phase-space integral can be expressed through them as
$$d\Phi_{Wg}=\frac{\hat{s}^{1-\varepsilon}}{16\pi^2} \frac{d\Omega^{1-2\varepsilon}}{(2\pi)^{1-2\varepsilon}}dxdv v^{-\varepsilon}(1-x-v)^{-\varepsilon}[2\pi\delta(x\hat{s}-m_{W}^{2})].\tag{4.11}$$