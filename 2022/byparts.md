@def title = "Integration by parts"
# Integration by parts in $\mathbb R^n$
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
$\inn{\grad u , \nu}$. Analogously, applying again \eqref{basic int} to
the products $u v_{x_i}$ and summing over $i$ one gets
$$
\int_U \inn{\grad u, \grad v} dx = -\int_{\partial U} u\Delta v dx
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
\int_U u \Delta^2 v dx = -\int_U \inn{\grad u, \grad \Delta v} dx
+\int_{\partial U} u \frac{\partial \Delta v}{\partial \nu} dS
$$
and that the integral over $U$ can in turn be decomposed as
$$
\int_U \inn{\grad u, \grad\Delta v} dx=
-\int_U \Delta u \Delta v dx +
\int_{\partial U} \Delta v \frac{\partial u}{\partial \nu} dS
$$