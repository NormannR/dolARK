## Perturbation

Solving models with heterogeneous agents and aggregate uncertainty is possible through many methods. In this section, we explain how to use DolARK to apply the perturbation method presented by [Reiter (2008)](https://doi.org/10.1016/j.jedc.2008.08.010). On this basis, we also explain how to reduce the dimensionality of the state-space. We notably show how to implement the method developed in [Bayer and Luetticke (2019)](https://uca610a4a83db144640feb22a4f0.dl.dropboxusercontent.com/cd/0/inline2/ApwE_yaKJ4BKGW2vI7e2qBI5o5p9KoHpswIoQe5oWUKSgglSFiANgMpJwHxsKUHBRevccidaJA2kezIE8gUXkaKKUOxnTT1E84WsYvSAIpSQ6jE4MmvfjSH092Ie8heRDYQUJG94fUNPLFN1K4GChp8GHzJf0pd7mdn6Dkl1tkhp95Sumsl7Igk5QBgpr6jpDoD-Cm2Q9q6ayL4nOvPLFl-ivPDUdCfkts8_eyt7fORxCWR9lUEFOaS3BeMm-Go5dKiyJ-I0D44RMUTx6YPq5-9i8g_8pTfauv0YzB6LfkI4QBCUCEGoMDx1WIhg52XwMGtSs5QnMkpqJUq3xLjX0rk9/file).

### Method

The solving procedure can be simply summed up in two steps
1. Finding the steady-state equilibrium, as detailed in the [Equilibrium](./equilibrium/) section
2. Perturbing variables around the steady-state

More formally, the model can be split into transition equations and abritrage equations. Transition equations are

$$
m_{t+1} = \tau \left( m_t \right)\\
\mu_{t+1} = \Pi \left( x_t \right) \mu_t
$$

Arbitrage equations are

$$
x_t = \mathcal T \left( x_{t+1}, y_t, y_{t+1}\right)\\
0 = \mathcal A \left( \mu_t, x_t, m_t, y_t\right) 
$$