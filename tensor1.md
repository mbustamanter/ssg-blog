# Tensors, Part I
\toc
In this post I will be going through index notation, the basic
properties of tensors and two crucial functions that will allow
us to greatly simplify calculations and express quantities in a
concise manner. The index represenation of a tensor consists
in
## Kronecker's Delta
\begin{equation}
\delta_{ij}=
\begin{cases}
    1, & \text{if } i=j \\
    0, & \text{if } i\neq j
\end{cases}
\end{equation}
It has the important property of index substitution
\begin{equation}
a_i \delta_{ij} =a_j
\end{equation}
when the summation runs over all $i$'s. We can also play with
higher-order tensors and several Kronecker symbols.
\begin{equation}
b_{ijk} \delta_{jp}\delta_{kq}=b_{ipq} \\
c_{ijkl} \delta_{jp} \delta_{pq} = c_{iqkl}
\end{equation}
From the definition it is also clear that it satisfies a
symmetry property and a dimensional property, since a
Kronecker delta is defined to act on a particular space
of dimension $n$, generally equal to $3$.
\begin{equation}
\delta_{ij}=\delta_{ji} \\
\delta_{ij} \delta_{ji}=\delta_{ii}=n
\end{equation}
When dealing with the canonical basis in $\R^n$, inner products among
basis vectors coincide with the Kronecker delta
\begin{equation}
\inn{e_i,e_j}=\delta_{ij}
\end{equation}
## Levi-Civita Symbol
\begin{equation}
\varepsilon_{ijk}=
\begin{cases}
1, & \text{if $i,j,k$ are different and in cyclic order} \\
-1, & \text{if $i,j,k$ are different not in cyclic order} \\
0, & \text{if at least two of $i,j,k$ are equal}
\end{cases}
\end{equation}
## Vector Algebra computations
\begin{equation}
\inn{u,v}=\inn{u_i e_i, v_j e_j}=u_i v_j \inn{e_i,e_j}=u_i v_j \delta_{ij}=u_i v_i
\end{equation}