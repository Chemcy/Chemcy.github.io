[TOC]

# chapter 2
## No CAPM
<!-- Definition of $\beta_p$ -->
**Eq 2.1**

$$\beta_p=\frac {Cov(r_P, r_M)} {Var(r_M)} \ (2.1)$$

1. **Excess returns** are defined as total return - risk-free return
2. *any* portfolio P with **excess returns**$r_P$
3. market portfolio M with **excess returns** $r_M$

**Eq 2.2**

$$r_p(t)=\alpha_P + \beta_P r_M(t) + \epsilon_P(t) \ (2.2)$$

1. the **estimates** of $\beta_P$ and $\alpha_P$ are called ___realized___ or ___historical___ beta and alpha

**Eq 2.3**

Given a portfolio's beta:
$$r_p=\beta_P r_M + \theta_P \ (2.3)$$

1. ***residual return*** $\theta_P$ is uncorrelated with market return $r_M$

**Eq 2.4**

$$\sigma_P^2 = \beta_P^2 \sigma_M^2 + \omega_p^2 \ (2.4)$$

1. $\omega_p^2$ is residual variance of portfolio P, i.e., the variance of $\theta_P$

## The CAPM

**Eq 2.5**

$$E(r_P)=\beta_PE(r_M)=\beta_P\mu_M \ (2.5)$$

- Under the CAPM, the expected residual return on any stock or portfolio is **zero**. Expected excess returns are proportional to the stock's beta.

- Under the CAPM, an individual whose portfolio differs from the market is playing a **zero-sum game**. The player has **additional risk** and **no additional expected return**. This logic leads to passive investing; i.e., buy and hold the market portfolio.

## Technical appendix
**mathmatical notation**
$\pmb h$ vector of risky asset holdings
$\pmb f$ vector of expected excess returns
$\pmb \mu$ vector of expected excess returns under CAPM
$\pmb V$ covariance matrix of excess returns for risky assets
$\pmb \beta$ vector of asset betas
$\pmb e$ vector of ones

**Assumptions**
Consider a single period with no rebalancing of the portfolio within the period:

* A1. A risk-free asset exists.
* A2. All first and second momentums exist.
* A3. It is not possible to build a fully invested portfolio that has zero risk
* A4. The expected excess return on portfolio C, the fully invested portfolio with minimum risk, is positive.

###Characteristic Portfolios
Let $\pmb a^T=({a_1, a_2,..., a_N})$ be any vector of asset ***attributes*** or ***characteristics***. The ***exposure*** of portfolio $\pmb h_P$ to attribute $\pmb a$ is simply $a_P = \pmb h^T\pmb a$.

**Eq 2A.1**

$$\pmb h_a = \frac {\pmb V^{-1} \pmb a} {\pmb a^T \pmb V^{-1} \pmb a} \ (2A.1)$$

* **Characteristic portfolio** has minimum risk and unit exposure to $\pmb a$.
* $\pmb h_a$ gives the holdings of characteristic portfolio.

**Eq 2A.2**

$$\pmb \sigma_a^2 = \pmb h_a^T \pmb V \pmb h_a = \frac {1} {\pmb a^T \pmb V^{-1} \pmb a} \ (2A.2)$$

* Variance of characteristic portfolio $\pmb h_a$.

**Eq 2A.3**
$$ \pmb a = \frac {\pmb V \pmb h_a} {\pmb \sigma_a^2} \ (2A.3)$$

* The **beta** of all assets with respect to portfolio $\pmb h_a$ is equal to $\pmb a$.
* Note that $\pmb \beta=\pmb V \pmb h_p / \pmb \sigma_p^2$

**Eq 2A.4**
$$\pmb \sigma_{a, d} = \pmb a_d \pmb \sigma_a^2 = \pmb d_a \pmb \sigma_d^2 \ (2A.4)$$

* $\pmb a_d$ is exposure of portfolio $\pmb h_d$ to characteristic a.
* $\pmb d_a$ is exposure of portfolio $\pmb h_a$ to characteristic d.

