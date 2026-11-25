The path integral is an alternative way to quantise fields, for example QCD. This approach allows for time and space to be treated in equal footing, which preserves Lorentz invariance. Consider a one-dimensional spacetime, which one point like non-relativistic quantum particle propagating in time, $q(t)$. This is the starting point to consider fields. The transition can be made easier by thinking about having a system of $N$ particles in a lattice with lattice spacing $\ell$, $q_{n=1,\dots,N}(t)$. If you take $N\to \infty$ and view the system from very far away so the lattice spacing goes to zero, you can describe the system by replacing the discrete label by a continuous coordinate, you get a space dimension $q_{a}(t)\to \phi(t,x)$.

Note the time evolution operator is
$$\hat{U}(t_{f},t_{i})=\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}dt\hat{H}(t) \right]\tag{1.1}$$
With the path integral the aim is to compute the transition amplitude
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} ,\quad \text{with } t_{f}>t_{i} \tag{1.2}.$$
The absolute value squared of this amplitude gives the probability of finding the particle in an eigenstate with eigenvalue $q_{f}$ at the final time $t_{f}$, given that it started in an eigenstate with eigenvalue $q_{i}$ at the initial time $t_{i}$. Imagine we want to compute the amplitude for some state $\ket{\psi_{i}}$ at time $t_{i}$ to evolve to a state $\bra{\psi_{f}}$ at time $t_{f}>t_{i}$
$$\bra{\psi_{f}} \hat{U}(t_{f},t_{i})\ket{\psi_{i}} =\int_{-\infty}^{\infty}dq_{i}dq_{f}\underbrace{\braket{ \psi_{f} | q_{f} }}_{\psi^{*}(q_{f})} \bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} \underbrace{\braket{ q_{i} | \psi_{i} } }_{\psi(q_{i})}\tag{1.3}$$
The transition amplitude then captures the dynamics of the system, and can be computed using the path integral.

In QM to find the amplitude of a given outcome we have to sum over all ways a process can take place - the superposition principle. Consider the double slit experiment where you have a source of identical particles hitting a screen with two slits and other screen a distance from that where a detector measures how many electrons arrive at a given position $\mathcal{O}$ on the screen
![[Pasted image 20261108151704.png|369]]

The total amplitude for detection of a particle at a given point is given by the sum of the amplitudes for the particle to go through each of the two slits, which we will label as path $P_{1},P_{2}$ respectively,
$$\mathcal{A}(\text{observation at point }x)=\sum_{P=P_{1},P_{2}}\mathcal{A}(\text{taking path }P)\tag{1.4}.$$
These two paths have different lengths so the individual amplitudes are difference and there is interference between the two.

Feynman made a thought experiment where more slits were drilled into the screen, the above amplitude changes by adding a term in the sum for each new path you allow. Imagine now that there are so many slits that the whole screen disappears, you end up adding together paths specified by the position at which the electron passes through the nonexistent screen. Similarly, you can add more screens with many slits, you now have to sum over all different paths.
![[Pasted image 20261108152534.png|416]]

As we take the limit of infinite screens and slits, you end up summing, or rather integrating over all paths the electron can take between the source and the observation point. This is the defining notion of a path integral. The screens with slits give a discretisation of the path, and as you add more you are refining the path of the electron, like when you compute integrals.
![[Pasted image 20261108152746.png|445]]

Consider the time operator with a time independent Hamiltonian,
$$\hat{U}(t_{1},t_{2})=e^{ -i\hat{H}(t_{1}-t_{2})/\hbar }\tag{1.5}.$$
Following the picture of a path integral we want to descretise the particle's path and sum over all paths, so we start slicing time in infinitesimal steps. Recall causality that tells you $\hat{U}(t_{2},t_{3})\hat{U}(t_{3},t_{4})=\hat{U}(t_{2},t_{4})\tag{1.6}$ which is obvious for the time independent Hamiltonian. Then we can write
$$\bra{q_{f}}\hat{U}(t_{f},t_{i})\ket{q_{i}} =\bra{q_{f}} \hat{U}(t_{f},t_{N})\underbrace{\dots \hat{U}(t_{2},t_{1})}_{N-1} \hat{U}(t_{1},t_{i})\ket{q_{i}} \tag{1.6}$$
where we take the time steps to be $\varepsilon$.
$$t_{n}-t_{n-1}=\varepsilon=\frac{{t_{f}-t_{i}}}{N+1}>0.\tag{1.7}$$
Next insert a complete set of states
$$\int_{-\infty}^{\infty}dq_{n}\ket{q_{n}} \bra{q_{n}} =1,\qquad n=1,\dots,N\tag{1.8},$$
in between each pair of $\hat{U}$:
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} =\int_{-\infty}^{\infty}\left[ \prod_{n=1}^{N}dq_{n} \right]\bra{q_{f}} \hat{U}(t_{f},t_{N})\ket{q_{N}} \underbrace{\bra{q_{N}} \dots \ket{q_{2}} \bra{q_{1}} \hat{U}(t_{2},t_{1})\ket{p_{1}} }_{N-1}\bra{q_{i}} \hat{U}(t_{1},t_{i})\ket{q_{i}} \tag{1.9}.$$
Here we have time sliced the path of the particle, and are approximating the path by a sequence of infinitesimal time evolutions in between each consecutive times $t_{n},t_{n+1}$. At each time slice $t_{n}$ we integrate over all $q_{n}$, meaning we integrate over all possible particle positions.#
![[Pasted image 20261108155015.png|411]]

