Title: An overview of Stochastic Gradient Estimation techniques
description: How do you propagate gradients when using non-continuous functions in your network?
hero: How do you propagate gradients when using non-continuous functions in your network?
authors:
    - Abhishek Aggarwal
date: 2019-12-26

# **Stochastic Gradient Estimation**

# Problem statement 
We are given "well behaved"[^1] distribution $q_{\phi}(z),\ z \in \mathbb{R},\ \phi \in \mathbb{R}$. We are also given cost function $f(z) \in \mathbb{R}$ and a loss function $\mathcal{L}(\phi) = \mathbb{E}_{q_{\phi}(z)}[f(z)]$. We want to calculate unbiased [^2] stochastic estimator for $\mathcal{L}'(\phi)$ 

$$
\mathcal{L}'(\phi) = \mathbb{E}_{q_{\phi}(z)}[g(z, \phi)]
$$

As such, if we can calculate the gradient $g(z, \phi)$ then we can compute Monte Carlo estimate for practical applications.

$$
\mathcal{L}'(\phi) \approx \frac{1}{M}\sum_{i=1}^M g(z_i, \phi),\ \ z_i \sim q_{\phi}(z)
$$


[^1]: Differentiable density and no inner regions of zero density.
[^2]: Unbiased just means that if expecation is calculated for infinite samples, then we converge to the true expectation without any offset.


## Reference
- [Michael Figurnov (DeepMind) in DeepBayes2018](https://www.youtube.com/watch?v=BV465lgleHA)