If characteristic $ \pmb a$ is a weighted combination of characteristic $\pmb d$ and $ \pmb f$, i.e. $\pmb a = \pmb \kappa_d \pmb d+ \pmb \kappa_f \pmb f$:


**Eq 2A.5, 2A.6**
$$
\pmb h_a = 
(\frac {\pmb \kappa_d \pmb \sigma_a^2} {\pmb \sigma_d^2})\pmb h_d 
+ (\frac {\pmb \kappa_f \pmb \sigma_a^2} {\pmb \sigma_f^2})\pmb h_f
\ (2A.5)
$$
where
$$
\frac 1 {\pmb \sigma_a^2} = 
(\frac {\pmb \kappa_d \pmb a_d} {\pmb \sigma_d^2})
+ (\frac {\pmb \kappa_f \pmb a_f} {\pmb \sigma_f^2})
\ (2A.6)
$$

### Portfolio $C$

$$\pmb e^T = \{1,1,..., 1\} \ (2A.13)$$

$$\pmb h_C=\frac {\pmb V^{-1} \pmb e} {\pmb e^T \pmb V^{-1} \pmb e} \ (2A.14)$$

$$\pmb \sigma_C^2 = \pmb h_C^T \pmb V \pmb h_C = \frac {1} {\pmb e^T \pmb V^{-1} \pmb e} \ (2A.15)$$

* Every asset has a beta of 1 with respect to $C$.
* Given $e_P = \Sigma_n h_{P, n}$, for any portfolio P, we have $\sigma_{P, C} = e_p \sigma_C^2$

### Portfolio $B$
Given benchmark portfolio $\pmb B$ and define $\pmb \beta$ as:

$$\beta = \frac {\pmb V \pmb h_B} {\pmb \sigma_B^2} \ (2A.18)$$

Then the benchmark is the characteristic portfolio of beta, i.e.,

$$\pmb h_\beta=\frac {\pmb V^{-1} \pmb \beta} {\pmb \beta^T \pmb V^{-1} \pmb \beta}= \pmb h_B \ (2A.19)$$

### Portfolio $q$

* Define **Sharpe Ratio** as
$${SR}_P = \frac {\pmb f_P} {\pmb \sigma_p} \ (2A.22)$$
$$\pmb h_q=\frac {\pmb V^{-1} \pmb f} {\pmb f^T \pmb V^{-1} \pmb f} \ (2A.23)$$

Then

1. $$SR_q=max(SR_P | P)={(\pmb f^T \pmb V^{-1} \pmb f)^{\frac 1 2}} \ (2A.24)$$
2. $$f_q=1\ (2A.25), \  \sigma_q^2=\frac 1 {\pmb f^T \pmb V^{-1} \pmb f} \ (2A.26)$$
3. $$\pmb f =(\frac {\pmb V \pmb h_q} {\sigma_q}SR_q) \ (2A.27)$$
4. $$SR_p = \rho_{P,q}SR_q \ (2A.28)$$
5. $$e_q = \frac {f_C \sigma_q^2} {\sigma_C^2} \ (2A.29)$$

### Portfolio $A$
Define alpha as $\pmb \alpha=\pmb f - \pmb \beta f_B$.

### Portfolio $Q$

* Let portfolio $Q$ be the characteristic portfolio of $e_q\pmb f$.
* Portfolio Q is fully invested, with holdings $\pmb h_Q= \pmb h_q/e_q$
* $SR_Q=SR_p$
* For any portfolio P with a correlation $\rho_{P,Q}$ with portfolio $Q$, 

1. $$SR_P = \rho_{P,Q}SR_Q \ (2A.34)$$
2. $$\frac {f_C} {\sigma_C^2} = \frac {f_Q} {\sigma_Q^2} \ (2A.35)$$
$$\pmb f = f_Q(\frac {\pmb V \pmb h_Q} {\sigma_Q^2}) = f_Q \pmb \beta_{with\ respect\ to\ Q} \ \ \ \ (2A.36)$$
3. $$\beta_Q=\frac {f_B \sigma_Q^2} {f_Q \sigma_B^2}$$
4. $$\beta_Q = \frac {\beta_Cf_B} {f_C}$$