This way we generate all different trajectories - we are thus creating the path integral. This is doing what we expected, except that there we are picturing the motion of a particle in two dimensions and here we only have one. Apart from suppressing one of the dimensions, we are also doing a finer specification of the motion by specifying the time at which it passes through each point in space. In the end we need to compute the infinitesimal amplitude
$$\bra{q_{N+1}} \hat{U}(t_{n+1}=t_{n}+\varepsilon,t_{n})\ket{q_{n}} =\bra{q_{n+1}}e^{ -i\hat{H}\varepsilon/\hbar }\ket{q_{n}}\tag{1.10} . $$
We will assume the Hamiltonian takes a standard form with the kinetic term $T(\hat{p})$ depending only on momentum and the potential term $V(\hat{q})$ only on the position, $\hat{H}=T(\hat{p})+V(\hat{q})$.

Now we will use the Campbell-Baker-Hausdorf formula to split the exponentials as
$$\exp\left[ -i \frac{{T(\hat{p})+V(\hat{q})}}{\hbar}\varepsilon \right]=\exp\left[  -i\frac{T(\hat{p})}{\hbar}\varepsilon \right]\exp\left[ -i \frac{V(\hat{q})}{\hbar}\varepsilon \right]\exp\left[ \frac{\varepsilon^2[T(\hat{p}),V(\hat{q})]}{2\hbar^2} \right]\tag{1.11},$$
since we will take $\varepsilon$ to zero in the end we will ignore the sub-leading terms. We now have two exponentials to act on our states, since the kinetic terms depend on $\hat{p}$ we introduce once more a complete set of states, this time momentum eigenstates.
$$\bra{q_{n+1}} \hat{U}(t_{n+1}=t_{n}+\varepsilon,t_{n})\ket{q_{n}} =\int_{-\infty}^{\infty}dp_{n+1}\braket{ q_{n+1} | p_{n+1} } \bra{p_{n+1}} e^{ -iT(\hat{p})\varepsilon/\hbar }e^{ -iV(\hat{q})\varepsilon/\hbar } \ket{q_{n}} $$
$$=\int_{-\infty}^{\infty}dp_{n+1}\underbrace{\braket{ q_{n+q} | p_{n+1} } }_{\frac{\exp\left( \frac{i}{\hbar}q_{n+1}p_{n+1} \right)}{\sqrt{ 2\pi \hbar }}} \underbrace{\braket{ p_{n+1} | q_{n} }}_{\frac{\exp\left( -\frac{i}{\hbar}q_{n}p_{n+1} \right)}{\sqrt{ 2\pi \hbar }}} e^{ -i T(p_{n+1})\varepsilon/\hbar }e^{ -iV(q_{n})\varepsilon/\hbar }=\int_{-\infty}^{\infty} \frac{dp_{n+1}}{2\pi \hbar} e^{ -i\varepsilon/\hbar \overbrace{(T(p_{n+1})+V(q_{n}))}^{H(q_{n},p_{n+1})}+i\frac{\varepsilon}{\hbar}p_{n+1} (q_{n+1}-q_{n})/\varepsilon}\tag{1.12}$$
where we acted with the kinetic part of the Hamiltonian on the momentum eigenstate, and the potential part of the position eigenstate. Finally the overlap between position and momentum eigenstates is computed using
$$\braket{ p | q } =\frac{1}{\sqrt{ 2\pi \hbar }}e^{ -ipq/\hbar }\tag{1.13}.$$
We now plug back into the full time-sliced amplitude $(1.9)$ where we define $q_{0}=q_{i}$ and$q_{N+1}=q_{f}$
$$\bra{q_{f}}\hat{U}(t_{f},t_{i})\ket{q_{i}} =\int_{-\infty}^{\infty}  \underbrace{\left[\prod_{n=1}^{N}dq_{n} \right] \left[ \prod_{n=1}^{N+1} \frac{dp_{n}}{2\pi \hbar} \right]}_{:= \mathcal{D}'q\mathcal{D}p\text{ as } N\to \infty} \exp\left[ \sum_{n=0}^{N} -\frac{iH(q_{n},p_{n+1})}{\hbar}\varepsilon + \frac{i\varepsilon}{\hbar} \frac{{q_{n+1}-q_{n}}}{\varepsilon}p_{n+1} \right]\tag{1.14}.$$
We now take $N\to \infty$ (and thus $\varepsilon\to 0$) to get the Feynman path integral in phase space (meaning we are integrating over $p$ and $q$ as opposed to the configuration space path integral). In this limit we define a measure $\mathcal{D}'q\mathcal{D}p$, with the prime reminding us there is one less $q$ integral than $p$, and we find
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} =\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}} \mathcal{D}'q \mathcal{D}p \,\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right]\tag{1.15}$$
where the limit remind you that we integrate over all paths in phase space that have $q(t_{i})=q_{i}$ and $q(t_{f})=q_{f}$, with $p(t_{i})$ and $p(t_{f})$ arbitrary. Note that all paths $p(t),q(t)$ contribute. This means that they are not constrained by the equations of motion of classical Hamiltonian dynamics, in particular this implies $H(q,p)$ is not constant in time. It is worth pointing out that if we had started with a more general Hamiltonian where $\hat{p},\hat{q}$ dependence were not separate, there will be ordering ambiguities since $\hat{p},\hat{q}$ do not commute.

