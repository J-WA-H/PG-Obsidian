*Concentrating on the case of incident protons, one could naively assume that they consist of 3 valance quarks. If they don't interact, the PDFs would be
$$\begin{matrix}
f_{u/p} (x,\mu^2)=2\delta\left( x-\frac{1}{3} \right) \\
f_{d/p} (x,\mu^2)=\delta\left( x-\frac{1}{3} \right)
\end{matrix}\tag{8.1}$$
with all other PDFs being exactly zero. This would guarantee the flavour sum rule, given by
$$\int_{0}^{1}dx[f_{u/p} (x,\mu^2)-f_{\bar{u}/p}(x,\mu^2)]=2$$
$$\int _{0}^{1}dx[f_{d/p}(x,\mu^2)-f_{\bar{d}/p}(x,\mu^2)]=1$$
$$\int_{0}^{1}dx [f_{q/p}(x,\mu^2)-f_{\bar{q}/p}(x,\mu^2)]=0\quad \text{for } q\in \{ s,c,b \}\tag{8.2}$$
and the momentum sum rule
$$\int_{0}^{1}dx \,x\sum_{i}f_{i/h}(x,\mu^2)=1\,\forall\,\mu^2\text{ and all hadrons }h\tag{8.3}$$
where $i$ runs over all partons $\{ u,\bar{u},d,\bar{d},\dots,g \}$.
Switching on elastic interactions between the quarks, but still neglecting any emission of additional quanta, would not change this picture dramatically. The only effect of such a form of interaction would be to smear out the sharp peak at $x=\frac{1}{3}$ and replace it with a probability density such that its expectation value would be $\frac{1}{3}$,
$$\left\langle \left.  x\right|_{f_{u,d/p}(x,\mu^2)}  \right\rangle=\frac{1}{3}\tag{8.4}.$$
A drastic change occurs when the emission of quanta without their immediate reabsorption is considered. These sea partons would have a finite lifetime that increases with decreasing momentum fraction $x$. This leads to these sea partons typically having larger probability distributions at small rather than at large values of $x$. In fact, it is worth analysing the kinematics of parton emission as described by the QCD analogue of the splitting functions. They will lead to gluon emissions off valence quarks typically taking place for values of $z$ close to $1$, i.e. for small momentum fractions $(1-z)$ of the gluon with respect to the quark. As sea quarks as well as additional gluons emitted by these gluons inherit their kinematics, the perturbative production of sea partons favours them to have small values of $x$. Consequently, the combination of lifetime arguments and the form of the splitting functions induces non-zero sea PDFs, which typically steeply increase for decreasing $x$. Naively, and to a fairly good approximation,
$$f_{sea/p}(x,\mu^2)\propto x^{-\lambda}\tag{8.5}$$
where $\lambda \approx 1$ for gluons and sea quarks, and $\lambda \approx-\frac{1}{2}$ for valance quarks. This behaviour is contrasted with the cases of no or elastic interactions in a sketchy way as shown in the figure
![[Pasted image 20261105163804.png|416]]

Apart from the increase for small $x$ due to the sea partons, it is worth noting that also the distribution of valence partons, which for elastic interactions is centred around $x\approx \frac{1}{3}$, shifts towards smaller $x$ values of about $0.1$ and broadens out. This is due to them losing energy due to the emission of sea partons. And in fact, while the PDF for an up quark is taken at relatively low scales of $\mu_{F}=10\text{ GeV}$, this slight valance bump at $x\approx0.1$ persists also to higher scales. This picture of secondary parton radiation indeed is very similar to the case of photons emitted by an electron. There, the photons play the role of the sea, allowing the photons to split into electron-positron pairs supplements this sea with additional fermions.

Putting this together yields a picture of the proton in the $x$-$Q^2$ plane as shown below.
![[Pasted image 20261105164848.png|426]]

The behaviour of the PDFs is entirely calculable with perturbative methods, and is given by the [DGLAP](Deep%20Inelastic%20Scattering.md) equation for QED, with the starting condition
$$f_{e/e}(x,0)=\delta(1-x)\text{ and }f_{\gamma/e}(x,0)=0\tag{8.6}.$$
In contrast to this fully known QED case, the QCD case is more complicated due to the non-perturbative infrared structure of the theory. There, the perturbative regime is bound from below, typically it is assumed that perturbative QCD breaks down for scales of $\mathcal{O}(1\text{ GeV})$ and below. This implies that the starting conditions for a DGLAP evolution must be taken from data. A consequence of this scaling behaviour is that for increasing normalisation scales $\mu$ the sea contribution is logarithmically increasing, a phenomenon known as scaling violation. Pictorially speaking, the probability of finding a parton within a parton increases by probing with larger transverse resolution power, as provided by the scale. In this respect, partons are not elementary objects. Rather they are objects that carry the quantum numbers of the fundamental fields of QCD, quarks and gluons, but they cannot be interpreted as naked particles at all scales. In other words, partons are non-elementary particles, with a complicated internal structure but behave like fundamental quanta when probed at a low enough scale. In this respect, partons are very similar to the colliding electron of the electromagnetic analogy, which is a superposition of various Fock states involving secondary quanta.