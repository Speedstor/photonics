# More solutions to the wave equation
> Other than the wavefunction, what other functions satisfy the wave equation? I know a sum of wavefunctions of different frequency is valid, but what more?

In one dimension the complete answer is d'Alembert's: every solution of ∂²u/∂t² = c² ∂²u/∂x² has the form

u(x, t) = f(x − ct) + g(x + ct)

for _any_ twice-differentiable functions f and g. The sinusoids are just one choice of f. A Gaussian pulse exp(−(x − ct)²/σ²) works, a triangular bump works, a sawtooth works, a single smooth hump of any shape works — the equation only says "whatever shape you start with slides rigidly left or right at speed c." The sum of sinusoids you already know is really a special case of this: the Fourier integral ∫A(k)e^{ik(x−ct)}dk is just one way of writing a general f(x − ct). So in 1D, "superposition of frequencies" and "arbitrary traveling shape" are the same statement in two languages.

If you relax to weak (distributional) solutions, f and g don't even need to be differentiable: step functions, kinks, and delta spikes propagate perfectly well, which is how shocks and sharp wavefronts are modeled.

In three dimensions the picture is richer, because there is no longer a single "shape slides along" formula, but you still get large families beyond sinusoids:

- Plane waves f(n̂·x − ct) for any direction n̂ and any profile f.
- Spherical waves f(r − ct)/r and g(r + ct)/r — the 1/r factor is what makes an arbitrary radial profile work in 3D. (Cylindrical waves can't be written this cleanly; they involve Bessel functions and leave a wake.)
- Standing waves: any product of a spatial eigenfunction of the Laplacian (sines, spherical harmonics times spherical Bessel functions, etc.) with cos(ωt) or sin(ωt).
- Polynomial solutions like x² + c²t², xt, or x³ + 3c²xt² — anything satisfying the equation algebraically, which shows solutions need not be oscillatory or even bounded.
- Kirchhoff's formula gives the general solution: pick any initial displacement and initial velocity profile you like, and the formula produces a valid u(x, t). Every solution arises this way, so the solution space is as large as the space of initial-data pairs.

A useful way to think about it: the wave equation is linear and homogeneous, so the solutions form a vector space, and the sinusoids are one convenient basis for it. Everything else is a linear combination of them in principle, but "linear combination" includes continuous integrals over frequency and direction, which is enough to build any shape at all. The real constraint isn't on the form of the function, it's on the dispersion relation: every Fourier component must satisfy ω = c|k|. If you instead had ω depending on k some other way (as in the Schrödinger equation or water waves), shapes would spread out as they travel, and the "any profile slides rigidly" property would be lost.



# d'Alembert's formula in wave equations
> d'Alembert's formula is only describing the solution for the 1d wave equation, it doesn't generalize anything else right?

Mostly right about the _formula_, but not about the _idea_. The explicit expression

$u(x,t) = ½[f(x+ct) + f(x−ct)] + (1/2c) ∫_{x−ct}^{x+ct} g(s) ds$

is specific to the 1D wave equation on the whole line with constant speed. It depends on the fact that in one dimension the operator factors as (∂_t − c∂_x)(∂_t + c∂_x), so every solution is literally a left-moving wave plus a right-moving wave. That factoring doesn't exist in higher dimensions, so you can't just write down "F(x−ct) + G(x+ct)" in 2D or 3D.

That said, it generalizes in several directions, and each one is worth knowing:

- **Higher dimensions.** The 3D analogue is Kirchhoff's formula (spherical means), and the 2D one is Poisson's formula, obtained from Kirchhoff by the "method of descent." These are the same object — the solution operator for the Cauchy problem — just with a more complicated kernel. The comparison is also where you first meet Huygens' principle: in 3D a disturbance has a sharp trailing edge, while in 1D and 2D it lingers (that ∫g term is the 1D version of the lingering).
- **Source terms.** Duhamel's principle extends d'Alembert to u_tt − c²u_xx = F(x,t) by adding an integral of F over the characteristic triangle below (x,t). Same structure, one extra term.
- **Boundaries.** On a half-line or interval, you get the solution by extending the data (odd extension for Dirichlet, even for Neumann) and applying d'Alembert — the method of reflections.
- **Other hyperbolic equations in two variables.** Any constant-coefficient second-order hyperbolic PDE in (x,t) can be put into wave-equation canonical form by a linear change of variables, so d'Alembert covers all of them. For variable coefficients, Riemann's method is the direct descendant of the same approach.
- **The conceptual payload.** Characteristics, finite propagation speed, the domain of dependence / range of influence — all of that is first made visible by d'Alembert and holds for every hyperbolic equation, including nonlinear ones (Burgers, Euler) where no closed formula exists.

So think of it as the simplest member of a family rather than a one-off: the closed form is 1D-only, but the machinery behind it is the template for the whole theory of hyperbolic PDEs.