It can be quite tedious to calculate all [[Green Functions]] so it can be useful to, while computing moments of a Gaussian integral ($\int x^k\exp(-x^2)$) it is useful to define a generating function. 
The trick we can use to only have to evaluate one integral for all $k$,
$$\frac{d^k}{dJ^k}\left( \int_{-\infty}^{\infty}dx e^{ -ax^2+Jx } \right)=\int_{-\infty}^{\infty}dx\,x^{k}e^{ -ax^2 }\tag{5.1}$$
so we note that if you take derivatives with respect to $J$ of the integral above and then set $J=0$ we generate integrals of moments of the Gaussian. So all we have to do is compute the integral on the LHS, which can easily be done by completing the square,
$$I(J)=\int_{-\infty}^{\infty}dx e^{ -ax^2+Jx }=\sqrt{ \frac{\pi}{a} }e^{ J^2/(4a) }\tag{5.2}.$$
And now $I(J)$ is the generating function. The result for $I(J)$ can be generalised to higher dimensions
$$\int dx_{1}\dots dx_{n} \exp[-x^iA_{ij}x^{j}+J_{i}x^{i}]=\sqrt{ \frac{\pi^n}{\det A} }\exp\left[ \frac{1}{4}J_{i}(A^{-1})^{ij}J_{j} \right]\tag{5.3}$$
where $i,j=1,\dots,n$ and $A$ is a matrix while $J,x$ are vectors.

This can help in calculating Green Functions. Just like for Gaussian integrals, we can define a generating functional for Green functions
$$Z[J]\equiv 1+\sum_{N=1}^{\infty} \frac{1}{N!} \int_{-\infty}^{\infty}ds_{1}\dots ds_{N}G(s_{1},\dots,s_{N})J(s_{1})\dots J(s_{N})\tag{5.4}$$
where we call $J$ an external source - it is fixed as opposed to the fields in the path integral we integrate over. We then have that we can get any Green function as
$$G(s_{1},\dots,s_{N})= \left. \frac{\delta^NZ[J]}{\delta J(s_{1})\dots\delta J(s_{N})} \right|_{J=0},\tag{5.5}$$
where by taking $N$ derivatives all terms with less than $N$ $J(s_{i})$ disappear, and by setting $J=0$ all terms with more than $N$ $J(s_i)$ got to zero.

We had written the Green function as a path integral which if we assume the standard quadratic term $T(\hat{p})=\frac{\hat{p}^2}{2m}$ becomes
$$G(t_{1},\dots,t_{N})=\mathcal{N}\int \mathcal{D}q\,q(t_{1})\dots q(t_{N})e^{ iS[q]/\hbar }, \quad \mathcal{N}^{-1}=\int \mathcal{D}q e^{ iS[q]/\hbar }\tag{5.6}.$$
So finally we can write the generating function $Z[J]$ as a path integral
$$Z[J]=\underbrace{\mathcal{N}\int \mathcal{D}q e^{ iS[q]/\hbar }}_{=1} +\mathcal{N}\int \mathcal{D}q \sum_{N=1}^{\infty} \frac{1}{N!} \int_{-\infty}^{\infty}ds_{1}\dots ds_{N}J(s_{1})\dots J(s_{N})q(s_{1})\dots q(s_{N})e^{ iS[q]/\hbar }\\ = \mathcal{N}\int \mathcal{D}q e^{ iS{q}/\hbar }\left[ 1+\sum_{n=1}^{\infty} \frac{1}{N!}\left( \int_{-\infty}^{\infty}dsJ(s)q(s) \right)^{N} \right]=\mathcal{N}\int \mathcal{D}q \exp\left[ \frac{i}{\hbar}S[q]+ \int_{-\infty}^{\infty}dt\,q(t)J(t) \right]\tag{5.7}.$$
We now see again how $Z[J]$ acts as a generating functional: taking functional derivatives of $Z[J]$ with respect to $J(s)$ amounts to inserting $q(s)$ inside the path integral
$$\frac{{\delta Z[J]}}{\delta J(s)}=\mathcal{N}\int \mathcal{D}q \frac{\delta}{\delta J(s)}\exp\left[ \frac{i}{\hbar}S{[q]}+\int_{-\infty}^{\infty}dt\,q(t)J(t)  \right]\tag{5.8} = \mathcal{N} \int \mathcal{D}q\, q(s)\exp\left[ \frac{i}{\hbar}S[q]+\int_{-\infty}^{\infty}dt\,q(t)J(t) \right].$$
Note that if we compute the transition amplitude adding the source term, i.e. sending $S\to S+\frac{\hbar}{i}\int_{-\infty}^{\infty}q(t)J(t)$ we can get the generating functional from the modified transition amplitude as
$$\lim_{ t_{f} \to \infty \\t_{i}\to-\infty } \frac{\braket{ q_{f},t_{f} | q_{i},t_{i} }}{\braket{ q_{f} | 0 } \braket{ 0 | q_{i} } },\quad \text{with }S\to S+\frac{\hbar}{i}\int ^{\infty}_{-\infty}dt\,q(t)J(t).\tag{5.9} $$
This can be evaluated via Gaussians for the harmonic oscillator to give
$$Z[J]=\exp\left[ \frac{1}{2}\int_{-\infty}^{\infty}dt_{1}dt_{2} J(t_{1})G(t_{1},t_{2})J(t_{2}) \right]\tag{5.10}$$
where $G(t_{1},t_{2})$ obeys
$$-\frac{im}{\hbar}\left( \omega^2 + \frac{d^2}{dt^2} \right)G(t,s)+\delta(t-s)=0\tag{5.11}.$$
