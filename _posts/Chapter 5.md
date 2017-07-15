[TOC]

#Text
## Definition of Alpha

$$r_P(t) = \alpha_P + \beta_P \cdot r_B(t) + \epsilon_P(t) \ (5.1)$$

- $r_P(t)$ are portfolio excess returns in periods $t = 1,2,...T$
- $r_B(t)$ are benchmark excess returns over those same periods

$$\pmb \theta_P(t) = \pmb \alpha_P + \pmb \epsilon_p(t) \ (5.2)$$
- $\theta$ are residual returns for portfolio $\pmb P$
- The estimated $\pmb \beta_P$ and $\pmb \alpha_P$ from **regression** are ***realized*** or ***historical*** beta and alpha.
- $\pmb \alpha_P$ is the average residual return and $\pmb \epsilon_p(t)$ is the mean zero random component of residual return.

When looking to the future, alpha is a forecast of residual return.
$$\pmb \alpha = E(\pmb \theta) \ (5.3)$$

$$\alpha_P = \pmb h_P^T \cdot \pmb \alpha \ (5.4)$$

## Ex post IR

- An ***information ratio***, denoted IR, is a ratio of (annualized) residual return to (annualized) residual risk.

## Ex ante IR

$$IR_P = \frac {\alpha_P} {\omega_P} \ (5.5)$$

- The information ratio is independent of the manager’s level of aggressiveness.

$${\alpha_P} = IR \cdot {\omega_P} \ (5.7)$$
$$VA[P] = {\alpha_P} - {\lambda_R} \cdot {\omega_P}^2 \ (5.8)$$

$$VA[{\omega_P}] = {\omega_P} \cdot IR - {\lambda_R} \cdot {\omega_P}^2 \ (5.9)$$
$$\omega^{\star}=\frac {IR} {2\lambda_R} \ (5.10)$$

# Technical Appendix
## Portfolio $A$