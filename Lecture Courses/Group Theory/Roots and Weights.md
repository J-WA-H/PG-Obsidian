We need a method to analyse the representations of arbitrary simple [[Lie Groups]], like $SU(2)$. First, we do what we always try in quantum mechanics, find the largest possible set of commuting hermitian observables and use their eigenvalues to label their states. In this case, our observables will be the largest set of hermitian generators we can find that commute with one another, and therefore be simultaneously diagonalised. 

We want the largest possible set of commuting hermitian generators because we want to diagonalise as much as possible, A subset of commuting hermitian generators which is as large as possible is called a Cartan subalgebra. 

In a particular irreducible representation, $D$, there will be a number of hermitian generators, $H_{i}$ for $i=1,\dots,m$, corresponding to the elements of the Cartan subalgebra called the Cartan generators satisfying
$$H_{i}=H_{i}^{\dagger}\qquad \text{and} \qquad [H_{i},H_{j}]=0.\tag{4.1}$$
The Cartan generators form a linear space. Thus, we can choose a basis in which they satisfy
$$\mathrm{Tr}(H_{i}H_{j})=k_{D}\delta_{ij} \text{ for } i,j=1\;\text{to } m\tag{4.2} $$
where $k$ is some constant that depends on the representation and on the normalisation of the generators. The integer $m$, the number of independent Cartan generators, is called the rank of the algebra.

Carton generators can be simultaneously diagonalised. After diagonalisation, the states of the representation $D$ can be written as $\ket{\mu,x,D}$ where
$$H_{i}\ket{\mu,x,D} =\mu_{i}\ket{\mu,x,D}\tag{4.3} $$
and $x$ is any other label that is necessary to specify the state.

The eigenvalues $\mu_{i}$ are called weights. They are real because they are eigenvalues of hermitian operators. The $m$-component vector with components $\mu_{i}$ is the weight vector.

The adjoint representation, defined by
$$[T_{a}]_{bc}=-if_{abc},\tag{4.4}$$
is important as the rows and columns of matrices are labelled by the same index that labels the generators, which means the states correspond to the generators themselves. Define an arbitrary generator $\ket{X_{a}}$. Linear combinations of these states correspond to linear combinations of the generators,
$$\alpha \ket{X_{a}} +\beta \ket{X_{b}} =\ket{\alpha X_{a}+\beta X_{b}} \tag{4.5}.$$
A convenient scalar product is
$$\braket{ X_{a} | X_{b} } =\lambda^{-1}\mathrm{Tr}(X_{a}^{\dagger}X_{b})\tag{4.6}$$
where $\lambda$ is the same as $k_{D}$.

The action of a generator on a state is
$$X_{a}\ket{X_{b}} =\ket{X_{c}} \bra{X_{c}} X_{a}\ket{X_{b}} =\ket{X_{c}} [T_{a}]_{cb} = -if_{acb}\ket{X_{c}} =if_{abc}\ket{X_{c}} =\ket{if_{abc}X_{c}} =\ket{[X_{a},X_{b}]} \tag{4.7}.$$
The roots are the weights of the adjoint representation. Because $[H_{i},H_{j}]=0$, the states corresponding to the Cartan generators have zero weight vectors
$$H_{i}\ket{H_{j}} =\ket{[H_{i},H_{j}]} =0\tag{4.8}.$$
Furthermore, all states in the adjoint representation with zero weight vectors correspond to Cartan generators. Because of $(4.2)$, the Cartan states are orthonormal. The other states of the adjoint representation, those not corresponding to the Cartan generators, have non-zero weight vectors, $\alpha$, with components $\alpha_{i}$, $H_{i}\ket{E_{\alpha}}=\alpha_{i}\ket{E_{\alpha}}$ which means that the corresponding generators satisfy
$$[H_{i},E_{\alpha}]=\alpha_{i}E_{\alpha}.\tag{4.9}$$
It will turn out that for the adjoint representation, the non-zero weights uniquely specify the corresponding states, so there is no need for another parameter. Like the $SU(2)$ raising and lowering operators, the $E_{\alpha}$ are not hermitian. They cannot be hermitian because we can take the adjoint of $(4.9)$ to get
$$[H_{i},E_{\alpha}^{\dagger}]=-\alpha_{i}E_{\alpha}^{\dagger}\tag{4.10}.$$
Thus we can take $E_{\alpha}^{\dagger}=E_{-\alpha}$. 

States corresponding to different weights must be orthogonal, because they have different eigenvalues of at least one of the Cartan generators. Thus, we can choose the normalisation of the states in the adjoint representation so that
$$\braket{ E_{\alpha} | E_{\beta} }=\lambda^{-1}\mathrm{Tr}(E_{\alpha}^{\dagger}E_{\beta})=\delta_{\alpha\beta}=\prod_{i}\delta_{\alpha_{i}\beta_{i}}\tag{4.11}.$$
The weights $\alpha_{i}$ are called roots, and the special weigh vector $\alpha$ with components $\alpha_{i}$ is the root vector.

The $E_{\pm\alpha}$ are raising and lowering operators for the weights, because the state $E_{\pm\alpha}\ket{\mu,D}$ has weight $\mu\pm\alpha$,
$$H_{i}E_{\pm\alpha}\ket{\mu,D} =[H_{i},E_{\pm\alpha}]\ket{\mu,D} +E_{\pm\alpha}H_{i}\ket{\mu,D} =(\mu\pm\alpha)_{i}E_{\pm\alpha}\ket{\mu,D}\tag{4.12}. $$
As there is no notion of positivity yet, it is irrelevant to consider which is raising and which is lowering. The above is true for any representation, but particularly important for the adjoint representation. To see why, consider the state $E_{\alpha}\ket{E_{-\alpha}}$. This has weight $\alpha-\alpha=0$, thus it is a linear combination of states corresponding to Cartan generators. This in turn implies that $[E_{\alpha},E_{-\alpha}]$ is a linear combination of Cartan generators:
$$E_{\alpha}\ket{E_{-\alpha}} =\beta_{i}\ket{H_{i}} =\ket{\beta_{i}H_{i}} =\ket{\beta \cdot H} =\ket{[E_{\alpha},E_{-\alpha}]} \tag{4.13}.$$
But we can actually compute $\beta$,
$$\beta=\bra{H_{i}} E_{\alpha}\ket{E_{-\alpha}} =\lambda^{-1}\mathrm{Tr}(H_{i}[E_{\alpha},E_{-\alpha}])=\lambda^{-1}\mathrm{Tr}(E_{-\alpha}[H_{i},E_{\alpha}])=\lambda^{-1} \alpha_{i} \mathrm{Tr}(E_{-\alpha}E_{\alpha})=\alpha_{i}\tag{4.14}.$$
Thus $[E_{\alpha},E_{-\alpha}]=\alpha \cdot H$. 

More generally, the weight $\mu$ of a representation $D$, the $E_{3}$ value is
$$E_{3}\ket{\mu,x,D} = \frac{{\alpha \cdot \mu}}{\alpha^2}\ket{\mu,x,D}.\tag{4.15} $$
