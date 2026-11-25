When dealing with the action, we have to deal with functionals. Functionals map functions to numbers. Functional derivatives tell us how the functional changes when a small change in the input function is made. We define a functional derivative as
$$\frac{\delta F[J]}{\delta J(s)}=\lim_{ \varepsilon \to 0 } \frac{{F[J(t)+\varepsilon\delta(t-s)]-F[J(t)]}}{\varepsilon}\tag{2.1}.$$
If $F[J]=J(t)$ then
$$\frac{\delta F[J]}{\delta J(s)}=\delta(t-s)\tag{2.2}.$$
Similarly, we can also write an infinitesimal variation of the functional as
$$\delta F[J]=\int ds\,\delta J(s) \frac{\delta F[J]}{\delta J(s)}\tag{2.3}$$
or equivalently we can expand $F[J+\delta J]-F[J]$ to leading order in $\delta J$. 

So far the [[Feynman Path Integral]] has focused on one observable, the transition amplitude. But it is also useful to ask more refined questions, like making measurements for observables, e.g. $\hat{q}$ at different times $\bra{q_{f}}\hat{U}(t_{f},t)\hat{q}\hat{U}(t,t_{i})\ket{q_{i}}$. This equation amounts to starting with a state $\ket{q_{i}}$ at $t_{i}$, then at time $t$ you measure the value of the operator $\hat{q}$ and at $t_{f}$ compute the overlap of your state with $\bra{q_{f}}$. The derivation of the path integral by time slicing goes through, except now we get a $q(t)$ as a result of $\hat{q}$ acting on the complete set of states we introduce at time $t$. We can then write this correlation function as a path integral
$$\bra{q_{f}} \hat{U}(t_{f},t)\hat{q}\hat{U}(t,t_{i})\ket{q_{i}}=\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}}\mathcal{D}'q\mathcal{D}p\,q(t)\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right].\tag{2.4} $$
Exactly the same goes through with more insertions of $\hat{q}$ at different intermediate times
$$\bra{q_{f}} \hat{U}(t_{f},t_{N})\hat{q}\hat{U}(t_{N},t_{N-1})\hat{q}\hat{U}(t_{N-1},t_{N-2})\dots \hat{U}(t_{2},t_{1})\hat{q}U(t_{1},t)\ket{q_{i}} = \bra{q,t_{f}} \hat{q}(t_{N})\dots \hat{q}(t_{1})\ket{q_{i},t_{i}} =\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}} \mathcal{D}'q \mathcal{D}p q(t_1)\dots \hat{q}(t_{N})\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right].\tag{2.5}$$
Here the instantaneous eigenstates of the Heisenberg picture position operator $\ket{q,t}$ are defined as $\hat{q}(t)\ket{q,t}=q\ket{q,t}$. We also changed from the time independent operators $\hat{q}$ to the Heisenberg operators that depend on time $\hat{q}(t)$ as indicated by the fact that they have a time dependence.

