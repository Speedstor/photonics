### Generalized Stokes' theorem
$$
\int_{\partial \Omega}\omega =\int_{\Omega} d\omega
$$

| Dimension of region | Classical name                    | Statement                                                                             | In English                     |
| ------------------- | --------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------ |
| 1 (interval)        | Fundamental theorem of calculus   | $\int^b_a f'dx=f(b)-f(a)$                                                             |                                |
| 1 (curve)           | Gradient theorem                  | $\int_C \nabla f\cdot d\mathbf{l} = f(\text{end}) - f(\text{start})$                  |                                |
| 2 (flat region)     | Green's theorem                   | $\oint_C(P\ dx+Q\ dy)=\iint(Q_x-P_y)dA$                                               |                                |
| 2 (surface in 3D)   | (Kelvin-)Stokes' theorem          | $\oint_C\mathbf{F}\cdot d\mathbf{l}=\iint_S(\nabla\times\mathbf{F})\cdot d\mathbf{S}$ |                                |
| 3 (volume)          | Divergence theorem [^other_names] | $\oiint_S\mathbf{F}\cdot d\mathbf{S} = \iiint_V \nabla\cdot\mathbf{F}\ dV$            | flux out equals sources inside |





[^other_names]:  Also called "Gauss's theorem", "Gauss-Ostrogradsky theorem"
