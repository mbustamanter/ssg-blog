@def title = "Integration by parts"
# Integration by parts in $\mathbb R^n$ and applications
\toc
## Review of the Basic Theorems
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
$\scal{\grad u , \nu}$. Analogously, applying again \eqref{basic int} to
the products $u v_{x_i}$ and summing over $i$ one gets
$$
\int_U \scal{\grad u, \grad v} dx = -\int_{\partial U} u\Delta v dx
+\int_{\partial U} u \frac{\partial v}{\partial \nu} dS
\label{int 4}
$$
Finally, taking advantage of symmetry in the LHS of \eqref{int 4}
by expressing it in terms of $\Delta u$ results in
$$
\int_U (u\Delta v-v\Delta u) dx =
\int_{\partial U} \left ( u\frac{\partial v}{\partial \nu}-v\frac{\partial u}{\partial \nu} \right ) dS
$$
Two often overlooked identities are related to the biharmonic operator and fall
as corollaries of the former relations are
$$
\int_U u \Delta^2 v dx= \int_{\partial U} u \frac{ \partial \Delta v}{\partial \nu} dS
-\int_{\partial U} \Delta v \frac{\partial u}{\partial \nu} dS
+\int_U \Delta u \Delta v dx
\label{bi1}
$$
and for the symmetrical case
$$
\int_U \par{u \Delta^2 v-v\Delta^2 u}dx=
\int_{\partial U} \par{u \frac{\partial \Delta v}{\partial \nu}-
v\frac{\partial \Delta u}{\partial \nu}} dS
+\int_{\partial U} \par{\Delta u \frac{\partial v}{\partial \nu}-
v\frac{\partial u}{\partial \nu}}dS
$$
as an evident consequence of \eqref{bi1}. To prove \eqref{bi1}, use \eqref{int 4}
to see that
$$
\int_U u \Delta^2 v dx = -\int_U \scal{\grad u, \grad \Delta v} dx
+\int_{\partial U} u \frac{\partial \Delta v}{\partial \nu} dS
$$
and that the integral over $U$ can in turn be decomposed as
$$
\int_U \scal{\grad u, \grad\Delta v} dx=
-\int_U \Delta u \Delta v dx +
\int_{\partial U} \Delta v \frac{\partial u}{\partial \nu} dS
$$
## Applications
### Energy Methods
#### Wave Equation on $\R^n \times (0,\infty)$
Let $u \in C^2(\mathbb R^n \times (0,\infty))$ be a solution of
$$
\begin{cases}
u_{tt}-c^2 \Delta u=0 & (x,t) \in \R^n \times (0,\infty) \\
u(x,0)=g(x) & x \in \R^n \\
u_t(x,0)=h(x) & x \in \R^n
\label{wave-prob}
\end{cases}
$$
Where $g$ and $h$ have compact support. Define the energy functional
$$
E(t)=\frac 1 2 \int_{\R^n} \par{u_t^2 +c^2 \norm{\grad u}^2}dx
$$
To prove that there is indeed _conservation_ of energy we will differentiate
$E$ to arrive at
$$
E'(t)=\frac 1 2 \int_{\R^n} \par{2u_t u_{tt}+2\sum_{i=1}^n u_{x_i} u_{x_i t}} dx \\
= \int_{\R^n} \par{u_t u_{tt}+\scal{\grad u , \grad u_t}} dx
$$
Bearing in mind that all the derivatives of functions with compact support also
have compact support, $u$ and $u_t$ are zero save for a set $U \subseteq \R^n$.
Applying \eqref{int 4} to the last expression gives
$$
E'(t)=\int_U u_t u_{tt} dx -\int_U c^2 u_t \Delta u dx +\int_{\partial U}
u_t \frac{\partial u}{\partial \nu} dS \\
= \int_U u_t (u_{tt}-c^2\Delta u) dx =0
$$
Hence $E$ is constant over $[0,\infty)$. This also provides uniqueness for the
equation: suppose $u_1$ and $u_2$ satisfy \eqref{wave-prob}, so their difference
$w=u_1-u_2$ satisifies the wave equation with homogeneous boundary conditions.
We know in this case $E(0)=0$ and it is equal to a constant in the general case,
so $E(t)=0$ for all $t>0$. This immediately implies $w$ constant, and by initial
data $w=0$.
#### Wave Equation
### Weak Formulation (sometimes solutions)
#### Biharmonic Equation
#### Advection-Diffusion-Reaction Equation
$$
\begin{cases}
-\dive(\mu \grad u) + \scal{b, \grad u}+cu=s & U \\
u=g & \Gamma_D \\
\mu \frac{\partial u}{\partial \nu} = r & \Gamma_N \\
\mu \frac{\partial u}{\partial \nu} = \gamma & \Gamma_R
\end{cases}
$$
To find the weak formulation, introduce the space
$$V=\left \{v \in H^1(U): v|_{\Gamma_D}=0\right \}$$
we mutliply the first equation by $v \in V$ and integrate over $U$.