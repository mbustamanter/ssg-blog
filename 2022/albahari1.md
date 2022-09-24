# Albahari Integrals
## Integrals (Euler's Formula)
\begin{align}
I_1 &=\int_0^\infty e^{-st}\cos(at)dt=\Re(I_3) \\
I_2 &=\int_0^\infty e^{-st}\sin(at)dt=\Im(I_3) \\
I_3 &= I_1+i I_2=\int_0^\infty e^{-(s+ia)t}dt=\frac{s}{s^2+a^2}-i\frac{a}{s^2+a^2}
\end{align}

\begin{align}
J_1 &=\int_0^1 e^{-tx} \cos(2\pi nx)dx=\Re(J_3) \\
J_2 &=\int_0^1 e^{-tx} \sin(2\pi nx)dx=\Im(J_3) \\
J_3 &=\int_0^1 e^{-x(t+2\pi in)} dx=\frac{t(1-e^{-t})}{t^2+(2\pi n)^2}
-i\frac{2\pi n(1-e^{-t})}{t^2+(2\pi n)^2}
\end{align}