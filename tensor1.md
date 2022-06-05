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
$$a_i \delta_{ij} =a_j $$
when the summation runs over all $i$'s.
## Levi-Civita Symbol
