[TOC]

# Chapter 3 of APT

## Background
Active risk $\psi_P$:
$$\psi_P = Std(r_{PA})=Std(r_P - r_B) \ (3.7)$$

$$\omega_P = \sqrt {\sigma_P^2 - \beta_P^2 \cdot \sigma_B^2}  \ (3.8)$$

$$\beta_P = \frac {Cov(r_P, r_B)} {Var(r_B)} \ (3.9)$$

Covariance matrix $V$.

## Single-factor model of risk:

$$r_n = \beta_n \cdot r_M + \theta_n \ (3.11)$$

$$Cov(r_n, r_m) = \beta_n \cdot \beta_m \cdot \sigma_m^2 \ (3.12)$$
and
$$\sigma_n^2 = \beta_n^2 \cdot \sigma_M^2 + \omega_n^2 \ (3.13)$$

$$Cov(r_n, r_m) = \sigma_n \cdot \sigma_m \cdot \rho \ (3.15)$$

## Structural Risk Model

$$r_n(t) = \Sigma_k {X_{n, t}(t) \cdot b_k(t) + u_n(t)} \ (3.16)$$

- $r_n(t)$: excess return (return above the risk-free return) on stock n during the period from time t to time t + 1
- $X_{n, t}(t)$: exposure of asset n to factor k, estimated at time t. Exposures are frequently called factor loadings. For the other common factors, the exposures are standardized s
o that the average exposure over all stocks is 0, and the standard deviation across stocks is 1.
- $b_k(t)$: factor return to factor k during the period from time t to time t + 1.
- $u_n(t)$: stock n's specific return during the period from time t to time t + 1.

$$V_{n, m} = \sum_{k_1,k_2=1}^K {X_{n, k_1} \cdot F_{k_1, k_2} \cdot X_{m, k_2} + \Delta_{n, m}} \ (3.17)$$


# TA

$$\pmb r = \pmb X \cdot \pmb b + \pmb u (3A.1)$$

Assumptions
A1 $Cov(u_n, b_k) = 0$ for all $n$ and $k$.
A2 $Cov(u_n, u_m) = 0$  if $m \neq n$.

$$\pmb V = \pmb X \cdot \pmb F \cdot \pmb X^T + \pmb \Delta \ (3A.2)$$

Estimated factor returns:

$$\pmb b = (\pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb X)^{-1} \cdot \pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb r \ (3A.3)$$

## Specific risk modeling

$$u_n^2(t) = S(t)[1+v_n(t)] \ (3A.5)$$
with
$$\frac 1 N \cdot \sum_{n=1}^{N}u_n^2(t) = S(t) \ (3A.6)$$
and 
$$\frac 1 N \cdot \sum_{n=1}^{N}v_n(t) = 0 \ (3A.6)$$

## Risk analysis

Factor exposure of portfolio $P$.
$$\chi_P = \pmb X^T \cdot h_P \ (3A.8)$$

Variance of $P$
$$\sigma_P^2 =\pmb \chi_{P}^T \cdot \pmb F \cdot \pmb \chi_{P} + \pmb h_{P}^T \cdot \pmb \Delta \cdot \pmb h_{P} = \pmb h_{P}^T \cdot \pmb V \cdot \pmb h_{P} (3A.9)$$

Active:
$$\pmb h_{PA} = \pmb h_p - \pmb h_B \ (3A.10)$$
$$\pmb \chi_{PA} = \pmb X^T \cdot \pmb h_{PA} \ (3A.11)$$

Active risk:

$$\psi_P = Std(r_{PA})=Std(r_P - r_B) \ (3.7)$$
$$\psi_P^2 =\pmb \chi_{PA}^T \cdot \pmb F \cdot \pmb \chi_{PA} + \pmb h_{PA}^T \cdot \pmb \Delta \cdot \pmb h_{PA} = \pmb h_{PA}^T \cdot \pmb V \cdot \pmb h_{PA} \ (3A.12)$$


$$\pmb \beta = \frac {\pmb V \cdot \pmb h_B} {\sigma_B^2} = \frac {\pmb X \cdot \pmb F \cdot \pmb \chi_B + \pmb \Delta \cdot \pmb h_B} {\sigma_B^2} \ (3A.13)$$

$$\pmb \beta = \pmb X \cdot \pmb b + \pmb d \ (3A.16)$$
$$\pmb b = \frac {\pmb F \cdot \pmb \chi_B} {\sigma_B^2} \ (3A.14)$$
$$\pmb d = \frac {\pmb \Delta \cdot \pmb h_B} {\sigma_B^2} \ (3A.15)$$

$$\beta_P = \pmb h_P^T \cdot \pmb \beta = \pmb \chi_P^T \cdot \pmb b + \pmb h_P^T \cdot \pmb d \ (3A.17)$$
$$\beta_{PA} = \pmb h_{PA}^T \cdot \pmb \beta = \pmb \chi_{PA}^T \cdot \pmb b + \pmb h_{PA}^T \cdot \pmb d$$

$$\sigma_P^2 = \beta_P^2 \cdot \sigma_B^2 + \omega_P^2 \ (3A.18)$$

- Residual covariance matrix

