# Matrix Derivatives I
\toc
## Definition
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
### Trace of $X$
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
### Traces of $XA$, $X^T A$, $AXB$ and $AX^T B$
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
The same problem but with the transpose is tackled in the same fashion
$$
\frac{\partial}{\partial X} \tr(X^T A)= \frac{\partial (X_{ij}^T A_{ji})}{\partial X_{kl}}
=\frac{\partial X_{ji}}{\partial X_{kl}} A_{ji} = \delta_{jk} \delta_{il} A_{ji} = A_{kl}
=A^T
$$

$$
\tr(AXB)=\frac{\partial (A_{ij} X_{jk} B_{ki})}{\partial X_{pq}}
$$

## Second-Order Trace Derivatives
### Traces of $X^2$ and $X^2 B$
### Traces of $X^T B X$ and $XBX^T$
### Traces of $AXBX$, $B^T XCXB$, $X^T BXC$ and $AXBX^TC$