Now we note that on the left hand side of $(2.5)$ the times are all ordered, $t_{f}>t_{n}>\dots>t_{1}>t_{i}$ but the right-hand side in the second line does not care, as these are all functions not operators. If we take two times out of order, e.g. $t_{1}>t_{2}$ we end up computing the integral with $\hat{q}(t_{1})$ and $\hat{q}(t_{2})$ interchanged. You can easily see this by computing both of the correlators $\bra{q_{f},t_{f}}\hat{q}(t_{2})\hat{q}(t_{1})\ket{q_{i},t_{i}}$ and $\bra{q_{f},t_{i}}\hat{q}(t_{1})\hat{q}(t_{2})\ket{q_{i},t_{i}}$, where that $t_{2}>t_{1}$ in the first equation, and that $t_{1}>t_{2}$ in the second, and noticing they both produce
$$\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}}\mathcal{D}'q\mathcal{D}p\, q(t_{1})q(t_{2})\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right]\tag{2.6}.$$
In other words, we can write the following equation,
$$\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}}\mathcal{D}'q\mathcal{D}p\, q(t_{1})q(t_{2})\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right]=\begin{cases}
\bra{q_{f},t_{f}}\hat{q}(t_{2})\hat{q}(t_{1})\ket{q_{i},t_{i}}, & \text{if } t_{2}>t_{1} \\
\bra{q_{f},t_{i}}\hat{q}(t_{1})\hat{q}(t_{2})\ket{q_{i},t_{i}} & \text{if } t_{1}>t_{2}
\end{cases}.\tag{2.7}$$
We can write the RHS more economically by using the time-ordered product
$$\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}}\mathcal{D}'q\mathcal{D}p\, q(t_{1})q(t_{2})\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right] = \bra{q_{f},t_{f}}T[\hat{q}(t_{2})\hat{q}(t_{1})]\ket{q_{i},t_{i}}  \tag{2.8}.$$
This holds for more than two operator insertions, which means the path integral always computes time-ordered correlators,
$$\int_{q(t_{i})=q_{i}\\q(t_{f})=q_{f}}\mathcal{D}'q\mathcal{D}p\, q(t_{1})\dots q(t_{n})\exp\left[ -\frac{i}{\hbar}\int_{t_{i}}^{t_{f}}(H(q,p)-p\dot{q})dt \right]=\bra{q_{f},t_{f}} T[\hat{q}(t_{n})\dots \hat{q}(t_{i})]\ket{q_{i},t_{i}} \tag{2.6}.$$
The time ordered product moves later times left. This expands the observables we can compute with the path integral.

Say we want to study an evolution where we prepared a given state in the infinite past, and want to measure the overlap with some state in the infinite future, after putting various operator insertions at intermediate times denoted by the $\dots$ below
$$\lim_{ t_{i} \to -\infty \\t_{f}\to+ \infty}\bra{\chi} e^{ -i\hat{H}t_{f}/\hbar\dots } \newcommand{\sumint}{\mathop{\rlap{\kern.5em\int}\sum}} \sumint \ket{E}e^{ -iEt_{i}/\hbar }\braket{ E | \psi }   \tag{2.7}  .$$
This assumes a time-independent Hamiltonian. We have used another complete basis, this time of energy eigenstates $\hat{H}\ket{E}=E\ket{E}$, and use them to write a resolution of the identity. Note that the sum holds if we have a discrete energy spectrum, otherwise we should replace the sum with an integral which is what the symbol $\sumint$ reinforces. This type of measurement is closer to what one would measure in an experiment in particle physics where one would prepare an "in" state in the infinite past (far from all interactions) with a definite number of particles in a given state, and measure the transition amplitude for a given "out" state in the infinite future, perhaps inserting operators to compute the matrix element of some time-ordered product. 

As $t_{i}\to \infty$, the phase $e^{ iEt_{i}/\hbar }$ is highly oscillatory unless $E=0$. To analyse this, we move to Euclidean time by doing a Wick rotation. We can analytically continue time to the complex plane
$$t\to e^{ -i\theta }t,\qquad \text{with }\theta \in \left[ 0, \frac{\pi}{2} \right]\tag{2.8}$$
when $\theta=0$ we are back where we started in Minkowski time, but when we go to $\theta=\frac{\pi}{2}$ we go to Euclidean time, i.e. $t\to-it_{E}$. It will often be convenient to Wick rotate to Euclidean time, do our computations there, where things are convergent and better defined, and then rotate back. This in the correlation function looks like
$$\lim_{ t_{i} \to -\infty \\ t_{f}\to +\infty} \bra{\chi} \exp\left[ -\frac{\hat{H}}{\hbar}(it_{f}\cos \theta+t_{f}\sin \theta)\dots \right]\sumint \ket{E} \exp\left[ \frac{E}{\hbar}(it_{i}\cos \theta+t_{i}\sin \theta) \right]\braket{ E | \psi } \tag{2.9} $$
and we see that when $\theta=\frac{\pi}{2}$ states are weighted by $e^{ Et_{i}/\hbar }$, and so when we take $t_{i}\to-\infty$ only the ground state, survives. Here we assume there exists a unique ground state $\ket{0}$ that is separated by a gap from the other states. We can do the same for $t_{f}\to+\infty$ by inserting a complete set of states there as well and we get
$$\lim_{ t_{i} \to -\infty \\ t_{f}\to +\infty} \braket{ \chi | E }  \exp\left[ -\frac{\hat{H}}{\hbar}(it_{f}\cos \theta+t_{f}\sin \theta)\right]\bra{E} \dots\sumint \ket{E} \exp\left[ \frac{E}{\hbar}(it_{i}\cos \theta+t_{i}\sin \theta) \right]\braket{ E | \psi } \tag{2.9} = \braket{ \chi | 0 } \bra{0} \dots \ket{0} \braket{ 0 | \psi } $$
and we see the details of the initial and final state are just captured in an overall normalisation. In other words, if we want to know the expectation value of any time-ordered product of operators (or just the amplitude itself) between an initial state $\ket{\psi}$ at $t_{i}=-\infty$ and a final state $\bra{\chi}$ at $t_{f}=+\infty$ the fundamental object we need to compute is the vacuum expectation value appearing in the middle of the last expression.

