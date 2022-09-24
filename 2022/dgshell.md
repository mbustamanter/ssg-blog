# Differential Geometry for Shell Kinematics
\toc
## Differential Forms
### First Fundamental Form
### Second Fundamental Form
### Third Fundamental Form
### The Metric Tensor as a function of the fundamental forms
\begin{equation}
g_\alpha=a_\alpha-\xi^3 b^\lambda_\alpha a_\alpha
\end{equation}

\begin{equation}
g_3=\frac{\partial \varphi}{\partial \xi^3}=a_3
\end{equation}

\begin{align}
g_{\alpha \beta}&=
\inn{(a_\alpha-\xi^3 b^\lambda_\alpha a_\lambda),(a_\beta-\xi^3 b^\mu_\beta a_\mu)} \\
&=\inn{a_\alpha,a_\beta}-\xi^3 b^\lambda_\alpha \inn{a_\lambda,a_\beta}
-\xi^3 b^\mu_\beta\inn{a_\mu,a_\alpha}+(\xi^3)^2 b^\lambda_\alpha b^\mu_\beta\inn{a_\lambda,a_\mu}\\
&=a_{\alpha\beta}-\xi^3 b^\lambda_\alpha a_{\lambda\beta}-\xi^3 b^\mu_\beta a_{\mu\alpha}
+(\xi^3)^2 b^\lambda_\alpha b^\mu_\beta a_{\lambda\mu} \\
&=a_{\alpha\beta}-\xi^3 b_{\beta\alpha}-\xi^3 b_{\alpha\beta}
+(\xi^3)^2 b^\lambda_\alpha b_{\lambda\beta} \\
&=a_{\alpha\beta}-2\xi^3 b_{\alpha\beta}+(\xi^3)^2 c_{\alpha\beta}
\end{align}

\begin{equation}
g_{\alpha 3}=\inn{g_\alpha,g_3}=0
\end{equation}

\begin{equation}
g_{33}=\inn{g_3,g_3}=1
\end{equation}
## Shell Kinematics
\begin{equation}
U(\xi^1,\xi^2,\xi^3)=u(\xi^1,\xi^2)+\xi^3 \theta_\lambda(\xi^1,\xi^2)a^\lambda(\xi^1,\xi^2)
\end{equation}

\begin{equation}
e_{ij}=\frac 1 2 \par{\inn{g_i,U_{,j}}+\inn{g_j,U_{,i}}}
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
\inn{g_\beta,U_{,\alpha}}&=
\inn{(a_\beta-\xi^3 b^\mu_\beta a_\mu),(u_{\lambda|\alpha}-b_{\lambda\alpha}u_3
+\xi^3 \theta_{\lambda|\alpha})a^\lambda+(u_{3,\alpha}+b^\lambda_\alpha u_\lambda
+\xi^3 b^\lambda_\alpha \theta_\lambda)a_3} \\
&=(u_{\lambda|\alpha}-b_{\lambda\alpha}u_3+\xi^3 \theta_{\lambda|\alpha})\delta_{\beta\lambda}
-(u_{\lambda|\alpha}-b_{\lambda\alpha}u_3+\xi^3 \theta_{\lambda|\alpha})\xi^3
b^\mu_\beta \delta_{\mu\lambda} \\
&=u_{\beta|\alpha}-b_{\beta\alpha}u_3+\xi^3 \theta_{\beta|\alpha}
-(u_{\mu|\alpha}-b_{\mu\alpha}u_3+\xi^3 \theta_{\mu|\alpha}) \xi^3 b^\mu_\beta \\
&=u_{\beta|\alpha}-b_{\beta\alpha}u_3+\xi^3 \theta_{\beta|\alpha}
-\xi^3 b^\mu_\beta u_{\mu|\alpha}+\xi^3 b^\mu_\beta b_{\mu\alpha} u_3
-(\xi^3)^2 b^\mu_\beta \theta_{\mu|\alpha} \\
&=u_{\beta|\alpha}-b_{\beta\alpha}u_3
+\xi^3 (\theta_{\beta|\alpha}-b^\mu_\beta u_{\mu|\alpha}+c_{\alpha\beta}u_3)
-(\xi^3)^2 b^\mu_\beta \theta_{\mu|\alpha}
\end{align}

\begin{align}
\inn{g_3,U_{,\alpha}}=\inn{a_3,U_{,\alpha}}=u_{3,\alpha}+b^\lambda_\alpha u_\lambda
+\xi^3 b^\lambda_\alpha \theta_\lambda
\end{align}

\begin{align}
\inn{g_\alpha,U_{,3}} &=
\inn{(a_\alpha-\xi^3 b^\lambda_\alpha a_\lambda),\theta_\mu a^\mu} \\
&=\theta_\mu \delta_{\alpha\mu}-\xi^3 b^\lambda_\alpha \delta_{\lambda\mu} \theta_\mu
=\theta_\alpha-\xi^3 b^\lambda_\alpha \theta_\lambda
\end{align}