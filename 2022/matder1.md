# Matrix Derivatives I
Here I will explain how to compute particular cases of matrix
derivatives using tensor notation. First, a simple and quite
intuitive rule for determining derivatives of matrix components
with respect to an arbitrary matrix component is stated.
$$
\frac{\partial X_{ij}}{\partial X_{kl}}=\delta_{ik} \delta_{jl}
\label{matrix der def}
$$
We'll first begin by exposing the differentiation of simple expressions
involving traces of the matrix with which we differentiate and traces
of products of constant matrices with the variable matrix.
\eqref{matrix der def}, along with the product rule are the protagonists
in all these manipulations.
## First-Order Trace Derivatives
$$
\frac{\partial}{ \partial X} \tr(X)=I \\
\label{simp prob 1}
$$
To solve this first problem notice that the trace of $X$ in tensor
notation is written as $X_{ii}$, that is, with same first and last indices
$$
\frac{\partial}{\partial X} \tr(X) = \frac{\partial X_{ii}}{\partial X_{kl}}
= \delta_{ik} \delta_{il}=\delta_{kl}=I
$$
where the last equality is true because the derivative is a second-order
tensor whose indices must be the same as the ones used to derivate.
$$
\frac{\partial}{\partial X} \tr(XA)=A^T
$$
For this situation we use the fact that dot product of tensors must
have equal adjacent indices between terms
$$
\frac{\partial}{\partial X} \tr(XA) = \frac{\partial (X_{ij} A_{ji})}{\partial X_{kl}}
=\frac{\partial X_{ij}}{\partial X_{kl}} A_{ji} = \delta_{ik} \delta_{jl} A_{ji}
=A_{lk} = (A^T)_{kl}=A^T
$$
Now, 
## Second-Order Trace Derivatives
## Third-Order Trace Derivatives