It is natural to now define the $N$-point Green function (meaning we have $N$ insertions of the position operator) as
$$G(t_{1},\dots,t_{N})= \bra{0} T(\hat{q}(t_{1})\dots \hat{q}(t_{N}))\ket{0} .\tag{2.10}$$
This is now an expectation value of $T(\hat{q}(t_{1})\dots \hat{q}(t_{N}))$ in the ground state, and it captures how position measurements at different times are correlated - these are correlation functions. Using the above discussion we have that this is obtained by taking the initial and final times to $\pm \infty$ with any other initial and final states, provided they have non-zero overlap with $\ket{0}$, i.e. $\braket{ \chi | 0 }\neq 0$ and $\braket{ 0 | \psi }\neq 0$. They will only differ by an overall normalisation, which means the Green function can be defined as a path integral (note we are back in Minkowski time)
$$G(t_{1},\dots,t_{N})=\mathcal{N}\int \mathcal{D}'q\mathcal{D}p\,q(t_{1})\dots q(t_{n})\exp\left[ -\frac{i}{\hbar}\int_{-\infty}^{\infty}(H(q,p)-p\dot{q})dt \right]\tag{2.11}$$
where the only thing to do is to fix the normalisation scale such that we capture the Green function and remove any reference to the particular initial and final states we considered. This is easy to do since $\braket{ 0 | 0 }=1$ we can compute the zero-point Green amplitude to get the normalisation
$$\mathcal{N}^{-1}=\int \mathcal{D}'q\mathcal{D}p\exp\left[ -\frac{i}{\hbar}\int_{-\infty}^{\infty}(H(q,p)-p\dot{q})dt \right].\tag{2.12}$$
This finally leads to the path integral formula for the Green function
$$G(t_{1},\dots,t_{N})= \frac{{\int \mathcal{D}'q\mathcal{D}p\,q(t_{1})\dots q(t_{n})\exp\left[ -\frac{i}{\hbar}\int_{-\infty}^{\infty}(H(q,p)-p\dot{q})dt \right]}}{\int \mathcal{D}'q\mathcal{D}p\exp \left[ -\frac{i}{\hbar}\int_{-\infty}^{\infty}(H(q,p)-p\dot{q})dt \right]}\tag{2.13}$$
which measures how the measurements of $\hat{q}$ at different times are correlated. Note that we have not fixed any particular boundary condition on $q(t)$ as long as we take the same boundary condition in the numerator and the denominator since the boundary conditions only contribute with an overall normalisation.

Noting that in a Wick rotation $t\to -it_{E}$ and $\dot{q}=\frac{dq}{dt}\to i \frac{dq}{dt_{E}}$, and
$$i\int_{t_{i}}^{t_{f}}dt\left( \frac{1}{2}m\dot{q}^2-V(q) \right)\to-\int_{t_{E_{1}}}^{t_{E_{2}}}dt_{E}\left( \frac{1}{2}m\left( \frac{dq}{dt_{E}} \right)^2+V(q) \right)\tag{2.14}.$$
This gives the Euclidean path integral
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} =\int \mathcal{D}q\exp\left[ -\frac{1}{\hbar}\int_{t_{E_{1}}}^{t_{E_{2}}}dt_{E}\left( \frac{1}{2}m\left( \frac{dq}{dt_{E}} \right)^{2}+V(q) \right) \right]\tag{2.15}$$
where the weight is now a real exponential, which makes things convergent.