$$\pmb {VR} = \pmb V - \pmb \beta \cdot \sigma_B^2 \cdot \pmb \beta^2$$

## Attribution of Risk

### Marginal Contribution

- Marginal contribution for total risk:
$$\pmb {MCTR} = \frac {\partial \sigma_P} {\partial \pmb h_P^T} = \frac {\pmb V \cdot \pmb h_P} {\sigma_P} \ (3A.20)$$

The $\pmb {MCTR}(n)$ is the partial derivative of $\sigma_P$ with respect to $\pmb h_P(n)$.
We can think of it as the approximate change in portfolio risk given a 1 percent increase in the holding of asset n, financed by decreasing the cash account by 1 percent. 
To first order:
$$\Delta \sigma_P \approx \Delta_P^T \cdot \pmb {MCTR} \ (3A.21)$$

- Marginal contribution to residual risk:
$$\pmb {MCRR} = \frac {\pmb {VR} \cdot \pmb h_{P}} {\omega_P} = \frac {\pmb V \cdot \pmb h_{PR}} {\omega_P} \ (3A.22)$$

- $\pmb h_{PR} = \pmb h_P - \beta_P \cdot \pmb h_B$ is the residual holdings vector for portfolio $P$.
- In comparison: $\pmb h_{PA} = \pmb h_p - \pmb h_B \ (3A.10)$


- Marginal contribution to active risk:
$$\pmb {MCAR} = \frac {\pmb {V} \cdot \pmb h_{PA}} {\psi_P} \ (3A.23)$$


$$\pmb {MCAR} = \pmb \beta \cdot k_1 + \pmb {MCRR} \cdot k_2 \ (3A.24)$$
where
$$k_1 = \frac {\beta_{PA} \cdot \sigma_B^2} {\psi_P}\ (3A.26)$$
$$k_2 = \frac {\omega_P} {\psi_P}(3A.26)$$

### Factor Marginal Contributions

$$\pmb h_{PA} \rightarrow \pmb h_{PA} + [(\pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb X)^{-1} \cdot \pmb X^T \cdot \pmb \Delta^{-1}]^T \cdot \pmb \delta_k (3A.27)$$ 
where $[(\pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb X)^{-1} \cdot \pmb X^T \cdot \pmb \Delta^{-1}]$ is the $K$ by $N$ vector of factor portfolios, and $\delta_k$ is a $K$ by 1 vector containing zeros except in the $k^{th}$ row.


$$\delta \psi_P = [[(\pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb X)^{-1} \cdot \pmb X^T \cdot \pmb \Delta^{-1}]^T \cdot \pmb \delta_k]^T \cdot \pmb {MCAR} = \pmb \delta_k^T \cdot (\pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb X)^{-1} \cdot \pmb X^T \cdot \pmb \Delta^{-1} \cdot \frac {\pmb {V} \cdot \pmb h_{PA}} {\psi_P} \ (3A.28)$$

$$\frac {\delta \psi_P} {\pmb \delta_K^T} = \frac {\pmb F \cdot \pmb \chi_{PA}} {\psi_P} + [\frac {(\pmb X^T \cdot \pmb \Delta^{-1} \cdot \pmb X)^{-1} \cdot \pmb \chi_{PA}} {\psi_P}] \ (3A.29)$$

$$\frac {\delta \psi_P} {\pmb \delta_K^T} \approx \frac {\pmb F \cdot \pmb \chi_{PA}} {\psi_P} \ (3A.30)$$

### Attribution of Risk
$$\pmb h_{PA}^T \cdot \pmb {MCAR} =\pmb h_{PA}^T \cdot  \frac {\pmb {V} \cdot \pmb h_{PA}} {\psi_P} = {\psi_P} \ (3A.31)$$

$$\frac {\pmb h_{PA}^T \cdot \pmb {MCAR}} {\psi_P} = 1 \ (3A.32)$$

$$\Delta {\psi_P} \approx \Delta h_{PA}(n) \cdot \pmb {MCAR}(n) \approx [\frac {\Delta h_{PA}(n)} {h_{PA}(n)} ]\cdot h_{PA}(n) \cdot \pmb {MCAR}(n) \ (3A.34)$$


Relative marginal contribution to active risk ($\pmb {RMCAR}(n)$):
$$\pmb {RMCAR}(n) = h_PA(n) \cdot MCAR(n) \ (3A.35)$$

### Attribution to Factors
Factor marginal contribution to active risk ($\pmb {FMCAR}$)
$$\pmb {FMCAR}= \frac {\partial \psi_P} {\partial \pmb \chi_{PA}^T} = \frac {\pmb F \cdot \pmb \chi_{PA}} {\psi_{PA}} \ (3A.38)$$


### Correlations and Market Volatility
$$\rho_{n, m} = \frac {\beta_n \cdot \beta_m \cdot \sigma_M^2} {\sqrt{(\beta_n^2 \cdot \sigma_M^2 + \omega_n^2) \cdot (\beta_m^2 \cdot \sigma_M^2 + \omega_m^2)}} \ (3A.40)$$

But now let's assume that both assets have betas of 1, and identical residual risk.
$$\rho_{n, m} \rightarrow \frac {\sigma_M^2} {\sigma_M^2 + \omega^2} \ (3A.41)$$