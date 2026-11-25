The free particle is one of the few cases where the [[Feynman Path Integral]] can be calculated explicitly. This has $V(q)=0$. Lets start from the time-sliced definition of the position space path integral and [Wick rotate](Green%20Functions) the infinitesimal times $\varepsilon\to e^{ -i\theta\varepsilon }$,
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} =\lim_{ N \to \infty } \left( \frac{m}{2\pi i\hbar\varepsilon} \right)^{\frac{N+1}{2}}\int_{-\infty}^{\infty}dq_{1}\dots \int_{-\infty}^{\infty}dq_{N}\exp\left[ \sum_{n=0}^{N} \frac{i}{\hbar} \frac{m}{2e^{-i\theta}\varepsilon}(q_{n+1}-q_{n})^2 \right],\tag{3.1}$$
where $q_{i}=q_{0}$ and $q_{f}=q_{N+1}$. The Wick rotation makes the integral Gaussian and convergent with real exponents. Start with the $q_{1}$ integral,
$$\int_{-\infty}^{\infty} dq_{1}\exp\left[ \frac{im}{\underbrace{2\hbar e^{ -i\theta }\varepsilon}_{\equiv-c}}((q_{2}-q_{1})^2+(q_{1}-q_{0})^2) \right]=\sqrt{ \frac{\pi}{2c} }e^{ -c/2 }(q_{0}-q_{2})^2\tag{3.2}$$
where all integrals can be reduced to a Gaussian with $\mathrm{Re}(c)>0$ since we Wick rotated, and $0<\theta< \frac{\pi}{2}$. Next compute the integral over $q_{2}$
$$\int_{-\infty}^{\infty}dq_{2}\exp\left[ -c\left( (q_{3}-q_{2})^2+\frac{1}{2}(q_{2}-q_{0})^2 \right) \right]=\sqrt{ \frac{2\pi}{3c} }\exp\left[ -\frac{(q_{3}-q_{0})^2c}{3} \right].\tag{3.3}.$$
A pattern starts to emerge so the integral over $q_{n}$ becomes
$$\int_{-\infty}^{\infty}dq_{n}e^{ -(q_{n+1}-q_{n})^2c }e^{ -c(q_{n}-q_{0})/n }-\sqrt{ \frac{n\pi}{(n+1)c} }\exp\left[ -\frac{(q_{n+1}-q_{0})^2c}{n+1} \right]\tag{3.4}.$$
Doing all integrals from $q_{1}$ to $q_{N}$ gives
$$\bra{q_{f}} \hat{U}(t_{f},t_{i})\ket{q_{i}} =\lim_{ N \to \infty } \left( \frac{m}{2\pi i\hbar\varepsilon} \right)^{(N+1)/2}\left( \prod_{n=1}^{N-1} \sqrt{ \frac{n\pi}{(n+1)c} } \right)\left( \frac{N\pi}{(N+1)c} \right)^{1/2}\exp\left[ -\frac{(q_{N+1}-q_{0})^2c}{N+1} \right]=\lim_{ N \to \infty } \sqrt{ \frac{m}{2\pi \hbar i\varepsilon(N+1)} }\exp\left[ i \frac{(q_{f}-q_{i})^2m}{2\hbar\varepsilon(N+1)} \right]\\=\sqrt{ \frac{m}{2\pi i\hbar(t_{f}-t_{i})} }\exp\left[ i \frac{(q_{f}-q_{i})^2m}{2\hbar(t_{f}-t_{i})} \right]\tag{3.5}$$
where we took $\theta\to 0$ and used that $\varepsilon(N+1)=t_{f}-t_{i}$ and that $\prod_{n=1}^{N-1} \sqrt{ \frac{n}{n+1} }=\sqrt{ \frac{1}{N} }$. Overall the transition amplitude is independent of $N$ so the limit disappears.

