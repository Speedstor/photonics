
### 1.a Maxwell Equations
$$
\begin{aligned}
\nabla\times E + \frac{ \partial B }{ \partial t }  = 0 \\
\nabla\times H - \frac{ \partial D }{ \partial t } =J \\
\nabla \cdot D = \rho  \\
\nabla \cdot B = 0
\end{aligned}
$$

### 1.b Constitutive equations
$$
D = \varepsilon E = \varepsilon_{0}E + P\\
B = \mu H = \mu_{0}H + \mu_{0} M
$$

### 1.c Boundary Conditions
- Derived from: [[#1.a Maxwell Equations]] 
- Derived via: [[integral theorems of vector calculus|Divergence theorem]], [[integral theorems of vector calculus|Stokes theorem]]

**Normal components**: [^pillbox]
$$
B_{2n}=B_{1n} \\
D_{2n}-D_{1n}=\rho
$$
**Tangential Components**: [^loop]
$$
\mathbf{n}\times(\mathbf{E}_{2}-\mathbf{E}_{1})=0\\
\mathbf{n}\times(\mathbf{H}_{2}-\mathbf{H}_{1})=\mathbf{K}
$$






**Appendix**
- E - V/m
- H - A/m
- D - C/m<sup>2</sup>
- B - Wb/m<sup>2</sup>
- $\rho$ and $J$ - C/m<sup>3</sup> and A/m<sup>2</sup>
- $\varepsilon_0 = 8.854\times 10^{-12}$
- $\rho$ - surface charge density - C/m<sup>2</sup>
- $\mathbf{K}$ - surface current density - A/m


[^pillbox]: Derived by applying the divergence theorem to a thin pillbox straddling the interface.
	![[pillbox.png|130]]
[^loop]: Derived by applying Stokes' theorem to a loop across the surface of the interface.
	![[loop.png|130]]
