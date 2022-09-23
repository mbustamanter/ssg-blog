# Differential Geometry for Shell Kinematics
\toc
## Differential Forms
### First Fundamental Form
### Second Fundamental Form
### Third Fundamental Form
### The Metric Tensor as a function of the fundamental forms
## Shell Kinematics
\begin{equation}
U(\xi^1,\xi^2,\xi^3)=u(\xi^1,\xi^2)+\xi^3 \theta_\lambda(\xi^1,\xi^2)a^\lambda(\xi^1,\xi^2)
\end{equation}

\begin{equation}
e_{ij}=\frac 1 2 \par{g_i \cdot U_{,j}+g_j \cdot U_{,i}}
\end{equation}

\begin{align}
\frac{\partial u}{\partial\xi^\alpha}&=
\frac{\partial}{\partial\xi^\alpha}(u_\lambda a^\lambda+u_3a_3) \\
&=u_{\lambda|\alpha}a^\lambda+b^\lambda_\alpha u_\lambda a_3+u_{3,\alpha}a_3+u_3 a_{3,\alpha}\\
&=u_{\lambda|\alpha}a^\lambda-b_{\lambda\alpha}u_3 a^\lambda
+(u_{3,\alpha}+b^\lambda_\alpha u_\lambda)a_3 \\
&=(u_{\lambda|\alpha}-b_{\lambda\alpha}u_3)a^\lambda+(u_{3,\alpha}+b^\lambda_\alpha u_\lambda)a_3
\end{align}

\begin{equation}
\frac{\partial}{\partial \xi^\alpha} (\theta_\lambda a^\lambda)
=\theta_{\lambda|\alpha} a^\lambda+b^\lambda_\alpha \theta_\lambda a_3
\end{equation}

\begin{align}
\frac{\partial U}{\partial \xi^\alpha} &=
\frac{\partial u}{\partial \xi^\alpha}
+\xi^3 \frac{\partial (\theta_\lambda a^\lambda)}{\partial \xi^\alpha} \\
&=(u_{\lambda|\alpha}-b_{\lambda\alpha}u_3+\xi^3 \theta_{\lambda|\alpha})a^\lambda
+(u_{3,\alpha}+b^\lambda_\alpha u_\lambda+\xi^3 b^\lambda_\alpha \theta_\lambda)a_3
\end{align}

\begin{equation}
\frac{\partial U}{\partial \xi^3}=\theta_\lambda a^\lambda
\end{equation}

\begin{align}
e_{\alpha \beta} &=
\end{align}