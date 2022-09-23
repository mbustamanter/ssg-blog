# Matrix Derivatives I: Low Order Traces
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
\begin{align*}
\frac{\partial}{\partial X} \tr(XA) & = \frac{\partial (X_{ij} A_{ji})}{\partial X_{kl}}
=\frac{\partial X_{ij}}{\partial X_{kl}} A_{ji} \\
& = \delta_{ik} \delta_{jl} A_{ji} =A_{lk} = (A^T)_{kl}=A^T
\end{align*}
$$
The same problem but with the transpose is tackled in the same fashion
$$
\begin{align*}
\frac{\partial}{\partial X} \tr(X^T A) & = \frac{\partial (X_{ij}^T A_{ji})}{\partial X_{kl}}
=\frac{\partial X_{ji}}{\partial X_{kl}} A_{ji} \\
& = \delta_{jk} \delta_{il} A_{ji} = A_{kl}
=A^T
\end{align*}
$$
As for the product of $X$ with two constant matrices, there are two index concatenations
in tensorial notation
$$
\begin{align*}
\frac{\partial}{\partial X} \tr(AXB) & =\frac{\partial (A_{ij} X_{jk} B_{ki})}{\partial X_{pq}}=
\frac{\partial X_{jk}}{\partial X_{pq}} A_{ij} B_{ki} = \delta_{jp} \delta_{kq} A_{ij}B_{ki} \\
& = A_{ip} B_{qi} = B_{qi} A_{ip} = (BA)_{qp}=(BA)_{pq}^T = (BA)^T \\
& = A^T B^T
\end{align*}
$$
and swapping $X$ for $X^T$
$$
\begin{align*}
\frac{\partial}{\partial X}\tr(AX^T B) & =\frac{\partial (A_{ij}X^T_{jk}B_{ki})}{\partial X_{pq}}
= \frac{\partial X_{kj}}{\partial X_{pq}} A_{ij} B_{ki} = \delta_{kp}\delta_{jq}A_{ij}B_{ki} \\
& = A_{iq}B_{pi}=B_{pi}A_{iq} = (BA)_{pq}=BA
\end{align*}
$$
## Second-Order Trace Derivatives
### Traces of $X^2$ and $X^2 B$
$$
\begin{align*}
\frac{\partial}{\partial X} \tr(X^2) & =\frac{\partial (X_{ij}X_{ji})}{\partial X_{pq}}
=\frac{\partial X_{ij}}{\partial X_{pq}} X_{ji}+X_{ij}\frac{\partial X_{ji}}{\partial X_{pq}} \\
& = \delta_{ip}\delta_{jq} X_{ji} +X_{ij} \delta_{jp}\delta_{iq} \\
& =X_{qp}+X_{qp}=2(X^T)_{pq}
=2X^T
\end{align*}
$$

\begin{align*}
\frac{\partial}{\partial X_{pq}} \tr(X^2 B) & =
\frac{\partial (X_{ij}X_{jk}B_{ki})}{\partial X_{pq}} \\
& = \frac{\partial X_{ij}}{\partial X_{pq}} X_{jk}B_{ki}
+ X_{ij}\frac{\partial X_{jk}}{\partial X_{pq}}B_{ki} \\
& = \delta_{ip} \delta_{jq} X_{jk} B_{ki} + X_{ij} \delta_{jp} \delta_{kq} B_{ki}
= X_{qk}B_{kp}+X_{ip}B_{qi}= (XB)_{qp} + B_{qi}X_{ip} \\
&=(XB)_{qp}+(BX)_{qp}=(XB+BX)^T_{pq}=(XB+BX)^T
\end{align*}
### Traces of $X^T B X$ and $XBX^T$
\begin{align*}
\frac{\partial}{\partial X} \tr(X^T BX) & = \frac{\partial (X_{ji}B_{jk}X_{ki})}{\partial X_{pq}}\\
& = \frac{\partial X_{ji}}{\partial X_{pq}} B_{jk}X_{ki}
+X_{ji}B_{jk} \frac{\partial X_{ki}}{\partial X_{pq}} \\
& = \delta_{jp}\delta_{iq} B_{jk}X_{ki}+X_{ji}B_{jk}\delta_{kp}\delta_{iq}
= B_{pk}X_{kq}+X_{jq}B_{jp} \\
& = (BX)_{pq}+ (B^T)_{pj} X_{jq} = (BX)_{pq}+(B^T X)_{pq}\\
&=(BX+B^T X)_{pq}=BX+B^T X
\end{align*}

\begin{align*}
\frac{\partial}{\partial X} \tr(XBX^T) &=
\frac{\partial (X_{ij}B_{jk}X_{ik})}{\partial X_{pq}} \\
&=\frac{\partial X_{ij}}{\partial X_{pq}} B_{jk}X_{ik}+
X_{ij}B_{jk} \frac{\partial X_{ik}}{\partial X_{pq}} \\
&=\delta_{ip}\delta_{jq}B_{jk}X_{ik}+X_{ij}B_{jk}\delta_{ip}\delta_{kq}
=B_{qk} X_{pk}+X_{pj} B_{jq} \\
&=X_{pk} (B^T)_{kq}+(XB)_{pq}=(XB^T)_{pq}+(XB)_{pq}=(XB^T+XB)_{pq} \\
&=XB^T+XB
\end{align*}
### Traces of $AXBX$, $B^T XCXB$, $X^T BXC$ and $AXBX^TC$
\begin{align*}
\frac{\partial}{\partial X} \tr(AXBX) &=
\frac{\partial (A_{ij}X_{jk}B_{kl}X_{li})}{\partial X_{pq}} \\
& = A_{ij} \frac{\partial X_{jk}}{\partial X_{pq}} B_{kl}X_{li}+
A_{ij}X_{jk}B_{kl}\frac{\partial X_{li}}{\partial X_{pq}} \\
&=A_{ij}\delta_{jp}\delta_{kq} B_{kl}X_{li}+
A_{ij}X_{jk}B_{kl}\delta_{lp}\delta_{iq}
=A_{ip}B_{ql}X_{li}+A_{qj}X_{jk}B_{kp} \\
&=(A^T)_{pi} (X^T)_{il} (B^T)_{lq} + (AXB)_{qp}=(A^T X^T B^T)_{pq}+(AXB)^T_{pq} \\
&=(A^T X^T B^T+(AXB)^T)_{pq}=A^T X^T B^T+B^T X^T A^T
\end{align*}

\begin{align*}
\frac{\partial}{\partial X} \tr(B^T XCBX) &=
\frac{\partial(B_{ji}X_{jk}C_{kl}B_{lm}X_{mi})}{\partial X_{pq}} \\
&=B_{ji} \frac{\partial X_{jk}}{\partial X_{pq}} C_{kl}B_{lm}X_{mi}+
B_{ji}X_{jk}C_{kl}B_{lm}\frac{\partial X_{mi}}{\partial X_{pq}} \\
&=B_{ji}\delta_{jp}\delta_{kq}C_{kl}B_{lm}X_{mi}+
B_{ji}X_{jk}C_{kl}B_{lm}\delta_{mp}\delta_{iq} \\
&=B_{pi}C_{ql}B_{lm}X_{mi}+B_{jq}X_{jk}C_{kl}B_{lp}
\end{align*}

\begin{align*}
\frac{\partial}{\partial X} \tr(X^TBXC)=
\end{align*}

\begin{align*}
\frac{\partial}{\partial X} \tr(AXBX^TC)=
\end{align*}