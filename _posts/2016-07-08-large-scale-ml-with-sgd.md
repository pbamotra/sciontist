---
layout: post
type: both
tag: paper, ml
title: Large-Scale Machine Learning with SGD
_url:
  - title: Why Python is slow: Looking under the hood
    type: fa-external-link
    uri: https://jakevdp.github.io/blog/2014/05/09/why-python-is-slow/
    heart: <span style="color:#19B5FE" title="Fascinating stuff"><i class="fa fa-bolt" aria-hidden="true"></i></span>
---
Link to paper: [L´eon Bottou, Large-Scale Machine Learning
with SGD](http://leon.bottou.org/publications/pdf/compstat-2010.pdf) <i class="fa fa-file-pdf-o" aria-hidden="true"></i>
<br />
<br />
Keypoints: -

- Under sufficient regularity assumptions, when the initial estimate $w_0$ is close enough to the optimum, and when the gain $\gamma$ is sufficiently small, this (gradient descent) algorithm achieves <b>linear convergence</b>, that is, -log $\rho$ $\backsim$ t, where $\rho$ represents the residual error.
- Much better optimization algorithms can be designed by replacing the scalar gain by a positive definite matrix $\Gamma_t$ that approaches the inverse of the Hessian of the cost at the optimum.
- This second order gradient descent (2GD) is a variant of the well known Newton algorithm. Under sufficiently optimistic regularity assumptions, and provided that $w_0$ is sufficiently close to the optimum, second order gradient descent achieves quadratic convergence.
- Since the stochastic algorithm does not need to remember which examples were visited during the previous iterations, it can process examples on the fly in a deployed system. In such a situation, the stochastic gradient descent directly optimizes the expected risk, since the examples are randomly drawn from the ground truth distribution.
- The convergence speed of stochastic gradient descent is in fact limited by the noisy approximation of the true gradient.
- Under sufficient regularity conditions, the best convergence speed is achieved using gains $\gamma_t$ $\propto$ $t^{-1}$.
- Although the stochastic gradient algorithms, SGD and 2SGD, are clearly the worst optimization algorithms, they need less time than the other algorithms to reach a predefined expected risk. Therefore, in the large scale setup, that is, when the limiting factor is the computing time rather than the number of examples, the stochastic learning algorithms performs asymptotically better!
