# Tensors, Part I
\toc
In this post I will be going through index notation, the basic
properties of tensors and two crucial functions that will allow
us to greatly simplify calculations and express quantities in a
concise manner.
## Kronecker's Delta
$$
\delta_{ij}=
\begin{cases}
    1, & \text{if } i=j \\
    0, & \text{if } i\neq j
\end{cases}
$$
It has the important property of index substitution
$$
a_i \delta_{ij} =a_j
$$
when the summation runs over all $i$'s. We can also play with
higher-order tensors and several Kronecker symbols.
$$
b_{ijk} \delta_{jp}\delta_{kq}=b_{ipq} \\
c_{ijkl} \delta_{jp} \delta_{pq} = c_{iqkl}
$$
From the definition it is also clear that it satisfies a
symmetry property and a dimensional property, since a
Kronecker delta is defined to act on a particular space
of dimension $n$, generally equal to $3$.
$$
\delta_{ij}=\delta_{ji} \\
\delta_{ij} \delta_{ji}=\delta_{ii}=n
$$
## Levi-Civita Symbol
