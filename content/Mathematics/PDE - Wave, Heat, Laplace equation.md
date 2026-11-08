# General PDE
**Second Order PDE**^[$L$ is an operator]
$$
Lu=\sum_{i,j}a_{ij}\partial_{i}\partial_{j}u+\sum_{i}b_{i}\partial_{i}u+cu
$$

**Second Order PDE with two independent variables**
$$
Au_{xx}+2Bu_{xy}+Cu_{yy}+Du_{x}+Eu_{y}+F=0
$$


#  Prototypical PDEs
- **Wave equation** - $u_{tt}=c^2\nabla^2u=c^2(u_{{xx}}+u_{yy}+u_{zz})$ 
- **Heat equation** - $u_t = k\nabla^2u$
- **Laplace's equation** - $\nabla^2 u=0$


# Prototypical Solutions
- **d'Alembert's formula** is the general solution to the 1D wave equation
	- 1D wave equation:$u_{tt}-c^2u_{xx}=0$
	- with initial condition$\left\{\begin{smallmatrix*}[l] u(x,0) = g(x), \\ u_t(x,0) = h(x), \end{smallmatrix*}\right. \qquad \text{where } -\infty<x<\infty,\ t>0.$
	- $u(x,t) = ½[g(x − ct) + g(x + ct)] + (1/2c) ∫_{x−ct}^{x+ct} h(s) ds$
	







Fable's Book Recommendations
```markdown
It depends on your level and what you want out of it. The standard picks:

**First course (undergraduate, applied flavor)**

- **Haberman, _Applied Partial Differential Equations with Fourier Series and Boundary Value Problems_.** The classic for a first pass: separation of variables, Fourier series, Sturm–Liouville, Green's functions, done slowly and concretely with lots of worked problems. Very forgiving.
- **Strauss, _Partial Differential Equations: An Introduction_.** Shorter and more mathematical than Haberman, but still accessible. Good if you want proofs alongside computation and a clear treatment of the wave/heat/Laplace trio and the classification we talked about.
- **Farlow, _Partial Differential Equations for Scientists and Engineers_.** Cheap Dover paperback, 47 short "lessons," each one a single technique. Ideal if you want a quick refresher or a survey of methods rather than a deep course.

**Second course (graduate, rigorous)**

- **Evans, _Partial Differential Equations_.** The standard graduate text. Part I covers the explicit methods, Part II builds Sobolev spaces and weak solutions, Part III does nonlinear theory. Demanding but extremely well written, and it's what most graduate courses use.
- **John, _Partial Differential Equations_.** Older and terser than Evans, but elegant, and especially good on the Cauchy problem and hyperbolic equations.

**Specialized**

- **Olver, _Introduction to Partial Differential Equations_.** Sits between Strauss and Evans; strong on symmetry methods and clear about where numerics come in.
- **LeVeque, _Finite Volume Methods for Hyperbolic Problems_** and **Trefethen, _Spectral Methods in MATLAB_** if you want the numerical side done properly.
- **Logan, _Applied Partial Differential Equations_.** Short, modern, and unusually good on the method of characteristics and nonlinear waves.

If you want a single recommendation: Strauss if you're reviewing or want the math, Haberman if you want to learn to compute solutions, Evans if you're heading toward research.
```
