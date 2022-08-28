@def title = "Integration by parts"
# Integration by parts in $\mathbb R^n$ and applications
\toc
## The Basic Theorems
In what follows, $U$ is assumed to be an open, bounded subset of
$\mathbb R ^n$ with $C^1$ boundary and $u$, $v$ sufficiently
regular functions. Then
$$
\int_U u_{x_i} dx = \int_{\partial U} u\nu_i dS
\label{basic int}
$$
is the basic identity from which the following are built. Applied
to the product $uv$, this gives
$$
\int_U u_{x_i}v dx = -\int_U uv_{x_i} dx+\int_{\partial U} uv\nu_i dS
$$
And applying \eqref{basic int} to the first-order derivatives
$u_{x_i}$ and adding up the equalities we obtain
$$
\int_U \Delta u dx = \int_{\partial U} \frac{\partial u}{\partial \nu} dS
$$
where $\frac{\partial u}{\partial \nu}$ is defined to be equal to
the inner product between the gradient and the outward unit vector,
$\scal{\grad u \cdot \nu}$. Analogously, applying again \eqref{basic int} to
the products $u v_{x_i}$ and summing over $i$ one gets
$$
\int_U \scal{\grad u \cdot \grad v} dx = -\int_{\partial U} u\Delta v dx
+\int_{\partial U} u \frac{\partial v}{\partial \nu} dS
\label{int 4}
$$
Finally, taking advantage of symmetry in the LHS of \eqref{int 4}
by expressing it in terms of $\Delta u$ results in
$$
\int_U (u\Delta v-v\Delta u) dx =
\int_{\partial U} \left ( u\frac{\partial v}{\partial \nu}-v\frac{\partial u}{\partial \nu} \right ) dS
$$
## Applications
### Energy Methods
#### Wave Equation
Let $u \in C^2(\mathbb R^n \times (0,\infty))$ be a solution of
$$
\begin{cases}
u_{tt}=c^2 \Delta u & (x,t) \in \R^n \times (0,\infty) \\
u(x,0)=g(x) & x \in \R^n \\
u_t(x,0)=h(x) & x \in \R^n
\end{cases}
$$
Define the energy functional
$$
E(t)=\frac 1 2 \int_{\R^n} \lparen u_t^2 +c^2 \norm{\grad u}^2 \rparen dx
$$
to prove that there is indeed _conservation_ of energy we will differentiate
$E$ to arrive at
### Weak Formulation (sometimes solutions)
#### Biharmonic Equation
#### Advection-Diffusion-Reaction Equation