In the classical limit, $\hbar\to 0$ we recover the Euler-Lagrange equations.

We can do the integrals over momentum to get a position space integral. To do this we assume the standard kinetic term
$$T(\hat{p})=\frac{\hat{p}^2}{2m}\tag{1.16}$$
which makes the integral a Gaussian,
$$\int_{-\infty}^{\infty} \frac{dp_{n+1}}{2\pi \hbar}\exp\left[ -\frac{i\varepsilon}{\hbar}\left( \frac{p^2_{n+1}}{2m}+V(q_{n})-p_{n+1} \frac{{q_{n+1}-q_{n}}}{\varepsilon} \right) \right]=\int_{-\infty}^{\infty} \frac{dp'_{n+1}}{2\pi \hbar}\exp\left[ \frac{(p'_{n+1})^2}{2m}+V(q_{n})-m \frac{(q_{n+1}-q_{n})^2}{2\varepsilon^2} \right]=\sqrt{ \frac{m}{2\pi i\hbar\varepsilon} }\exp\left[ -\frac{i\varepsilon}{\hbar}\left( V(q_{n})-\frac{m(q_{n+1}-q_{n})^2}{2\varepsilon^2} \right) \right]\tag{1.17}$$
where we completed the squares by changing variables to $p'_{n+1}=p_{n+1}-\frac{{q_{n+1}-q_{n}}}{\varepsilon}m$ and performed a Gaussian Integral. From this we obtain
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} =\int_{-\infty}^{\infty}\underbrace{\left[ \prod_{n=1}^{N}dq_{n}\sqrt{ \frac{m}{2\pi i\hbar\varepsilon} } \right]\sqrt{ \frac{m}{2\pi i\hbar\varepsilon} }}_{:=\mathcal{D}q\text{ as }N\to \infty}\exp\left[ \sum_{n=0}^{N} \frac{i\varepsilon}{\hbar}\left( \frac{m}{2}\left( \frac{{q_{n+1}-q_{n}}}{\varepsilon} \right)^2-V(q_{n}) \right) \right]\tag{1.18}$$
where we recognise he exponent as the action $S[q]$ as we take $N\to \infty$, $\varepsilon\to 0$ and the sum becomes an integral,
$$S[q]=\int_{t_{i}}^{t_{f}}dtL(q,\dot{q})=\int_{t_{i}}^{t_{f}}dt\left( \frac{m}{2}\dot{q}^2-V(q) \right)\tag{1.19}.$$
We finally obtain the Feynman path integral in configuration space
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}}= \int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}} \mathcal{D}q\,\exp\left[ \frac{i}{\hbar}S[q] \right]\tag{1.20}. $$
We obtained the path integral as a weighted sum over all particle trajectories, There are a few path integrals we can compute explicitly, however for most physically interesting problems we will have to develop some sort of perturbation theory of the few models we can solve. This can be a perturbation theory you can solve exactly, or around the classical limit.